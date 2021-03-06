---
title: 使用实现 IDisposable 的对象
ms.date: 04/07/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- Dispose method
- try/finally block
- garbage collection, encapsulating resources
ms.assetid: 81b2cdb5-c91a-4a31-9c83-eadc52da5cf0
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 7c586c725a385029db80763ba13915be79c6cd7e
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33576319"
---
# <a name="using-objects-that-implement-idisposable"></a>使用实现 IDisposable 的对象

公共语言运行时的垃圾回收器回收托管对象使用的内存，而使用非托管资源的类型则实现 <xref:System.IDisposable> 接口，以允许回收分配给这些非托管资源的内存。 在使用完实现 <xref:System.IDisposable> 的对象后，应调用该对象的 <xref:System.IDisposable.Dispose%2A?displayProperty=nameWithType> 实现。 可以通过两种方法执行此操作：  
  
* 使用 C# `using` 语句或 Visual Basic `Using` 语句。  
  
* 实现 `try/finally` 块。  

## <a name="the-using-statement"></a>using 语句

C# 中的 `using` 语句和 Visual Basic 中的 `Using` 语句可以简化创建和清理对象而必须编写的代码。 `using` 语句获取一个或多个资源，执行指定的语句，并自动处置对象。 但是，`using` 语句仅对在用于构造对象的方法的范围内使用的对象有用。  
  
以下示例使用 `using` 语句创建并发布 <xref:System.IO.StreamReader?displayProperty=nameWithType> 对象。  
  
[!code-csharp[Conceptual.Disposable#1](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.disposable/cs/using1.cs#1)]
[!code-vb[Conceptual.Disposable#1](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.disposable/vb/using1.vb#1)]  
  
请注意，虽然 <xref:System.IO.StreamReader> 类实现 <xref:System.IDisposable> 接口（这指示使用非托管资源），但此示例不显式调用 <xref:System.IO.StreamReader.Dispose%2A?displayProperty=nameWithType> 方法。 当 C# 或 Visual Basic 编译器遇到 `using` 语句时，它会发出与以下显式包含 `try/finally` 块的代码等效的中间语言 (IL)。  
  
[!code-csharp[Conceptual.Disposable#3](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.disposable/cs/using3.cs#3)]
[!code-vb[Conceptual.Disposable#3](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.disposable/vb/using3.vb#3)]  
  
使用 C# `using` 语句，还可以在一个语句（在内部相当于嵌套语句 `using`）中获取多个资源。 下面的示例实例化两个 <xref:System.IO.StreamReader> 对象以读取两个不同文件的内容。  
  
[!code-csharp[Conceptual.Disposable#4](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.disposable/cs/using4.cs#4)]

## <a name="tryfinally-block"></a>Try/finally 块

可以选择直接实现 `try/finally` 块，而不是将 `try/finally` 块包装在 `using` 语句中。 这可以是私有编码样式，或者你可能出于下列原因之一需要这样做：  
  
* 包含 `catch` 块可处理 `try` 块中引发的任何异常。 否则，不会处理 `using` 语句引发的任何异常，`using` 块中引发的任何异常也是如此，前提是 `try/catch` 块不存在。  
  
* 实例化实现 <xref:System.IDisposable>（其范围对于声明它的块是非本地的）的对象。  
  
下面的示例与上一示例类似，不同之处在于此示例使用 `try/catch/finally` 块实例化、使用和清理 <xref:System.IO.StreamReader> 对象，同时处理 <xref:System.IO.StreamReader> 构造函数及其 <xref:System.IO.StreamReader.ReadToEnd%2A> 方法抛出的任何异常。 请注意，`finally` 块中的代码检查实现 <xref:System.IDisposable> 的对象在其调用 `null` 方法之前不为 <xref:System.IDisposable.Dispose%2A>。 此操作失败会导致运行时发生 <xref:System.NullReferenceException> 异常。  
  
[!code-csharp[Conceptual.Disposable#6](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.disposable/cs/using5.cs#6)]
[!code-vb[Conceptual.Disposable#6](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.disposable/vb/using5.vb#6)]  
  
如果选择实现或必须实现 `try/finally` 块，可以遵循此基本模式，因为编程语言不支持 `using` 语句，但允许直接调用 <xref:System.IDisposable.Dispose%2A> 方法。 
  
## <a name="see-also"></a>请参阅

[清理非托管资源](../../../docs/standard/garbage-collection/unmanaged.md)   
[using 语句（C# 参考）](~/docs/csharp/language-reference/keywords/using-statement.md)   
[Using 语句 (Visual Basic)](~/docs/visual-basic/language-reference/statements/using-statement.md)
