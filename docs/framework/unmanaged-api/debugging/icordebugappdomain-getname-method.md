---
title: ICorDebugAppDomain::GetName 方法
ms.date: 03/30/2017
api_name:
- ICorDebugAppDomain.GetName
api_location:
- mscordbi.dll
api_type:
- COM
f1_keywords:
- ICorDebugAppDomain::GetName
helpviewer_keywords:
- ICorDebugAppDomain::GetName method [.NET Framework debugging]
- GetName method, ICorDebugAppDomain interface [.NET Framework debugging]
ms.assetid: 02c596d7-00b0-4e2c-856b-5425158fcefd
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 84f895e749fc8f2520dbce3caf9e6c11fda78a7a
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33405764"
---
# <a name="icordebugappdomaingetname-method"></a>ICorDebugAppDomain::GetName 方法
获取应用程序域的名称。  
  
## <a name="syntax"></a>语法  
  
```  
HRESULT GetName (  
    [in]  ULONG32           cchName,  
    [out] ULONG32           *pcchName,  
    [out, size_is(cchName), length_is(*pcchName)]   
         WCHAR              szName[]  
);  
```  
  
#### <a name="parameters"></a>参数  
 `cchName`  
 [in] `szName` 数组的大小。 将此值设置为零，以将此方法放在查询模式。  
  
 `pcchName`  
 [out]名称或中实际返回的字符数的大小的指针`szName`。 在查询模式下，此值允许调用方知道多大的缓冲区分配的名称。  
  
 `szName`  
 [out]存储应用程序域的名称数组。  
  
## <a name="remarks"></a>备注  
 调试器将调用`GetName`方法一次，以获取名称所需的缓冲区的大小。 调试器分配缓冲区，，然后调用该方法的第二个时间以填充的缓冲区。 要获取的大小的名称，第一个调用被称为*查询模式*。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** CorDebug.idl、 CorDebug.h  
  
 **库：** CorGuids.lib  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]
