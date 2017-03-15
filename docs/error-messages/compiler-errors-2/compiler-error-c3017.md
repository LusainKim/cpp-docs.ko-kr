---
title: "컴파일러 오류 C3017 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3017"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3017"
ms.assetid: 12ab2c2a-d0d2-4900-9cbf-39be0af590dd
caps.latest.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 7
---
# 컴파일러 오류 C3017
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

OpenMP 'for' 문의 종료 테스트 형식이 잘못되었습니다.  
  
 OpenMP 문의 `for` 루프를 완벽하고 명시적으로 지정해야 합니다.  
  
 다음 샘플에서는 C3017을 생성합니다.  
  
```  
// C3017.cpp // compile with: /openmp int main() { int i = 0, j = 10; #pragma omp parallel { #pragma omp for for (i = 0; i; ++i)   // C3017 // Try the following line instead: // for (i = 0; i < 10; ++i) ; } }  
```