---
title: "컴파일러 오류 C2400 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2400"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2400"
ms.assetid: 1ba441ee-73f9-42a5-bfe9-fbeab93808eb
caps.latest.revision: 9
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 9
---
# 컴파일러 오류 C2400
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'context'에 인라인 어셈블러 구문 오류가 있습니다. 'token'을\(를\) 찾았습니다.  
  
 토큰으로 인해 지정한 컨텍스트에서 구문 오류가 발생했습니다.  
  
 다음 샘플에서는 C2400 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2400.cpp  
// processor: x86  
int main() {  
   __asm {  
      heh ax,bx;   // C2400, heh is not a valid x86 instruction  
      mov ax,bx;   // OK  
   }  
}  
```