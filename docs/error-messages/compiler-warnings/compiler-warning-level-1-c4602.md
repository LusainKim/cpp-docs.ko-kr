---
title: "컴파일러 경고(수준 1) C4602 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C4602"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C4602"
ms.assetid: c1f0300f-e2a2-4c9e-a7c3-4c7318d10509
caps.latest.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 8
---
# 컴파일러 경고(수준 1) C4602
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

\#pragma pop\_macro: 'macro name'에 이 식별자에 대한 이전 \#pragma push\_macro가 없습니다.  
  
 특정 매크로 대해 [pop\_macro](../../preprocessor/pop-macro.md)를 사용하는 경우 먼저 해당 매크로 이름을 [push\_macro](../../preprocessor/push-macro.md)에 전달했어야 합니다. 예를 들어 다음 샘플에서는 C4602를 생성합니다.  
  
```  
// C4602.cpp // compile with: /W1 int main() { #pragma pop_macro("x")   // C4602 x is not on the stack }  
```