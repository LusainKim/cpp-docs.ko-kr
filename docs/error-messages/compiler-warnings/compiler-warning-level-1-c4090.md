---
title: "컴파일러 경고 (수준 1) C4090 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4090
dev_langs: C++
helpviewer_keywords: C4090
ms.assetid: baad469d-23d4-45aa-ad9c-305b32d61e9a
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 81506e59243cd8ec17087af6a06391ff097ab05d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4090"></a>컴파일러 경고 (수준 1) C4090
'operation': 다른 'modifier' 한정자  
  
 작업에서 사용 되는 변수 몰래 컴파일러에 의해 수정 되지 않도록 하는 지정 된 한정자로 정의 됩니다. 식은 수정 없이 컴파일됩니다.  
  
 경우에 대 한 포인터가이 경고를 발생할 수 있습니다는 **const** 또는 `volatile` 항목이를 가리키도록 선언 되지 않은 포인터에 할당 된 **const** 또는 `volatile`합니다.  
  
 이 경고는 C 프로그램에 대해 발생 합니다. C + + 프로그램에서 컴파일러는 오류 발생: [C2440](../../error-messages/compiler-errors-1/compiler-error-c2440.md)합니다.  
  
 다음 샘플에서는 C4090 오류가 생성 됩니다.  
  
```  
// C4090.c  
// compile with: /W1  
int *volatile *p;  
int *const *q;  
int **r;  
  
int main() {  
   p = q;   // C4090  
   p = r;  
   q = p;   // C4090  
   q = r;  
   r = p;   // C4090  
   r = q;   // C4090  
}  
```