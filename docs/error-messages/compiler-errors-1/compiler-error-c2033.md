---
title: "컴파일러 오류 C2033 | Microsoft Docs"
ms.custom: ""
ms.date: "12/03/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C2033"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C2033"
ms.assetid: fd5a1637-9db2-4c98-a7cc-b63b39737cd9
caps.latest.revision: 7
caps.handback.revision: 7
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
---
# 컴파일러 오류 C2033
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

'identifier': 비트 필드에 간접 참조를 사용할 수 없습니다.  
  
 비트 필드가 허용되지 않는 포인터로 선언되었습니다.  
  
 다음 샘플에서는 C2033을 생성합니다.  
  
```  
// C2033.cpp struct S { int *b : 1;  // C2033 };  
```  
  
 해결 방법:  
  
```  
// C2033b.cpp // compile with: /c struct S { int b : 1; };  
```