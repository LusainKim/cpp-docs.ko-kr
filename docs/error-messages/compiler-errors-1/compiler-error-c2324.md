---
title: "컴파일러 오류 C2324 | Microsoft Docs"
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
  - "C2324"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2324"
ms.assetid: 215f0544-85b0-452d-825f-17a388b6a61c
caps.latest.revision: 10
caps.handback.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C2324
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier' : 'name' 오른쪽에 올 수 없습니다.  
  
 소멸자가 잘못된 식별자를 통해 호출되었습니다.  
  
 다음 샘플에서는 C2324 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2324.cpp  
class A {};  
typedef A* pA_t;  
int i;  
  
int main() {  
   pA_t * ppa = new pA_t;  
   ppa->~i;   // C2324  
   ppa->~pA_t();   // OK  
}  
```