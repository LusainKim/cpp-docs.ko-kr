---
title: "컴파일러 오류 C3017 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3017
dev_langs:
- C++
helpviewer_keywords:
- C3017
ms.assetid: 12ab2c2a-d0d2-4900-9cbf-39be0af590dd
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 6a053011e948efed2f14a102a9d3f250d87384bd
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3017"></a>컴파일러 오류 C3017
OpenMP 'for' 문의 종료 테스트 형식이 잘못되었습니다.  
  
 OpenMP 문의 `for` 루프를 완벽하고 명시적으로 지정해야 합니다.  
  
 다음 샘플에서는 C3017을 생성합니다.  
  
```  
// C3017.cpp  
// compile with: /openmp  
int main()  
{  
   int i = 0, j = 10;  
  
   #pragma omp parallel  
   {  
      #pragma omp for  
      for (i = 0; i; ++i)   // C3017  
      // Try the following line instead:  
      // for (i = 0; i < 10; ++i)  
         ;  
   }  
}  
```
