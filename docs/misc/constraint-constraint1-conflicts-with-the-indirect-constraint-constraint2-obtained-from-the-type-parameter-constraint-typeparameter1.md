---
title: "형식 매개 변수 제약 조건 &#39;&lt;typeparameter1&gt;&#39;에서 가져온 간접 제약 조건 &lt;constraint2&gt;&#39;가 &#39;&lt;constraint1&gt;&#39; 제약 조건과 충돌합니다. | Microsoft Docs"
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
  - "bc32110"
  - "vbc32110"
helpviewer_keywords: 
  - "BC32110"
ms.assetid: e799214d-23b4-4a3f-b61a-0b9d3387ead3
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 형식 매개 변수 제약 조건 &#39;&lt;typeparameter1&gt;&#39;에서 가져온 간접 제약 조건 &lt;constraint2&gt;&#39;가 &#39;&lt;constraint1&gt;&#39; 제약 조건과 충돌합니다.
제네릭 형식이 직접 및 간접 제약 조건의 조합으로 인해 충돌하는 제약 조건으로 선언되었습니다.  
  
 다음 문은 이 오류를 생성할 수 있습니다.  
  
 `Public Class testClass(Of t1 As {Structure, t2}, t2 As Class)`  
  
 직접 제약 조건 `Structure` 및 간접 제약 조건 `Class`으로 인해 형식 매개 변수 `t1`에 대한 충돌이 발생합니다. 그 이유는 해당 형식 인수가 `Structure` 제약 조건에서는 값 형식이어야 하고 `Class`에서는 참조 형식이어야 하기 때문입니다.  
  
 **오류 ID:** BC32110  
  
### 이 오류를 해결하려면  
  
-   제약 조건의 충돌을 방지하려면 형식 매개 변수 제약 조건을 변경합니다.  
  
## 참고 항목  
 [Visual Basic의 제네릭 형식](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Type List](../Topic/Type%20List%20\(Visual%20Basic\).md)   
 [구조체\(Visual Basic\)](http://msdn.microsoft.com/ko-kr/263ce115-ac36-4c05-8cb7-0e0eead5c6d0)   
 [클래스\(Visual Basic\)](http://msdn.microsoft.com/ko-kr/0777c6e6-46bc-451b-ad70-57b49d4ef4f7)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)