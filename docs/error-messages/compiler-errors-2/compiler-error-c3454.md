---
title: "컴파일러 오류 C3454 | Microsoft Docs"
ms.custom: ""
ms.date: "11/04/2016"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "C3454"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "C3454"
ms.assetid: dc4e6d57-5b4d-4114-8d6f-22f9ae62925b
caps.latest.revision: 6
author: "corob-msft"
ms.author: "corob"
manager: "ghogen"
caps.handback.revision: 6
---
# 컴파일러 오류 C3454
[!INCLUDE[vs2017banner](../../assembler/inline/includes/vs2017banner.md)]

\[attribute\]는 클래스 선언에 사용할 수 없습니다.  
  
 클래스는 특성이 되도록 정의되어야 합니다.  
  
 자세한 내용은 [attribute](../../windows/attribute.md)을 참조하세요.  
  
## 예제  
 다음 샘플에서는 C3454를 생성합니다.  
  
```  
// C3454.cpp // compile with: /clr /c using namespace System; [attribute]   // C3454 ref class Attr1; [attribute]   // OK ref class Attr2 {};  
```