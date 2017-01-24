---
title: "프레임 창 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CFrameWnd 클래스, 프레임 창"
  - "문서 프레임 창"
  - "프레임 창[C++]"
  - "프레임 창[C++], 프레임 창 정보"
  - "MDI[C++], 프레임 창"
  - "MFC[C++], 프레임 창"
  - "SDI(단일 문서 인터페이스)"
  - "SDI(단일 문서 인터페이스), 프레임 창"
  - "분할 창, 및 프레임 창"
  - "뷰[C++], 및 프레임 창"
  - "창 클래스[C++], 프레임"
  - "창[C++], MDI"
ms.assetid: 40677339-8135-4f5e-aba6-3fced3078077
caps.latest.revision: 11
caps.handback.revision: 7
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 프레임 창
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

When an application runs under Windows, the user interacts with documents displayed in frame windows.  A document frame window has two major components: the frame and the contents that it frames.  A document frame window can be a [single document interface](../mfc/sdi-and-mdi.md) \(SDI\) frame window or a [multiple document interface](../mfc/sdi-and-mdi.md) \(MDI\) child window.  Windows manages most of the user's interaction with the frame window: moving and resizing the window, closing it, and minimizing and maximizing it.  You manage the contents inside the frame.  
  
## Frame Windows and Views  
 The MFC framework uses frame windows to contain views.  The two components — frame and contents — are represented and managed by two different classes in MFC.  A frame\-window class manages the frame, and a view class manages the contents.  The view window is a child of the frame window.  Drawing and other user interaction with the document take place in the view's client area, not the frame window's client area.  The frame window provides a visible frame around a view, complete with a caption bar and standard window controls such as a control menu, buttons to minimize and maximize the window, and controls for resizing the window.  The "contents" consist of the window's client area, which is fully occupied by a child window — the view.  The following figure shows the relationship between a frame window and a view.  
  
 ![프레임 창 보기](../mfc/media/vc37fx1.png "vc37FX1")  
프레임 창 및 뷰  
  
## Frame Windows and Splitter Windows  
 Another common arrangement is for the frame window to frame multiple views, usually using a [splitter window](../mfc/multiple-document-types-views-and-frame-windows.md).  In a splitter window, the frame window's client area is occupied by a splitter window, which in turn has multiple child windows, called panes, which are views.  
  
### 추가 정보  
 **General Frame Window Topics**  
  
-   [Window objects](../mfc/window-objects.md)  
  
-   [Frame window classes](../mfc/frame-window-classes.md)  
  
-   [The Frame\-Window classes created by the Application Wizard](../mfc/frame-window-classes-created-by-the-application-wizard.md)  
  
-   [Frame window styles](../mfc/frame-window-styles-cpp.md)  
  
-   [What frame windows do](../mfc/what-frame-windows-do.md)  
  
 **Topics on Using Frame Windows**  
  
-   [Using frame windows](../mfc/using-frame-windows.md)  
  
-   [Creating document frame windows](../mfc/creating-document-frame-windows.md)  
  
-   [Destroying frame windows](../mfc/destroying-frame-windows.md)  
  
-   [Managing MDI child windows](../mfc/managing-mdi-child-windows.md)  
  
-   [Managing the current view](../mfc/managing-the-current-view.md) in a frame window that contains more than one view  
  
-   [Managing menus, control bars, and accelerators \(other objects that share the frame window's space\)](../mfc/managing-menus-control-bars-and-accelerators.md)  
  
 **Topics on Special Frame Window Capabilities**  
  
-   [Dragging and dropping files](../mfc/dragging-and-dropping-files-in-a-frame-window.md) from File Explorer or File Manager into a frame window  
  
-   [Responding to dynamic data exchange \(DDE\)](../mfc/responding-to-dynamic-data-exchange-dde.md)  
  
-   [Semimodal states: Context\-sensitive Windows Help \(Orchestrating other window actions\)](../mfc/orchestrating-other-window-actions.md)  
  
-   [Semimodal states: printing and print preview \(Orchestrating other window actions\)](../mfc/orchestrating-other-window-actions.md)  
  
 **Topics on Other Kinds of Windows**  
  
-   [Using Views](../mfc/using-views.md)  
  
-   [대화 상자](../mfc/dialog-boxes.md)  
  
-   [컨트롤](../mfc/controls-mfc.md)  
  
## 참고 항목  
 [Windows](../mfc/windows.md)