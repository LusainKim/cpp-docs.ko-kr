---
title: "컴파일러 오류 C3248 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3248"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3248"
ms.assetid: d00b9d7d-b6be-4a5b-bb52-48174ea71fc4
caps.latest.revision: 12
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 12
---
# 컴파일러 오류 C3248
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'function1' : '\_\_sealed'로 선언된 함수를 'function2'로 재정의할 수 없습니다.  
  
 파생 클래스에서 [\_\_sealed](../../misc/sealed.md) 가상 메서드를 재정의하려고 했습니다.  
  
 C3248은 **\/clr:oldSyntax**를 사용하는 경우에만 발생합니다.  
  
 다음 샘플에서는 C3248을 생성합니다.  
  
```  
// C3248b.cpp // compile with: /clr:oldSyntax using namespace System; __gc struct B { __sealed virtual void func(); }; __gc struct D : B { void func();   // C3248 };  
```