---
title: "컴파일러 경고 (수준 1) C4047 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C4047"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4047"
ms.assetid: b75ad6fb-5c93-4434-a85f-c4083051a5de
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# 컴파일러 경고 (수준 1) C4047
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'operator' : 'identifier1'의 간접 참조 수준이 'identifier2'과\(와\) 다릅니다.  
  
 포인터는 변수\(1 수준의 간접 참조\), 변수를 가리키는 별개의 포인터\(2 수준의 간접 참조\) 등을 가리킬 수 있습니다.  
  
## 예제  
 다음 샘플에서는 C4047 오류가 발생하는 경우를 보여 줍니다.  
  
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
  
## 예제  
 다음 샘플에서는 C4047 오류가 발생하는 경우를 보여 줍니다.  
  
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