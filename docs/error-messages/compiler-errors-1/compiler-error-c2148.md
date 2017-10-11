---
title: "컴파일러 오류 C2148 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2148
dev_langs:
- C++
helpviewer_keywords:
- C2148
ms.assetid: e510c2c9-7b57-4ce8-be03-ba363e2cc5d9
caps.latest.revision: 12
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 2d98197ed8043af05fd27239ca10aa3a0d06e3c0
ms.contentlocale: ko-kr
ms.lasthandoff: 10/09/2017

---
# <a name="compiler-error-c2148"></a>컴파일러 오류 C2148
0x7fffffff 바이트 배열의 전체 크기를 초과할 수 없습니다.  
  
 배열에는 제한을 초과합니다. 배열의 크기를 줄입니다.  
  
## <a name="example"></a>예제  
 다음 샘플에서는 C2148 오류가 생성 됩니다.  
  
```  
// C2148.cpp  
#include <stdio.h>  
#include <stdlib.h>  
  
int main( ) {  
   char MyArray[0x7ffffffff];   // C2148  
   char * MyArray2 = (char *)malloc(0x7fffffff);  
  
   if (MyArray2)  
      printf_s("It worked!");  
   else  
      printf_s("It didn't work.");  
}  
```
