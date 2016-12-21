---
title: "무명 형식 멤버 또는 속성 &#39;&lt;propertyname&gt;&#39;이 이미 선언되어 있습니다. | Microsoft Docs"
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
  - "bc36547"
  - "vbc36547"
helpviewer_keywords: 
  - "BC36547"
ms.assetid: 4c60d24a-62d7-404a-bc35-d1a1d9c9f851
caps.latest.revision: 7
caps.handback.revision: 7
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 무명 형식 멤버 또는 속성 &#39;&lt;propertyname&gt;&#39;이 이미 선언되어 있습니다.
속성 이름은 무명 형식 선언에서 한 번만 설정할 수 있습니다. 예를 들어 다음 선언은 잘못된 것입니다.  
  
```vb#  
'' Not valid, because the Label property is assigned to twice.  
' Dim anonType1 = New With {.Label = "Debra Garcia", .Label = .Label & ", President"}  
'' Not valid, because the property name inferred for both properties is  
'' Name.  
' Dim anonType2 = New With {Key product.Name, Key car1.Name}  
```  
  
 **오류 ID:** BC36547  
  
### 이 오류를 해결하려면  
  
-   속성 중 하나에 다른 이름을 선택합니다.  
  
    ```vb#  
    ' Valid.  
    Dim anonType3 = New With {.Name = "Debra Garcia", .Label = .Name & ", President"}  
    ```  
  
-   이름과 값을 유추하는 변수 또는 속성 이름에 대해 새 이름을 제공합니다.  
  
    ```vb#  
    ' Valid.  
    Dim anonType4 = New With {Key .ProductName = product.Name, Key .CarName = car1.Name}  
  
    ```  
  
## 참고 항목  
 [Anonymous Types](../Topic/Anonymous%20Types%20\(Visual%20Basic\).md)   
 [방법: 익명 형식 선언에서 속성 이름 및 형식 유추](../Topic/How%20to:%20Infer%20Property%20Names%20and%20Types%20in%20Anonymous%20Type%20Declarations%20\(Visual%20Basic\).md)