---
title: "문서 템플릿 및 문서/뷰 만들기 프로세스 | Microsoft Docs"
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
  - "CDocTemplate 클래스"
  - "문서 템플릿, 및 뷰"
  - "문서/뷰 아키텍처, 문서/뷰 만들기"
  - "아이콘, 여러 문서 템플릿을 위한"
  - "MFC, 문서 템플릿"
  - "여러 문서 템플릿"
  - "단일 문서 템플릿"
  - "템플릿, 문서 템플릿"
ms.assetid: 311ce4cd-fbdf-4ea1-a51b-5bb043abbcee
caps.latest.revision: 9
caps.handback.revision: 5
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 문서 템플릿 및 문서/뷰 만들기 프로세스
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

To manage the complex process of creating documents with their associated views and frame windows, the framework uses two document template classes: [CSingleDocTemplate](../mfc/reference/csingledoctemplate-class.md) for SDI applications and [CMultiDocTemplate](../mfc/reference/cmultidoctemplate-class.md) for MDI applications.  A `CSingleDocTemplate` can create and store one document of one type at a time.  A `CMultiDocTemplate` keeps a list of many open documents of one type.  
  
 Some applications support multiple document types.  For example, an application might support text documents and graphics documents.  In such an application, when the user chooses the New command on the File menu, a dialog box shows a list of possible new document types to open.  For each supported document type, the application uses a distinct document template object.  The following figure illustrates the configuration of an MDI application that supports two document types and shows several open documents.  
  
 ![2가지 문서 형식이 포함된 MDI 응용 프로그램](../mfc/media/vc387h1.png "vc387H1")  
두 문서 형식을 사용하는 MDI 응용 프로그램  
  
 Document templates are created and maintained by the application object.  One of the key tasks performed during your application's `InitInstance` function is to construct one or more document templates of the appropriate kind.  This feature is described in [Document Template Creation](../mfc/document-template-creation.md).  The application object stores a pointer to each document template in its template list and provides an interface for adding document templates.  
  
 If you need to support two or more document types, you must add an extra call to [AddDocTemplate](../Topic/CWinApp::AddDocTemplate.md) for each document type.  
  
 An icon is registered for each document template based on its position in the application's list of document templates.  The order of the document templates is determined by the order they are added with calls to `AddDocTemplate`.  MFC assumes that the first Icon resource in the application is the application icon, the next Icon resource is the first document icon, and so on.  
  
 For example, a document template is the third of three for the application.  If there is an Icon resource in the application at index 3, that icon is used for the document template.  If not, the icon at index 0 is used as a default.  
  
## 참고 항목  
 [일반 MFC 항목](../mfc/general-mfc-topics.md)   
 [문서 템플릿 만들기](../mfc/document-template-creation.md)   
 [문서\/뷰 만들기](../mfc/document-view-creation.md)   
 [MFC 개체 간 관계](../mfc/relationships-among-mfc-objects.md)   
 [새 문서, 창 및 뷰 만들기](../mfc/creating-new-documents-windows-and-views.md)