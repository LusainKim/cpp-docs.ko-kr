---
title: "컴파일러 오류 C3243 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3243"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3243"
ms.assetid: 35d8ad1a-377d-47df-be9d-c55eea23340f
caps.latest.revision: 6
caps.handback.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C3243
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

오버로드 함수가 'interface'에 의해 하나도 정의되지 않았습니다.  
  
 지정된 인터페이스에 없는 멤버를 [명시적으로 재정의](../../cpp/explicit-overrides-cpp.md)하려고 했습니다.  
  
 다음 샘플에서는 C3243을 생성합니다.  
  
```  
// C3243.cpp #pragma warning(disable:4199) __interface IX14A { void g(); }; __interface IX14B { void f(); void f(int); }; class CX14 : public IX14A, public IX14B { public: void IX14A::g(); void IX14B::f(); void IX14B::f(int); }; void CX14::IX14A::f()   // C3243 occurs here { }  
```