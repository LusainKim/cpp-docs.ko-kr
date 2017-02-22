---
title: "컴파일러 오류 C2365 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2365"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2365"
ms.assetid: 35839b0b-4055-4b79-8957-b3a0871bdd02
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# 컴파일러 오류 C2365
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'class member': 재정의: 이전 정의는 'class member'입니다.  
  
 클래스 멤버를 다시 정의하려고 했습니다.  
  
 다음 샘플에서는 C2365를 생성합니다.  
  
```  
// C2365.cpp // compile with: /c class C1 { int CFunc(); char *CFunc;   // C2365, already exists as a member function int CMem; char *CMem();   // C2365, already exists as a data member };  
```