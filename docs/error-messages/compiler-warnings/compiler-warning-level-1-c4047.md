---
title: "컴파일러 경고 (수준 1) C4047 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C4047
dev_langs: C++
helpviewer_keywords: C4047
ms.assetid: b75ad6fb-5c93-4434-a85f-c4083051a5de
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 9d42913533129fad2cbdc803e6f3d81bdea3ebd1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-warning-level-1-c4047"></a>컴파일러 경고 (수준 1) C4047
'operator' : 'identifier1'의 간접 참조 수준이 'identifier2'와 다릅니다.  
  
 포인터 변수 (한 수준의 간접 참조), (2 수준의 간접 참조), 변수 및 등을 가리키는 다른 포인터를 가리킬 수 있습니다.  
  
## <a name="example"></a>예  
 다음 샘플에서는 C4047 오류가 생성 됩니다.  
  
```  
// C4047.c  
// compile with: /W1  
  
int main() {  
   char **p = 0;   // two levels of indirection  
   char *q = 0;   // one level of indirection  
  
   char *p2 = 0;   // one level of indirection  
   char *q2 = 0;   // one level of indirection  
  
   p = q;   // C4047  
   p2 = q2;  
}  
```  
  
## <a name="example"></a>예  
 다음 샘플에서는 C4047 오류가 생성 됩니다.  
  
```  
// C4047b.c  
// compile with: /W1  
#include <stdio.h>  
  
int main() {  
   int i;  
   FILE *myFile = NULL;  
   errno_t  err = 0;  
   char file_name[256];  
   char *cs = 0;  
  
   err = fopen_s(&myFile, "C4047.txt", "r");  
   if ((err != 0) || (myFile)) {  
      printf_s("fopen_s failed!\n");  
      exit(-1);  
    }  
   i = fgets(file_name, 256, myFile);   // C4047  
   cs = fgets(file_name, 256, myFile);   // OK  
}  
```