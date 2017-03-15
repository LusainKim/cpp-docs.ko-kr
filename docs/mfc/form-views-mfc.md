---
title: "폼 뷰(MFC) | Microsoft Docs"
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
  - "응용 프로그램[MFC], 폼 기반"
  - "폼[C++]"
  - "폼[C++], 응용 프로그램에 추가"
  - "폼 기반 응용 프로그램"
  - "사용자 인터페이스, 폼"
ms.assetid: efbe73c1-4ca4-4613-aac2-30d916e92c0e
caps.latest.revision: 11
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
caps.handback.revision: 7
---
# 폼 뷰(MFC)
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

You can add forms to any Visual C\+\+ application that supports the MFC libraries, including a [forms\-based application](../mfc/reference/creating-a-forms-based-mfc-application.md) \(one whose view class is derived from `CFormView`\).  If you did not initially create your application to support forms, Visual C\+\+ will add this support for you when you insert a new form.  In an SDI or MDI application, which implements the default [document\/view architecture](../mfc/document-view-architecture.md), when the user chooses the `New` command \(by default, on the **File** menu\), Visual C\+\+ prompts the user to choose from the available forms.  
  
 With an SDI application, when the user chooses the `New` command, the current instance of the form continues to run but a new instance of the application with the selected form is created if one is not found.  In an MDI application, the current instance of the form continues to run when the user chooses the `New` command.  
  
> [!NOTE]
>  You can insert a form into a dialog\-based application \(one whose dialog class is based on `CDialog` and one in which no view class is implemented\).  However, without the document\/view architecture, Visual C\+\+ does not automatically implement the **File** &#124;**New** functionality.  You must create a way for the user to view additional forms, such as by implementing a tabbed dialog box with various property pages.  
  
 When you insert a new form into your application, Visual C\+\+ does the following:  
  
-   Creates a class based on one of the form\-style classes that you choose \(`CFormView`, `CRecordView`, `CDaoRecordView`, or `CDialog`\).  
  
-   Creates a dialog resource with appropriate styles \(or you can use an existing dialog resource that has not yet been associated with a class\).  
  
     If you choose an existing dialog resource, you may need to set these styles by using the Properties page for the dialog box.  Styles for a dialog box must include:  
  
     **WS\_CHILD**\=On  
  
     `WS_BORDER`\=Off  
  
     **WS\_VISIBLE**\=Off  
  
     **WS\_CAPTION\=**Off  
  
 For applications based on the document\/view architecture, the **New Form** command \(right\-click in Class View\) also:  
  
-   Creates a **CDocument**\-based class  
  
     Instead of having a new class created, you can use any existing **CDocument**\-based class in your project.  
  
-   Generates a document template \(derived from **CDocument**\) with string, menu, and icon resources.  
  
     You can also create a new class on which to base the template.  
  
-   Adds a call to **AddDocumentTemplate** in your application's `InitInstance` code.  
  
     Visual C\+\+ adds this code for each new form you create, which adds the form to the list of available forms when the user chooses the `New` command.  This code includes the form's associated resource ID and the names of the associated document, view, and frame classes that together make up the new form object.  
  
     Document templates serve as the connection between documents, frame windows, and views.  For a single document, you can create many templates.  
  
 자세한 내용은 다음을 참조하십시오.  
  
-   [Create a Forms\-Based Application](../mfc/reference/creating-a-forms-based-mfc-application.md)  
  
-   [Inserting a Form into a Project](../mfc/inserting-a-form-into-a-project.md)  
  
## 참고 항목  
 [사용자 인터페이스 요소](../mfc/user-interface-elements-mfc.md)