---
title: '&lt;specifiedPickupDirectory&gt;元素 （网络设置）'
ms.date: 03/30/2017
f1_keywords:
- http://schemas.microsoft.com/.NetConfiguration/v2.0#specifiedPickupDirectory
- http://schemas.microsoft.com/.NetConfiguration/v2.0#configuration/system.net/mailSettings/smtp/specifiedPickupDirectory
helpviewer_keywords:
- specifiedPickupDirectory element
- <specifiedPickupDirectory> element
ms.assetid: 0121f49d-bff2-4bc6-af06-f1628dcd61f1
author: mcleblanc
ms.author: markl
manager: markl
ms.openlocfilehash: 50ab7387fc5e2cac65cac1a6dba0e563225beec9
ms.sourcegitcommit: 59b51cd7c95c75be85bd6ef715e9ef8c85720bac
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/06/2018
ms.locfileid: "37874697"
---
# <a name="ltspecifiedpickupdirectorygt-element-network-settings"></a>&lt;specifiedPickupDirectory&gt;元素 （网络设置）
配置简单邮件传输协议 (SMTP) 服务器的本地目录。  
  
 \<configuration>  
\<system.net>  
\<mailSettings>  
\<smtp>  
\<specifiedPickupDirectory>  
  
## <a name="syntax"></a>语法  
  
```xml  
<specifiedPickupDirectory  
  pickupDirectoryLocation="directory"   
/>  
```  
  
## <a name="attributes-and-elements"></a>特性和元素  
 下列各节描述了特性、子元素和父元素。  
  
### <a name="attributes"></a>特性  
  
|特性|描述|  
|---------------|-----------------|  
|`pickupDirectoryLocation`|在应用程序在其中保存以供以后处理的 SMTP 服务器的电子邮件的目录。|  
  
### <a name="child-elements"></a>子元素  
 无。  
  
### <a name="parent-elements"></a>父元素  
  
|元素|描述|  
|-------------|-----------------|  
|[\<smtp > 元素 （网络设置）](../../../../../docs/framework/configure-apps/file-schema/network/smtp-element-network-settings.md)|配置简单邮件传输协议 (SMTP) 邮件发送选项。|  
  
## <a name="remarks"></a>备注  
 `specifiedPickupDirectory` 特性设置应用程序保存邮件以供 SMTP 服务器处理的目录。  
  
## <a name="example"></a>示例  
 下面的示例指定 c:\maildrop 作为邮件的拾取目录。  
  
```xml  
<configuration>  
  <system.net>  
    <mailSettings>  
      <smtp deliveryMethod="SpecifiedPickupDirectory">  
        <specifiedPickupDirectory  
          pickupDirectoryLocation="c:\maildrop"  
        />  
      </smtp>  
    </mailSettings>  
  </system.net>  
</configuration>  
```  
  
## <a name="see-also"></a>请参阅  
 <xref:System.Net.Mail.SmtpClient?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.SmtpSection?displayProperty=nameWithType>  
 <xref:System.Net.Configuration.SmtpSpecifiedPickupDirectoryElement?displayProperty=nameWithType>  
 [网络设置架构](../../../../../docs/framework/configure-apps/file-schema/network/index.md)
