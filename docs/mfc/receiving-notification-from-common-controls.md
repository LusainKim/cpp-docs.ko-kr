---
title: "공용 컨트롤에서 알림 받기 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ON_NOTIFY"
  - "WM_NOTIFY"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "공용 컨트롤[C++], 알림"
  - "컨트롤[MFC], 알림"
  - "알림, 공용 컨트롤"
  - "ON_NOTIFY 매크로"
  - "OnNotify 메서드"
  - "공용 컨트롤에서 알림 수신"
  - "Windows 공용 컨트롤[C++], 알림"
  - "WM_NOTIFY 메시지"
ms.assetid: 50194592-d60d-44d0-8ab3-338a2a2c63e7
caps.latest.revision: 11
caps.handback.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 공용 컨트롤에서 알림 받기
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Common controls are child windows that send notification messages to the parent window when events, such as input from the user, occur in the control.  
  
 The application relies on these notification messages to determine what action the user wants it to take.  Most common controls send notification messages as **WM\_NOTIFY** messages.  Windows controls send most notification messages as **WM\_COMMAND** messages.  [CWnd::OnNotify](../Topic/CWnd::OnNotify.md) is the handler for the **WM\_NOTIFY** message.  As with `CWnd::OnCommand`, the implementation of `OnNotify` dispatches the notification message to `OnCmdMsg` for handling in message maps.  The message\-map entry for handling notifications is `ON_NOTIFY`.  For more information, see [Technical Note 61: ON\_NOTIFY and WM\_NOTIFY Messages](../mfc/tn061-on-notify-and-wm-notify-messages.md).  
  
 Alternately, a derived class can handle its own notification messages using "message reflection." For more information, see [Technical Note 62: Message Reflection for Windows Controls](../mfc/tn062-message-reflection-for-windows-controls.md).  
  
## Retrieving the Cursor Position in a Notification Message  
 On occasion, it is useful to determine the current position of the cursor when certain notification messages are received by a common control.  For example, it would be helpful to determine the current cursor location when a common control receives a **NM\_RCLICK** notification message.  
  
 There is a simple way to accomplish this by calling `CWnd::GetCurrentMessage`.  However, this method only retrieves the cursor position at the time the message was sent.  Because the cursor may have been moved since the message was sent you must call **CWnd::GetCursorPos** to get the current cursor position.  
  
> [!NOTE]
>  `CWnd::GetCurrentMessage` should only be called within a message handler.  
  
 Add the following code to the body of the notification message handler \(in this example, **NM\_RCLICK**\):  
  
 [!code-cpp[NVC_MFCControlLadenDialog#4](../mfc/codesnippet/CPP/receiving-notification-from-common-controls_1.cpp)]  
  
 At this point, the mouse cursor location is stored in the `cursorPos` object.  
  
## 참고 항목  
 [컨트롤 만들기 및 사용](../mfc/making-and-using-controls.md)   
 [컨트롤](../mfc/controls-mfc.md)