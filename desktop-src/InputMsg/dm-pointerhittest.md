---
title: DM\_POINTERHITTEST message
description: Sent to a window, when pointer input is first detected, in order to determine the most probable input target for Direct Manipulation.
ms.assetid: E4CE60F0-0C2A-440A-8F64-B070867A1572
keywords:
- DM_POINTERHITTEST message Input Messages and Notifications
topic_type:
- apiref
api_name:
- DM_POINTERHITTEST
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# DM\_POINTERHITTEST message

\[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.\]

Sent to a window, when pointer input is first detected, in order to determine the most probable input target for [Direct Manipulation](https://msdn.microsoft.com/library/windows/desktop/hh446969).

> \[!Important\]  
> Desktop apps should be DPI aware. If your app is not DPI aware, screen coordinates contained in pointer messages and related structures might appear inaccurate due to DPI virtualization. DPI virtualization provides automatic scaling support to applications that are not DPI aware and is active by default (users can turn it off). For more information, see [Writing High-DPI Win32 Applications](https://msdn.microsoft.com/library/windows/desktop/dd464660).

 


```C++
#define DM_POINTERHITTEST       0x0250
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

Unused.

</dd> <dt>

*lParam* 
</dt> <dd>

Unused.

</dd> </dl>

## Return value

NULL

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 10 \[desktop apps only\]<br/>                                                              |
| Minimum supported server<br/> | Windows Server 2016 \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

[Messages](messages.md)
</dt> </dl>

 

 




