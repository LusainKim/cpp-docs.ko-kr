---
title: "컴파일러 오류 C2298 | Microsoft Docs"
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
  - "C2298"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2298"
ms.assetid: eb0120ad-c850-4bdd-911d-0361229cc859
caps.latest.revision: 10
caps.handback.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C2298
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'operation' : 멤버 함수 식에 대한 포인터의 연산이 잘못되었습니다.  
  
 멤버 함수 식에 대한 포인터가 멤버 함수를 호출해야 합니다.  
  
## 예제  
 다음 샘플에서는 C2298 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2298.cpp  
#include <stdio.h>  
  
struct X {  
   void mf() {  
      puts("in X::mf");  
   }  
  
   void mf2() {  
      puts("in X::mf2");  
   }  
};  
  
X x;  
// pointer to member functions with no params and void return in X  
typedef void (X::*pmf_t)();   
  
// a pointer to member function X::mf  
void (X::*pmf)() = &X::mf;  
  
int main() {  
   int (*pf)();  
   pf = x.*pmf;   // C2298  
   +(x.*pmf);     // C2298  
  
   pmf_t pf2 = &X::mf2;  
   (x.*pf2)();   // uses X::mf2  
   (x.*pmf)();   // uses X::mf  
}  
```  
  
## 예제  
 다음 샘플에서는 C2298 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2298_b.cpp  
// compile with: /c  
void F() {}  
  
class Measure {  
public:  
   void SetTrackingFunction(void (Measure::*fnc)()) {  
      TrackingFunction = this->*fnc;   // C2298  
      TrackingFunction = fnc;   // OK  
      GlobalTracker = F;   // OK  
   }  
private:  
   void (Measure::*TrackingFunction)(void);  
   void (*GlobalTracker)(void);  
};  
```