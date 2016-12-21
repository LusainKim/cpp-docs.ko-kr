---
title: "&#39;Class&#39; 제약 조건과 특정 클래스 형식 제약 조건은 함께 사용할 수 없습니다. | Microsoft Docs"
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
  - "vbc32107"
  - "bc32107"
helpviewer_keywords: 
  - "BC32107"
ms.assetid: 218a7f0c-dd4f-4086-a52c-e8d581377e8b
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;Class&#39; 제약 조건과 특정 클래스 형식 제약 조건은 함께 사용할 수 없습니다.
제약 조건 목록에는 [클래스\(Visual Basic\)](http://msdn.microsoft.com/ko-kr/0777c6e6-46bc-451b-ad70-57b49d4ef4f7) 제약 조건과 정의된 클래스의 이름이 함께 나옵니다.  
  
 제약 조건 목록은 형식 매개 변수에 전달되는 형식 인수에 대해 요구 사항을 적용합니다. 다음 요구 사항을 임의로 조합해서 지정할 수 있습니다.  
  
-   형식 인수는 하나 이상의 인터페이스를 구현해야 합니다.  
  
-   형식 인수는 최대 하나의 클래스에서 상속해야 합니다.  
  
-   형식 인수는 만드는 코드가 액세스할 수 있는, 매개 변수 없는 생성자를 노출해야 합니다\(`New` 제약 조건 포함\).  
  
 제약 조건 목록에 특정 클래스 또는 인터페이스가 없는 경우 다음 중 하나를 지정하여 더 많은 일반 요구 사항을 적용할 수 있습니다.  
  
-   형식 인수는 값 형식이어야 합니다\(`Structure` 제약 조건 포함\).  
  
-   형식 인수는 참조 형식이어야 합니다\(`Class` 제약 조건 포함\).  
  
 동일한 형식 매개 변수에 `Structure`와 `Class`를 둘 다 지정할 수 없으며 두 번 이상 지정할 수도 없습니다.  
  
 **오류 ID:** BC32107  
  
### 이 오류를 해결하려면  
  
-   형식 인수를 참조 형식으로 허용하려면 제약 조건 목록에서 클래스 이름을 제거합니다.  
  
-   형식 인수를 지정된 클래스 이름에서 상속하려는 경우에는 제약 조건 목록에서 `Class` 키워드를 제거합니다.  
  
## 참고 항목  
 [Visual Basic의 제네릭 형식](../Topic/Generic%20Types%20in%20Visual%20Basic%20\(Visual%20Basic\).md)   
 [Value Types and Reference Types](../Topic/Value%20Types%20and%20Reference%20Types.md)