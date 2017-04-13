---
title: "컴파일러 오류 C3002 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3002
dev_langs:
- C++
helpviewer_keywords:
- C3002
ms.assetid: 2d4241a7-c8eb-4d43-a128-dca255d137bc
caps.latest.revision: 6
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
ms.openlocfilehash: 841492014aaf99d63278a372f4cd03980700c4b8
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3002"></a>컴파일러 오류 C3002
'name1 name2': OpenMP 지시문 이름이 여러 개 있습니다.  
  
 여러 지시문 이름은 허용되지 않습니다.  
  
 다음 샘플에서는 C3002를 생성합니다.  
  
```  
// C3002.c  
// compile with: /openmp  
int main()  
{  
   #pragma omp parallel single   // C3002  
}  
```
