---
title: StrongNameGetBlobFromImage 函数
ms.date: 03/30/2017
api_name:
- StrongNameGetBlobFromImage
api_location:
- mscoree.dll
api_type:
- DLLExport
f1_keywords:
- StrongNameGetBlobFromImage
helpviewer_keywords:
- StrongNameGetBlobFromImage function [.NET Framework strong naming]
ms.assetid: 1de658e6-da32-4d01-9097-6f43c92222e1
topic_type:
- apiref
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: 9d562aef58c1e3b5bbbe690b54eb08384052c657
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
ms.locfileid: "33456770"
---
# <a name="strongnamegetblobfromimage-function"></a>StrongNameGetBlobFromImage 函数
获取位于指定的内存地址处的二进制表示形式的程序集映像。  
  
 此函数已弃用。 使用[iclrstrongname:: Strongnamegetblobfromimage](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)方法相反。  
  
## <a name="syntax"></a>语法  
  
```  
BOOLEAN StrongNameGetBlobFromImage (  
    [in]  BYTE        *pbBase,  
    [in]  DWORD       dwLength,  
    [in]  BYTE        *pbBlob,  
    [in, out] DWORD   *pcbBlob  
);  
```  
  
#### <a name="parameters"></a>参数  
 `pbBase`  
 [in]映射程序集清单内存地址。  
  
 `dwLength`  
 [in]大小，以字节为单位，在图像的`pbBase`。  
  
 `pbBlob`  
 [in]用于包含图像的二进制表示的缓冲区。  
  
 `pcbBlob`  
 [在中，out]请求的最大大小，以字节为单位， `pbBlob`。 返回时，实际大小，以字节为单位的`pbBlob`。  
  
## <a name="return-value"></a>返回值  
 `true` 在成功完成;否则为`false`。  
  
## <a name="remarks"></a>备注  
 如果`StrongNameGetBlobFromImage`函数未成功完成，请调用[StrongNameErrorInfo](../../../../docs/framework/unmanaged-api/strong-naming/strongnameerrorinfo-function.md)函数可检索的最后一个生成的错误。  
  
## <a name="requirements"></a>要求  
 **平台：** 请参阅[系统要求](../../../../docs/framework/get-started/system-requirements.md)。  
  
 **标头：** StrongName.h  
  
 **库：** 作为 MsCorEE.dll 中的资源  
  
 **.NET framework 版本：** [!INCLUDE[net_current_v10plus](../../../../includes/net-current-v10plus-md.md)]  
  
## <a name="see-also"></a>请参阅  
 [StrongNameGetBlobFromImage 方法](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblobfromimage-method.md)  
 [StrongNameGetBlob 方法](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-strongnamegetblob-method.md)  
 [ICLRStrongName 接口](../../../../docs/framework/unmanaged-api/hosting/iclrstrongname-interface.md)
