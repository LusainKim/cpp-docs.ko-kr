---
title: "컴파일러 오류 C3120 | Microsoft Docs"
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
  - "C3120"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3120"
ms.assetid: 9b6b210f-9948-4517-a4cc-b4aaadebde68
caps.latest.revision: 5
caps.handback.revision: 5
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C3120
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'method\_name': 인터페이스 메서드는 가변 인수 목록을 사용할 수 없습니다.  
  
 인터페이스 메서드는 가변 인수 목록을 사용할 수 없습니다.  예를 들어, 다음 인터페이스 정의에서는 C3120 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C3120.cpp  
__interface A {  
int X(int i, ...);    // C3120  
};  
  
int main(void) { return(0); }  
```