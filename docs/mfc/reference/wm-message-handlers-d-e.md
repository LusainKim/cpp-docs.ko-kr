---
title: "WM_ 메시지 처리기: D - E | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "ON_WM_ERASEBKGND"
  - "ON_WM_DEVICECHANGE"
  - "ON_WM_ENTERIDLE"
  - "ON_WM_DESTROYCLIPBOARD"
  - "ON_WM_DESTROY"
  - "ON_WM_DEADCHAR"
  - "ON_WM_DELETEITEM"
  - "ON_WM_DROPFILES"
  - "ON_WM_DEVMODECHANGE"
  - "ON_WM_ENDSESSION"
  - "ON_WM_ENABLE"
  - "ON_WM_DRAWITEM"
  - "ON_WM_DRAWCLIPBOARD"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ON_WM_DEADCHAR"
  - "ON_WM_DELETEITEM"
  - "ON_WM_DESTROY"
  - "ON_WM_DESTROYCLIPBOARD"
  - "ON_WM_DEVICECHANGE"
  - "ON_WM_DEVMODECHANGE"
  - "ON_WM_DRAWCLIPBOARD"
  - "ON_WM_DRAWITEM"
  - "ON_WM_DROPFILES"
  - "ON_WM_ENABLE"
  - "ON_WM_ENDSESSION"
  - "ON_WM_ENTERIDLE"
  - "ON_WM_ERASEBKGND"
  - "WM_ 메시지"
ms.assetid: 56fb89c8-68a8-4adf-883e-a9f63bf677e9
caps.latest.revision: 16
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 17
---
# WM_ 메시지 처리기: D - E
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

The following map entries on the left correspond to the function prototypes on the right:  
  
|Map entry|함수 프로토타입|  
|---------------|--------------|  
|ON\_WM\_DEADCHAR\(\)|afx\_msg void [OnDeadChar](../Topic/CWnd::OnDeadChar.md)\(UINT, UINT, UINT\);|  
|ON\_WM\_DELETEITEM\(\)|afx\_msg void [OnDeleteItem](../Topic/CWnd::OnDeleteItem.md)\(LPDELETEITEMSTRUCT\);|  
|ON\_WM\_DESTROY\(\)|afx\_msg void [OnDestroy](../Topic/CWnd::OnDestroy.md)\(\);|  
|ON\_WM\_DESTROYCLIPBOARD\(\)|afx\_msg void [OnDestroyClipboard](../Topic/CWnd::OnDestroyClipboard.md)\(\);|  
|ON\_WM\_DEVICECHANGE\(\)|afx\_msg void [OnDeviceChange](../Topic/CWnd::OnDeviceChange.md)\(UINT, DWORD\);|  
|ON\_WM\_DEVMODECHANGE\(\)|afx\_msg void [OnDevModeChange](../Topic/CWnd::OnDevModeChange.md)\(LPSTR\);|  
|ON\_WM\_DRAWCLIPBOARD\(\)|afx\_msg void [OnDrawClipboard](../Topic/CWnd::OnDrawClipboard.md)\(\);|  
|ON\_WM\_DRAWITEM\(\)|afx\_msg void [OnDrawItem](../Topic/CWnd::OnDrawItem.md)\(LPDRAWITEMSTRUCT\);|  
|ON\_WM\_DROPFILES\(\)|afx\_msg void [OnDropFiles](../Topic/CWnd::OnDropFiles.md)\(HDROP\);|  
|ON\_WM\_DWMCOLORIZATIONCOLORCHANGED\(\)|afx\_msg void [OnColorizationColorChanged](../Topic/CWnd::OnColorizationColorChanged.md)\(DWORD, BOOL\);|  
|ON\_WM\_DWMCOMPOSITIONCHANGED\(\)|afx\_msg void [OnCompositionChanged](../Topic/CWnd::OnCompositionChanged.md)\(\);|  
|ON\_WM\_DWMNCRENDERINGCHANGED\(\)|afx\_msg void [OnNcRenderingChanged](../Topic/CWnd::OnNcRenderingChanged.md)\(BOOL\);|  
|ON\_WM\_DWMWINDOWMAXIMIZEDCHANGE\(\)|afx\_msg void [OnWindowMaximizedChanged](../Topic/CWnd::OnWindowMaximizedChanged.md)\(BOOL\);|  
|ON\_WM\_ENABLE\(\)|afx\_msg void [OnEnable](../Topic/CWnd::OnEnable.md)\(BOOL\);|  
|ON\_WM\_ENDSESSION\(\)|afx\_msg void [OnEndSession](../Topic/CWnd::OnEndSession.md)\(BOOL\);|  
|ON\_WM\_ENTERIDLE\(\)|afx\_msg void [OnEnterIdle](../Topic/CWnd::OnEnterIdle.md)\(UINT, CWnd\*\);|  
|ON\_WM\_ENTERSIZEMOVE\(\)|afx\_msg void [OnEnterSizeMove](../Topic/CWnd::OnEnterSizeMove.md)\(\);|  
|ON\_WM\_ERASEBKGND\(\)|afx\_msg BOOL [OnEraseBkgnd](../Topic/CWnd::OnEraseBkgnd.md)\(CDC\*\);|  
|ON\_WM\_EXITSIZEMOVE\(\)|afx\_msg void [OnExitSizeMove](../Topic/CWnd::OnExitSizeMove.md)\(\);|  
  
## 참고 항목  
 [메시지 맵](../../mfc/reference/message-maps-mfc.md)   
 [WM\_ 메시지 처리기](../../mfc/reference/handlers-for-wm-messages.md)