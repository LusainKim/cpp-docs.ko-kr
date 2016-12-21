---
title: "대리자는 인터페이스 메서드를 구현할 수 없습니다. | Microsoft Docs"
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
  - "bc30018"
  - "vbc30018"
helpviewer_keywords: 
  - "BC30018"
ms.assetid: 71851072-c0c7-4131-aaf7-f3e9e6a2a448
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 대리자는 인터페이스 메서드를 구현할 수 없습니다.
대리자는 공유 프로시저 또는 개체의 인스턴스 프로시저를 가리키는 참조 형식입니다. 할당을 통해 가리키는 프로시저를 변경할 수 있으므로 `Delegate` 문은 `Handles` 또는 `Implements` 절을 지원할 수 없습니다.  
  
 **오류 ID:** BC30018  
  
### 이 오류를 해결하려면  
  
-   `Delegate` 문에서 `Implements` 절을 제거합니다.  
  
## 참고 항목  
 [빌드에 없음: 대리자 및 AddressOf 연산자](http://msdn.microsoft.com/ko-kr/7b2ed932-8598-4355-b2f7-5cedb23ee86f)   
 [Delegate Statement](../Topic/Delegate%20Statement.md)   
 [Handles](../Topic/Handles%20Clause%20\(Visual%20Basic\).md)   
 [Implements Statement](../Topic/Implements%20Statement.md)