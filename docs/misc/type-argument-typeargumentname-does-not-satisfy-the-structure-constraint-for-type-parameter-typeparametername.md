---
title: "형식 인수 &#39;&lt;typeargumentname&gt;&#39;은 형식 매개 변수 &#39;&lt;typeparametername&gt;&#39;에 대한 &#39;Structure&#39; 제약 조건을 만족하지 않습니다. | Microsoft Docs"
ms.custom: ""
ms.date: "12/09/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc32105"
  - "bc32105"
helpviewer_keywords: 
  - "BC32105"
ms.assetid: 09e5a837-8afd-4360-86bd-157e53c47513
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 형식 인수 &#39;&lt;typeargumentname&gt;&#39;은 형식 매개 변수 &#39;&lt;typeparametername&gt;&#39;에 대한 &#39;Structure&#39; 제약 조건을 만족하지 않습니다.
제네릭 형식에 제공되는 형식 인수가 해당 형식 매개 변수에서 값 형식 제약 조건을 충족하지 않습니다.  
  
 제약 조건 목록은 형식 매개 변수에 전달되는 형식 인수에 대해 요구 사항을 적용합니다. 제약 조건 목록에 특정 클래스나 인터페이스를 포함하지 않는 경우 다음 중 하나를 지정하여 일반 요구 사항을 적용할 수 있습니다.  
  
-   형식 인수는 값 형식\([구조체\(Visual Basic\)](http://msdn.microsoft.com/ko-kr/263ce115-ac36-4c05-8cb7-0e0eead5c6d0) 제약 조건 포함\)이어야 합니다.  
  
-   형식 인수는 참조 형식\([클래스\(Visual Basic\)](http://msdn.microsoft.com/ko-kr/0777c6e6-46bc-451b-ad70-57b49d4ef4f7) 제약 조건 포함\)이어야 합니다.  
  
 동일한 형식 매개 변수에 `Structure`와 `Class`를 둘 다 지정할 수 없으며 두 번 이상 지정할 수도 없습니다.  
  
 **오류 ID:** BC32105  
  
### 이 오류를 해결하려면  
  
-   값 형식의 형식 인수를 선택합니다.  
  
## 참고 항목  
 [Visual Basic의 제네릭 형식](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)   
 [방법: 제네릭 클래스 사용](../Topic/How%20to:%20Use%20a%20Generic%20Class%20\(Visual%20Basic\).md)