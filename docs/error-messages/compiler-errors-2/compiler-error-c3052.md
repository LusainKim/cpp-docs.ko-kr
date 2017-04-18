---
title: "컴파일러 오류 C3052 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3052
dev_langs:
- C++
helpviewer_keywords:
- C3052
ms.assetid: 87480c42-1ceb-4775-8d20-88c54a7bb6a6
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
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: 65c77919d980d574c0dacb27e9fc33f94d80391f
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3052"></a>컴파일러 오류 C3052
'var': default(none) 절 밑의 데이터 공유 절에 변수가 없습니다.  
  
 경우 [밑](../../parallel/openmp/reference/default-openmp.md) 는 사용 하는 구조화 된 블록에 사용 된 모든 변수가 명시적으로 지정 해야 하거나 [공유](../../parallel/openmp/reference/shared-openmp.md) 또는 [개인](../../parallel/openmp/reference/private-openmp.md)합니다.  
  
 다음 샘플에서는 C3052를 생성합니다.  
  
```  
// C3052.cpp  
// compile with: /openmp /c  
int main() {  
   int n1 = 1;  
  
   #pragma omp parallel default(none) // shared(n1) private(n1)  
   {  
      n1 = 0;   // C3052 use either a shared or private clause  
   }  
}  
```
