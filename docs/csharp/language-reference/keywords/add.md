---
title: add（C# 参考）
ms.date: 07/20/2015
f1_keywords:
- add_CSharpKeyword
helpviewer_keywords:
- add event accessor [C#]
ms.assetid: faf30b99-10e8-45cd-ab9a-57585d4d1d8d
ms.openlocfilehash: 143acc0d6e1989232f80ee74bf748d6c600b9741
ms.sourcegitcommit: 6bc4efca63e526ce6f2d257fa870f01f8c459ae4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36207868"
---
# <a name="add-c-reference"></a>add（C# 参考）
`add` 上下文关键字用于定义一个在客户端代码订阅你的[事件](../../../csharp/language-reference/keywords/event.md)时调用的自定义事件访问器。 如果提供自定义 `add` 访问器，还必须提供 [remove](../../../csharp/language-reference/keywords/remove.md) 访问器。  
  
## <a name="example"></a>示例  
 如下示例显示一个具有自定义 `add` 和 [remove](../../../csharp/language-reference/keywords/remove.md) 访问器的事件。 有关完整示例，请参阅[如何：实现接口事件](../../../csharp/programming-guide/events/how-to-implement-interface-events.md)。  
  
[!code-csharp[csrefKeywordsContextual#15](~/samples/snippets/csharp/VS_Snippets_VBCSharp/csrefKeywordsContextual/CS/csrefKeywordsContextual.cs#15)]
  
 通常不需要提供自己的自定义事件访问器。 大多数情况下，使用声明事件时由编译器自动生成的访问器就足够了。  
  
## <a name="see-also"></a>请参阅  
 [事件](../../../csharp/programming-guide/events/index.md)
