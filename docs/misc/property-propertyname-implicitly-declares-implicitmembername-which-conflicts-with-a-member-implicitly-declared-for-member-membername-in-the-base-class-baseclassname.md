---
title: "&#39;&lt;propertyname&gt;&#39; 속성이 &#39;&lt;baseclassname&gt;&#39; 기본 클래스에서 &#39;&lt;membername&gt;&#39; 멤버에 대해 암시적으로 선언된 멤버와 충돌하는 &#39;&lt;implicitmembername&gt;&#39;을 암시적으로 선언합니다. | Microsoft Docs"
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
  - "vbc40024"
  - "bc40024"
helpviewer_keywords: 
  - "BC40024"
ms.assetid: fab4f290-a41f-47d6-9bdb-44eb8dd395d5
caps.latest.revision: 14
caps.handback.revision: 14
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;propertyname&gt;&#39; 속성이 &#39;&lt;baseclassname&gt;&#39; 기본 클래스에서 &#39;&lt;membername&gt;&#39; 멤버에 대해 암시적으로 선언된 멤버와 충돌하는 &#39;&lt;implicitmembername&gt;&#39;을 암시적으로 선언합니다.
'\<membername1\>' 멤버가 '\<baseclassname\>' 기본 클래스에서 '\<membername2\>' 멤버에 대해 암시적으로 선언된 멤버와 충돌하는 '\<implicitmembername\>'을 암시적으로 선언합니다. 따라서 멤버를 'Overloads'로 선언할 수 없습니다.  
  
 파생 클래스의 속성에서 기본 클래스의 암시적 멤버와 같은 이름을 사용하는 암시적 멤버를 생성하고 [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md) 키워드를 지정합니다.  
  
 오버로드는 동일한 클래스에 있는 여러 버전의 속성 또는 프로시저 모두를 정의하는 데 사용됩니다. 기본 클래스 멤버가 이미 `Overloads`를 지정하지 않은 경우 기본 클래스 멤버의 추가 버전을 정의할 수 없습니다. 암시적 멤버는 `Overloads`를 지정하지 않으므로 컴파일러는 이 속성이 암시적 기본 클래스 멤버를 [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md) 처리한다고 간주합니다.  
  
 [!INCLUDE[vbprvb](../Token/vbprvb_md.md)] 컴파일러는 선언한 특정 프로그래밍 요소에 해당하는 암시적 멤버를 만듭니다. 다음 표에서 이러한 암시적 또는 *가상* 멤버를 요약합니다.  
  
|선언 요소|암시적으로 만든 멤버|  
|-----------|-----------------|  
|열거형|`value__` 멤버|  
|이벤트|`add_<eventname>` 프로시저<br /><br /> `remove_<eventname>` 프로시저<br /><br /> `<eventname>Event` 필드<br /><br /> `<eventname>EventHandler` 대리자|  
|속성|`get_<propertyname>` 프로시저<br /><br /> `set_<propertyname>` 프로시저|  
|`My.Form` 멤버, `My.WebService` 멤버 또는 <xref:Microsoft.VisualBasic.MyGroupCollectionAttribute> 특성으로 표시된 클래스의 멤버|`m_<variablename>` `Static` 변수<br /><br /> `<variablename>` 속성<br /><br /> `get_<variablename>` 프로시저<br /><br /> `set_<variablename>` 프로시저|  
|`WithEvents` 변수|`_<variablename>` 변수<br /><br /> `<variablename>` 속성<br /><br /> `get_<variablename>` 프로시저<br /><br /> `set_<variablename>` 프로시저|  
  
 이름 충돌의 위험이 있으므로 이러한 암시적 멤버 중 하나와 같은 형식을 사용하여 선언된 프로그래밍 요소의 이름을 지정하지 않아야 합니다. 예를 들어 요소 이름이 `get_` 또는 `set_`로 시작하지 않아야 합니다.  
  
 이 메시지는 기본적으로 경고입니다. 경고를 숨기거나 오류로 처리하는 방법에 대한 자세한 내용은 [Visual Basic에서 경고 구성](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md)을 참조하세요.  
  
 **오류 ID:** BC40024  
  
### 이 오류를 해결하려면  
  
-   암시적 기본 클래스 멤버를 숨기려면 속성을 선언할 때 [Overloads](../Topic/Overloads%20\(Visual%20Basic\).md) 키워드를 [Shadows](../Topic/Shadows%20\(Visual%20Basic\).md) 키워드로 바꿉니다.  
  
-   암시적 기본 클래스 멤버를 숨기지 않으려면 위의 표에 나열된 이름과의 충돌을 피하기 위해 속성 이름을 변경합니다.  
  
## 참고 항목  
 [Declared Element Names](../Topic/Declared%20Element%20Names%20\(Visual%20Basic\).md)