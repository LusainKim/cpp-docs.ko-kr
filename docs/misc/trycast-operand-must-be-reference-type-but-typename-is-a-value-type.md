---
title: "&#39;TryCast&#39; 피연산자는 참조 형식이어야 하는데 &#39;&lt;typename&gt;&#39;은 값 형식입니다. | Microsoft Docs"
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
  - "BC30792"
  - "vbc30792"
helpviewer_keywords: 
  - "BC30792"
ms.assetid: 3325fce5-dbc0-4d1d-9530-31f4720bfe6e
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;TryCast&#39; 피연산자는 참조 형식이어야 하는데 &#39;&lt;typename&gt;&#39;은 값 형식입니다.
인수 중 하나 이상에 대해 `TryCast` 연산자가 값 형식과 함께 사용됩니다.  
  
 `TryCast`는 두 인수 간의 상속 또는 구현 관계를 테스트합니다. 따라서 인수에는 참조 형식만 사용할 수 있습니다. 자세한 내용은 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)을 참조하세요.  
  
 **오류 ID:** BC30792  
  
### 이 오류를 해결하려면  
  
-   `DirectCast` 또는 `CType`을 사용하여 변환을 수행합니다. 둘 다 값 형식을 허용합니다.  
  
## 참고 항목  
 [TryCast Operator](../Topic/TryCast%20Operator%20\(Visual%20Basic\).md)   
 [DirectCast Operator](../Topic/DirectCast%20Operator%20\(Visual%20Basic\).md)   
 [CType 함수](../Topic/CType%20Function%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)