---
title: "컴파일러 오류 C3049 | Microsoft Docs"
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
  - "C3049"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3049"
ms.assetid: 6ddf54f6-2c30-4d04-b637-98c6c922c533
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C3049
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'arg': OpenMP 'default' 절의 인수가 잘못되었습니다.  
  
 잘못된 값이 [default](../../parallel/openmp/reference/default-openmp.md) 절에 전달되었습니다.  
  
 다음 샘플에서는 C3049를 생성합니다.  
  
```  
// C3049.cpp // compile with: /openmp /c int main() { int n1 = 1; #pragma omp parallel default(private)   // C3049 // try the following line instead // #pragma omp parallel default(shared) { ++n1; } }  
```