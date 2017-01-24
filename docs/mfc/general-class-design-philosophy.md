---
title: "일반 클래스 디자인 원칙 | Microsoft Docs"
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
  - "vc.classes.mfc"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "클래스[C++], MFC 클래스 디자인"
  - "클래스 디자인"
  - "MFC[C++], Windows API"
  - "Visual C, Windows API 호출"
  - "Windows API[C++], 및 MFC"
ms.assetid: e6861ae0-1581-4d9c-9ddf-63f9afcdb913
caps.latest.revision: 9
caps.handback.revision: 5
author: "mikeblome"
ms.author: "mblome"
manager: "ghogen"
---
# 일반 클래스 디자인 원칙
[!INCLUDE[vs2017banner](../assembler/inline/includes/vs2017banner.md)]

Microsoft Windows was designed long before the C\+\+ language became popular.  Because thousands of applications use the C\-language Windows application programming interface \(API\), that interface will be maintained for the foreseeable future.  Any C\+\+ Windows interface must therefore be built on top of the procedural C\-language API.  This guarantees that C\+\+ applications will be able to coexist with C applications.  
  
 The Microsoft Foundation Class Library is an object\-oriented interface to Windows that meets the following design goals:  
  
-   Significant reduction in the effort to write an application for Windows.  
  
-   Execution speed comparable to that of the C\-language API.  
  
-   Minimum code size overhead.  
  
-   Ability to call any Windows C function directly.  
  
-   Easier conversion of existing C applications to C\+\+.  
  
-   Ability to leverage from the existing base of C\-language Windows programming experience.  
  
-   Easier use of the Windows API with C\+\+ than with C.  
  
-   Easier to use yet powerful abstractions of complicated features such as ActiveX controls, database support, printing, toolbars, and status bars.  
  
-   True Windows API for C\+\+ that effectively uses C\+\+ language features.  
  
 For more on the design of the MFC Library, see:  
  
-   [The Application Framework](../mfc/application-framework.md)  
  
-   [Relationship to the C\-Language API](../mfc/relationship-to-the-c-language-api.md)  
  
## 참고 항목  
 [클래스 개요](../mfc/class-library-overview.md)