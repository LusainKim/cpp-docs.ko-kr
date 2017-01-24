---
title: "&#39;&lt;classname&gt;&#39; 클래스의 기본 클래스 &#39;&lt;classname2&gt;&#39;에는 인수 없이 호출할 수 있는 액세스 가능한 &#39;Sub New&#39;가 두 개 이상 있으므로 &#39;Sub New&#39;를 선언해야 합니다. | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-visual-basic"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vbc30387"
  - "bc30387"
helpviewer_keywords: 
  - "BC30387"
ms.assetid: ff587e79-fa47-4b55-9a08-24688b209e0a
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;classname&gt;&#39; 클래스의 기본 클래스 &#39;&lt;classname2&gt;&#39;에는 인수 없이 호출할 수 있는 액세스 가능한 &#39;Sub New&#39;가 두 개 이상 있으므로 &#39;Sub New&#39;를 선언해야 합니다.
호출할 수 있는 기본 클래스 생성자가 없으므로 파생 클래스가 생성자를 선언하지 않으며 [!INCLUDE[vbprvb](../Token/vbprvb_md.md)]가 생성자를 생성할 수 없습니다.  
  
 파생 클래스가 생성자를 선언하지 않는 경우 [!INCLUDE[vbprvb](../Token/vbprvb_md.md)]가 `MyBase.New()`를 호출하는 매개 변수가 없는 암시적 생성자를 생성하려고 합니다. 인수 없이 호출될 수 있는 기본 클래스에 액세스할 수 있는 생성자가 없거나 둘 이상 있는 경우 [!INCLUDE[vbprvb](../Token/vbprvb_md.md)]은 암시적 생성자를 생성할 수 없습니다.  
  
 **오류 ID:** BC30387  
  
### 이 오류를 해결하려면  
  
1.  파생 클래스의 임의 위치에서 하나 이상의 `Sub New` 생성자를 선언하여 구현합니다.  
  
2.  기본 클래스 생성자 `MyBase.New()`에 모든 `Sub New`의 첫 번째 줄로 호출을 추가합니다.  
  
## 참고 항목  
 [Object Lifetime: How Objects Are Created and Destroyed](../Topic/Object%20Lifetime:%20How%20Objects%20Are%20Created%20and%20Destroyed%20\(Visual%20Basic\).md)   
 [빌드에 없음: 생성자 및 소멸자 사용](http://msdn.microsoft.com/ko-kr/548eebe1-86c4-4377-b2f5-447cb8be3d90)   
 [Optional](../Topic/Optional%20\(Visual%20Basic\).md)   
 [ParamArray](../Topic/ParamArray%20\(Visual%20Basic\).md)   
 [Optional Parameters](../Topic/Optional%20Parameters%20\(Visual%20Basic\).md)   
 [Parameter Arrays](../Topic/Parameter%20Arrays%20\(Visual%20Basic\).md)