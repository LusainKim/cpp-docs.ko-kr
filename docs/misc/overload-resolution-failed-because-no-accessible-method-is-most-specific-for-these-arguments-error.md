---
title: "다음 인수에만 한정되는 액세스 가능한 &#39;&lt;method&gt;&#39;가 없으므로 오버로드 확인에 실패했습니다. &lt;error&gt; | Microsoft Docs"
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
  - "bc30521"
  - "vbc30521"
helpviewer_keywords: 
  - "확인 실패"
  - "BC30521"
  - "오버로드 확인에 실패했습니다."
ms.assetid: b8b41fa0-a64b-4e74-8443-be3afd2b6f11
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 다음 인수에만 한정되는 액세스 가능한 &#39;&lt;method&gt;&#39;가 없으므로 오버로드 확인에 실패했습니다. &lt;error&gt;
오버로드된 메서드를 호출했지만 컴파일러가 인수 목록이 변환될 수 있는 매개 변수 목록을 사용하여 두 개 이상의 오버로드를 발견했으며 이런 경우 컴파일러가 이들 사이에서 선택할 수 없습니다.  
  
 컴파일러는 호출 인수 목록과 오버로드 매개 변수 목록의 데이터 형식을 최대한 비슷하게 일치시키려고 합니다. 그러려면 형식 검사 스위치\([Option Strict Statement](../Topic/Option%20Strict%20Statement.md)\)가 `On`이든 `Off`이든 상관없이 모든 인수가 해당 매개 변수로 확대 변환되어야 합니다.  
  
 컴파일러가 확대 변환 요구 사항을 충족시키는 둘 이상의 오버로드를 발견하는 경우 인수 데이터 형식과 가장 근접한 오버로드, 즉 확대 변환 부분이 가장 적은 오버로드를 찾습니다. 한 오버로드는 한 인수의 데이터 형식에 더 가깝고 다른 오버로드는 다른 인수의 데이터 형식에 더 가까운 경우 이 오류 메시지가 생성됩니다. 자세한 내용과 예제는 [Overload Resolution](../Topic/Overload%20Resolution%20\(Visual%20Basic\).md)를 참조하세요.  
  
 **오류 ID:** BC30521  
  
### 이 오류를 해결하려면  
  
1.  메서드의 모든 오버로드를 검토하고 호출하려는 오버로드를 결정합니다.  
  
2.  호출 문에서 원하는 오버로드에 대해 정의된 매개 변수의 데이터 형식과 인수의 데이터 형식을 일치시킵니다. 하나 이상의 데이터 형식을 정의된 형식으로 변환하기 위해 [CType 함수](../Topic/CType%20Function%20\(Visual%20Basic\).md)를 사용해야 할 수도 있습니다.  
  
## 참고 항목  
 [Procedure Overloading](../Topic/Procedure%20Overloading%20\(Visual%20Basic\).md)   
 [Considerations in Overloading Procedures](../Topic/Considerations%20in%20Overloading%20Procedures%20\(Visual%20Basic\).md)   
 [Overload Resolution](../Topic/Overload%20Resolution%20\(Visual%20Basic\).md)   
 [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md)   
 [Overloaded Properties and Methods](../Topic/Overloaded%20Properties%20and%20Methods%20\(Visual%20Basic\).md)   
 [Option Strict Statement](../Topic/Option%20Strict%20Statement.md)   
 [CType 함수](../Topic/CType%20Function%20\(Visual%20Basic\).md)