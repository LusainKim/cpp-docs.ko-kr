---
title: "컴파일러 오류 C2118 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2118"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2118"
ms.assetid: bf4315d0-f085-4323-b813-96ee61a13bde
caps.latest.revision: 9
caps.handback.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C2118
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

첨자가 음수입니다.  
  
 배열 크기를 정의하는 값이 최대 배열 크기보다 크거나 0보다 작습니다.  
  
 다음 샘플에서는 C2118 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2118.cpp  
int main() {  
   int array1[-1];   // C2118  
   int array2[3];   // OK  
}  
```