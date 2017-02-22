---
title: "컴파일러 오류 C2488 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: ""
ms.topic: "error-reference"
f1_keywords: 
  - "C2488"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2488"
ms.assetid: cd435909-43e4-43c6-a57c-5d02468ef75f
caps.latest.revision: 10
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 10
---
# 컴파일러 오류 C2488
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier' : 'naked'는 비멤버 함수 정의에만 적용할 수 있습니다.  
  
 [naked](../../cpp/naked-cpp.md) 특성이 함수 선언에 적용되었습니다.  
  
 다음 샘플에서는 C2488 오류가 발생하는 경우를 보여 줍니다.  
  
```  
// C2488.cpp  
// compile with: /c  
// processor: x86  
__declspec( naked ) void func();   // C2488  declaration, not definition  
__declspec( naked ) void i;   // C2488  i is not a function  
  
__declspec( naked ) void func() {}   // OK  
```