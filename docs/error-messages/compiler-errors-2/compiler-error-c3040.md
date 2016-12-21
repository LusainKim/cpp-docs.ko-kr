---
title: "컴파일러 오류 C3040 | Microsoft Docs"
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
  - "C3040"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3040"
ms.assetid: 29e857ac-74f0-4ec6-becf-9026e38c160e
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C3040
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'var': 'reduction' 절의 변수 형식이 환산 연산자 'operator'와 호환되지 않습니다.  
  
 [reduction](../../parallel/openmp/reference/reduction.md) 절의 변수를 reduction 연산자와 함께 사용할 수 없습니다.  
  
 다음 샘플에서는 C3040을 생성합니다.  
  
```  
// C3040.cpp // compile with: /openmp /c #include "omp.h" double d; int main() { #pragma omp parallel reduction(&:d)   // C3040 ; #pragma omp parallel reduction(-:d)  // OK ; }  
```