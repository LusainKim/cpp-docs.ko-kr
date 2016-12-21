---
title: "컴파일러 경고 (수준 1) C4551 | Microsoft Docs"
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
  - "C4551"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4551"
ms.assetid: 458b59bd-e2d7-425f-9ba6-268ff200424f
caps.latest.revision: 6
caps.handback.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 경고 (수준 1) C4551
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

함수 호출에 인수 목록이 없습니다.  
  
 함수 호출에는 함수에 매개 변수가 없어도 함수 이름 뒤에 여는 괄호와 닫는 괄호가 있어야 합니다.  
  
 다음 샘플에서는 C4551 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C4551.cpp  
// compile with: /W1  
void function1() {  
}  
  
int main() {  
   function1;   // C4551  
   function1();   // OK  
}  
```