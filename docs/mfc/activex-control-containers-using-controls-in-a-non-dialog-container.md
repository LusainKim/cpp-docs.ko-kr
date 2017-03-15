---
title: "ActiveX 컨트롤 컨테이너: 대화 상자가 아닌 컨테이너에서 컨트롤 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "article"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "ActiveX 컨트롤 컨테이너[C++], 컨트롤 삽입"
  - "ActiveX 컨트롤 컨테이너[C++], 대화 상자가 아닌 컨테이너"
  - "ActiveX 컨트롤[C++], 만들기"
  - "Create 메서드[C++], ActiveX 컨트롤"
  - "CreateControl 메서드"
ms.assetid: 46f195b0-b8ca-4409-8cca-fbfaf2c9ab9f
caps.latest.revision: 10
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 6
---
# ActiveX 컨트롤 컨테이너: 대화 상자가 아닌 컨테이너에서 컨트롤 사용
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

In some applications, such as an SDI or MDI application, you will want to embed a control in a window of the application.  The **Create** member function of the wrapper class, inserted by Visual C\+\+, can create an instance of the control dynamically, without the need for a dialog box.  
  
 The **Create** member function has the following parameters:  
  
 `lpszWindowName`  
 A pointer to the text to be displayed in the control's Text or Caption property \(if any\).  
  
 `dwStyle`  
 Windows styles.  For a complete list, see [CWnd::CreateControl](../Topic/CWnd::CreateControl.md).  
  
 `rect`  
 Specifies the control's size and position.  
  
 `pParentWnd`  
 Specifies the control's parent window, usually a `CDialog`.  It must not be **NULL**.  
  
 `nID`  
 Specifies the control ID and can be used by the container to refer to the control.  
  
 One example of using this function to dynamically create an ActiveX control would be in a form view of an SDI application.  You could then create an instance of the control in the `WM_CREATE` handler of the application.  
  
 For this example, `CMyView` is the main view class, `CCirc` is the wrapper class, and CIRC.H is the header \(.H\) file of the wrapper class.  
  
 Implementing this feature is a four\-step process.  
  
### To dynamically create an ActiveX control in a non\-dialog window  
  
1.  Insert CIRC.H in CMYVIEW.H, just before the `CMyView` class definition:  
  
     [!code-cpp[NVC_MFC_AxCont#12](../mfc/codesnippet/CPP/activex-control-containers-using-controls-in-a-non-dialog-container_1.h)]  
  
2.  Add a member variable \(of type `CCirc`\) to the protected section of the `CMyView` class definition located in CMYVIEW.H:  
  
     [!code-cpp[NVC_MFC_AxCont#13](../mfc/codesnippet/CPP/activex-control-containers-using-controls-in-a-non-dialog-container_2.h)]  
    [!code-cpp[NVC_MFC_AxCont#14](../mfc/codesnippet/CPP/activex-control-containers-using-controls-in-a-non-dialog-container_3.h)]  
  
3.  Add a `WM_CREATE` message handler to class `CMyView`.  
  
4.  In the handler function, `CMyView::OnCreate`, make a call to the control's `Create` function using the **this** pointer as the parent window:  
  
     [!code-cpp[NVC_MFC_AxCont#15](../mfc/codesnippet/CPP/activex-control-containers-using-controls-in-a-non-dialog-container_4.cpp)]  
  
5.  프로젝트를 다시 빌드합니다.  A Circ control will be created dynamically whenever the application's view is created.  
  
## 참고 항목  
 [ActiveX 컨트롤 컨테이너](../mfc/activex-control-containers.md)