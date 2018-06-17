---
title: WM\_CHOOSEFONT\_GETLOGFONT message
description: An application sends the WM\_CHOOSEFONT\_GETLOGFONT message to a Font dialog box to retrieve information about the user's current font selections.
ms.assetid: afbf953a-13dd-409b-a988-f1426c8bbd31
keywords:
- WM_CHOOSEFONT_GETLOGFONT message Dialog Boxes
topic_type:
- apiref
api_name:
- WM_CHOOSEFONT_GETLOGFONT
api_location:
- Commdlg.h
api_type:
- HeaderDef
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# WM\_CHOOSEFONT\_GETLOGFONT message

An application sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to a **Font** dialog box to retrieve information about the user's current font selections.


```C++
#define WM_USER                        0x0400
#define WM_CHOOSEFONT_GETLOGFONT      (WM_USER + 1)
```



## Parameters

<dl> <dt>

*wParam* 
</dt> <dd>

This parameter is not used.

</dd> <dt>

*lParam* 
</dt> <dd>

A pointer to a [**LOGFONT**](https://msdn.microsoft.com/library/windows/desktop/dd145037) structure that receives information about the user's current font selections.

</dd> </dl>

## Return value

This message does not return a value.

## Remarks

The [**ChooseFont**](/windows/desktop/api/Commdlg/ns-commdlg-tagchoosefonta) function creates a **Font** dialog box. When the user closes the **Font** dialog box, the **ChooseFont** function returns information about the user's font selections in the [**CHOOSEFONT**](/windows/desktop/api/Commdlg/ns-commdlg-tagchoosefonta) structure. The **lpLogFont** member of the **CHOOSEFONT** structure is a pointer to a [**LOGFONT**](https://msdn.microsoft.com/library/windows/desktop/dd145037) structure.

Use the **WM\_CHOOSEFONT\_GETLOGFONT** message to get information about the user's current font selections while the **Font** dialog box is open. For example, if you enable the **Apply** button in the **Font** dialog box, send the message to get the font information to apply to the current text selection.

Typically, you enable a [*CFHookProc*](https://msdn.microsoft.com/en-us/library/ms646909(v=VS.85).aspx) hook procedure to process [**WM\_COMMAND**](https://msdn.microsoft.com/library/windows/desktop/ms647591) messages for the **Apply** button. When the user clicks the **Apply** button, the hook procedure sends the **WM\_CHOOSEFONT\_GETLOGFONT** message to the dialog box.

## Requirements



|                                     |                                                                                                          |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 2000 Professional \[desktop apps only\]<br/>                                               |
| Minimum supported server<br/> | Windows 2000 Server \[desktop apps only\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Commdlg.h (include Windows.h)</dt> </dl> |



## See also

<dl> <dt>

**Reference**
</dt> <dt>

[**CFHookProc**](https://msdn.microsoft.com/en-us/library/ms646909(v=VS.85).aspx)
</dt> <dt>

[**ChooseFont**](/windows/desktop/api/Commdlg/ns-commdlg-tagchoosefonta)
</dt> <dt>

[**CHOOSEFONT**](/windows/desktop/api/Commdlg/ns-commdlg-tagchoosefonta)
</dt> <dt>

[**WM\_COMMAND**](https://msdn.microsoft.com/library/windows/desktop/ms647591)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Common Dialog Box Library](common-dialog-box-library.md)
</dt> <dt>

**Other Resources**
</dt> <dt>

[**LOGFONT**](https://msdn.microsoft.com/library/windows/desktop/dd145037)
</dt> </dl>

 

 




