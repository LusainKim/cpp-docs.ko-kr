---
title: "연산자를 &#39;Shared&#39;로 선언해야 합니다. | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc33012"
  - "bc33012"
helpviewer_keywords: 
  - "BC33012"
ms.assetid: 5ad97616-4032-46cd-aaf7-517db5d1195f
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 연산자를 &#39;Shared&#39;로 선언해야 합니다.
[Operator Statement](../Topic/Operator%20Statement.md)에 [Shared](../Topic/Shared%20\(Visual%20Basic\).md) 키워드가 없습니다.  
  
 `Operator` 프로시저에는 [Public](../Topic/Public%20\(Visual%20Basic\).md) 및 `Shared` 키워드가 둘 다 필요하며, 변환 연산자에도 [Widening](../Topic/Widening%20\(Visual%20Basic\).md) 또는 [Narrowing](../Topic/Narrowing%20\(Visual%20Basic\).md) 키워드가 필요합니다.  
  
 **오류 ID:** BC33012  
  
### 이 오류를 해결하려면  
  
-   `Operator` 문에 `Shared` 키워드를 추가합니다.  
  
## 참고 항목  
 [Operator Procedures](../Topic/Operator%20Procedures%20\(Visual%20Basic\).md)   
 [Operator Statement](../Topic/Operator%20Statement.md)   
 [How to: Define an Operator](../Topic/How%20to:%20Define%20an%20Operator%20\(Visual%20Basic\).md)   
 [How to: Define a Conversion Operator](../Topic/How%20to:%20Define%20a%20Conversion%20Operator%20\(Visual%20Basic\).md)