---
title: "심각한 오류 C1310 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1310
dev_langs:
- C++
helpviewer_keywords:
- C1310
ms.assetid: ac48aa51-8023-42fe-b844-3f8bf228fbef
caps.latest.revision: 5
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 05955990b1df5d2e64215a96a5da205d45539bc0
ms.contentlocale: ko-kr
ms.lasthandoff: 10/09/2017

---
# <a name="fatal-error-c1310"></a>심각한 오류 C1310
OpenMP에서는 프로필 기반 최적화를 사용할 수 없습니다.  
  
 [/GL](../../build/reference/ltcg-link-time-code-generation.md) 로 컴파일된 모든 모듈을 [/LTCG:PGI](../../build/reference/gl-whole-program-optimization.md)와 연결할 수 없습니다.  
  
 다음 샘플에서는 C1310을 생성합니다.  
  
```  
// C1310.cpp  
// compile with: /openmp /GL /link /LTCG:PGI  
// C1310 expected  
int main()  
{  
   int i = 0, j = 10;  
  
   #pragma omp parallel  
   {  
      #pragma omp for  
      for (i = 0; i < 0; i++)   
         --j;  
   }  
}  
```
