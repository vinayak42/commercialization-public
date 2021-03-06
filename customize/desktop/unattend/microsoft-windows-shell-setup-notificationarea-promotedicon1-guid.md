---
title: GUID
description: GUID
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 98fb9868-a86d-4457-a28c-7c0742819ae8
ms.mktglfcycl: deploy
ms.sitesec: msdn
author: themar-msft
ms.author: themar
ms.date: 05/02/2017
ms.topic: article
ms.prod: windows-hardware
ms.technology: windows-oem
---

# GUID


`GUID` specifies the globally unique identifier (GUID) of an icon to be shown in the notification area at the far right of the taskbar.

By setting the [Path](microsoft-windows-shell-setup-notificationarea-promotedicon1-path.md) and GUID elements of the PromotedIcon1 component, you can configure another icon to be visible in the notification area. This icon will appear in place of the **Action Center** icon.

To select the icon to be visible, you must:

-   Select a signed binary-application file that includes a system-notification icon.

-   Set both the **Path** and **GUID** elements for the file.

The GUID for the icon is contained in the application. The NOTIFYICONDATA shell structure contains the guidItem. For more information, see the MSDN topic: [NOTIFYICONDATA](http://go.microsoft.com/fwlink/?LinkId=120340). For third-party applications, contact your application provider to find out if your application uses this structure and to obtain the GUID.

## Values


<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>GUID</p></td>
<td><p>Specifies the GUID of an icon to be shown in the notification area.</p></td>
</tr>
</tbody>
</table>

 

This string type does not support empty elements. Do not create an empty value for this setting.

## Valid Configuration Passes


specialize

## Parent Hierarchy


[Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md) | [NotificationArea](microsoft-windows-shell-setup-notificationarea.md) | [PromotedIcon1](microsoft-windows-shell-setup-notificationarea-promotedicon1.md) | **GUID**

## Applies To


For a list of the Windows editions and architectures that this component supports, see [Microsoft-Windows-Shell-Setup](microsoft-windows-shell-setup.md).

## XML Example


The following XML output shows how to promote a new notification icon to be visible in place of the **Action Center** icon.

```
  <PromotedIcon1>
    <Path>%PROGRAMFILES%\Fabrikam\Application1.exe</Path>
    <GUID>{d8742dcb-3e6a-4b3c-b3fe-374623cdcf06}</GUID>
  </PromotedIcon1>
```

## Related topics


[PromotedIcon1](microsoft-windows-shell-setup-notificationarea-promotedicon1.md)

[NOTIFYICONDATA Structure](http://go.microsoft.com/fwlink/?LinkId=120340)

 

 







