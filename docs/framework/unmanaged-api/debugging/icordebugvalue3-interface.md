---
title: "ICorDebugValue3 接口"
ms.custom: 
ms.date: 03/30/2017
ms.prod: .net-framework
ms.reviewer: 
ms.suite: 
ms.technology: dotnet-clr
ms.tgt_pltfrm: 
ms.topic: reference
api_name: ICorDebugValue3
api_location: mscordbi.dll
api_type: COM
f1_keywords: ICorDebugValue3
helpviewer_keywords: ICorDebugValue3 interface [.NET Framework debugging]
ms.assetid: 7d5385d3-f4a5-47c4-8478-a3513b5e9406
topic_type: apiref
caps.latest.revision: "6"
author: rpetrusha
ms.author: ronpet
manager: wpickett
ms.openlocfilehash: 3948a4c404036235767f8de6747966709b75bc4c
ms.sourcegitcommit: 4f3fef493080a43e70e951223894768d36ce430a
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2017
---
# <a name="icordebugvalue3-interface"></a><span data-ttu-id="4784a-102">ICorDebugValue3 接口</span><span class="sxs-lookup"><span data-stu-id="4784a-102">ICorDebugValue3 Interface</span></span>
<span data-ttu-id="4784a-103">扩展"ICorDebugValue"和"ICorDebugValue2"接口，以支持大于 2 GB 的数组。</span><span class="sxs-lookup"><span data-stu-id="4784a-103">Extends the "ICorDebugValue" and "ICorDebugValue2" interfaces to provide support for arrays that are larger than 2 GB.</span></span>  
  
## <a name="methods"></a><span data-ttu-id="4784a-104">方法</span><span class="sxs-lookup"><span data-stu-id="4784a-104">Methods</span></span>  
  
|<span data-ttu-id="4784a-105">方法</span><span class="sxs-lookup"><span data-stu-id="4784a-105">Method</span></span>|<span data-ttu-id="4784a-106">描述</span><span class="sxs-lookup"><span data-stu-id="4784a-106">Description</span></span>|  
|------------|-----------------|  
|[<span data-ttu-id="4784a-107">GetSize64 方法</span><span class="sxs-lookup"><span data-stu-id="4784a-107">GetSize64 Method</span></span>](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)|<span data-ttu-id="4784a-108">获取以字节为单位，此大小，`ICorDebugValue3`对象。</span><span class="sxs-lookup"><span data-stu-id="4784a-108">Gets the size, in bytes, of this `ICorDebugValue3` object.</span></span>|  
  
## <a name="remarks"></a><span data-ttu-id="4784a-109">备注</span><span class="sxs-lookup"><span data-stu-id="4784a-109">Remarks</span></span>  
 <span data-ttu-id="4784a-110">[Icordebugvalue:: Getsize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md)方法返回介于 0 到 2,147,483,647 个字节的范围的对象大小。</span><span class="sxs-lookup"><span data-stu-id="4784a-110">The [ICorDebugValue::GetSize](../../../../docs/framework/unmanaged-api/debugging/icordebugvalue3-getsize64-method.md) method returns an object size that ranges from 0 to 2,147,483,647 bytes.</span></span> <span data-ttu-id="4784a-111">在[!INCLUDE[net_v45](../../../../includes/net-v45-md.md)]，数组的大小可以超过 2 GB。</span><span class="sxs-lookup"><span data-stu-id="4784a-111">In the [!INCLUDE[net_v45](../../../../includes/net-v45-md.md)], the size of arrays can exceed 2 GB.</span></span> <span data-ttu-id="4784a-112">`ICorDebugValue3`接口使您能够确定这些阵列的大小。</span><span class="sxs-lookup"><span data-stu-id="4784a-112">The `ICorDebugValue3` interface enables you to determine the size of these arrays.</span></span>  
  
## <a name="requirements"></a><span data-ttu-id="4784a-113">要求</span><span class="sxs-lookup"><span data-stu-id="4784a-113">Requirements</span></span>  
 <span data-ttu-id="4784a-114">**平台：**请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。</span><span class="sxs-lookup"><span data-stu-id="4784a-114">**Platforms:** See [System Requirements](../../../../docs/framework/get-started/system-requirements.md).</span></span>  
  
 <span data-ttu-id="4784a-115">**标头：** CorDebug.idl、 CorDebug.h</span><span class="sxs-lookup"><span data-stu-id="4784a-115">**Header:** CorDebug.idl, CorDebug.h</span></span>  
  
 <span data-ttu-id="4784a-116">**库：** CorGuids.lib</span><span class="sxs-lookup"><span data-stu-id="4784a-116">**Library:** CorGuids.lib</span></span>  
  
 <span data-ttu-id="4784a-117">**.NET framework 版本：**[!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span><span class="sxs-lookup"><span data-stu-id="4784a-117">**.NET Framework Versions:** [!INCLUDE[net_current_v45plus](../../../../includes/net-current-v45plus-md.md)]</span></span>  
  
## <a name="see-also"></a><span data-ttu-id="4784a-118">另请参阅</span><span class="sxs-lookup"><span data-stu-id="4784a-118">See Also</span></span>  
    
    
 [<span data-ttu-id="4784a-119">调试接口</span><span class="sxs-lookup"><span data-stu-id="4784a-119">Debugging Interfaces</span></span>](../../../../docs/framework/unmanaged-api/debugging/debugging-interfaces.md)  
 [<span data-ttu-id="4784a-120">调试</span><span class="sxs-lookup"><span data-stu-id="4784a-120">Debugging</span></span>](../../../../docs/framework/unmanaged-api/debugging/index.md)