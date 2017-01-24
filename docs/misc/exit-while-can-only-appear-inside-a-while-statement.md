---
title: "&#39;Exit While&#39;은 &#39;While&#39; 문 내부에만 사용할 수 있습니다. | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30097"
  - "bc30097"
helpviewer_keywords: 
  - "BC30097"
ms.assetid: cf0a3e09-5252-4198-bb27-c103c98d9f19
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Exit While&#39;은 &#39;While&#39; 문 내부에만 사용할 수 있습니다.
`Exit While` 문이 `While` 블록 외부에서 발생합니다.`Exit While`는 `While` 문과 해당 `End While` 문 사이에만 사용할 수 있습니다.  
  
 **오류 ID:** BC30097  
  
### 이 오류를 해결하려면  
  
1.  유효한 `While` 문이 `Exit While` 앞에 있고 유효한 `End While` 문이 그 뒤에 있는지 확인합니다.  
  
2.  `While` 블록 내의 다른 컨트롤 구조체가 올바르게 종료되었는지 확인합니다.  
  
## 참고 항목  
 [While...End While Statement](../Topic/While...End%20While%20Statement%20\(Visual%20Basic\).md)