---
title: "두 개 이상의 형식이 가능하므로 이 인수에서 &#39;&lt;methodname&gt;&#39; 메서드에 있는 형식 매개 변수의 데이터 형식을 유추할 수 없습니다. | Microsoft Docs"
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
  - "bc36651"
  - "bc36654"
  - "vbc36651"
  - "vbc36654"
helpviewer_keywords: 
  - "BC36651"
  - "BC36654"
ms.assetid: d4bf408c-ca1f-44ad-855a-3df898de60c6
caps.latest.revision: 9
caps.handback.revision: 9
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# 두 개 이상의 형식이 가능하므로 이 인수에서 &#39;&lt;methodname&gt;&#39; 메서드에 있는 형식 매개 변수의 데이터 형식을 유추할 수 없습니다.
두 개 이상의 형식이 가능하므로 이 인수에서 '\<methodname\>' 메서드에 있는 형식 매개 변수의 데이터 형식을 유추할 수 없습니다. 데이터 형식을 명시적으로 지정하면 이 오류를 해결할 수 있습니다.  
  
 형식 유추를 사용하여 제네릭 프로시저 호출에서 형식 매개 변수의 형식을 확인하려고 했습니다. 컴파일러에서는 둘 이상의 형식 매개 변수에 가능한 데이터 형식을 둘 이상 찾고 이 오류를 보고합니다.  
  
> [!NOTE]
>  인수 지정이 옵션이 아닌 경우\(예: 쿼리 식의 쿼리 연산자\) 두 번째 문장 없이 오류 메시지가 나타납니다.  
  
 다음 코드에서는  오류를 보여 줍니다.  
  
```vb#  
Option Strict Off Module Module1 Sub Main() '' Not valid. 'targetMethod(1, "2") End Sub Sub targetMethod(Of T)(ByVal p1 As T, ByVal p2 As T) End Sub End Module  
```  
  
 **오류 ID:** BC36654\([!INCLUDE[vbteclinq](../misc/includes/vbteclinq_md.md)] 쿼리 내부\) 및 BC36651\(쿼리 외부\)  
  
### 이 오류를 해결하려면  
  
-   쿼리 외부에서 오류가 나타난 경우 형식 매개 변수의 데이터 형식을 명시적으로 지정합니다.  
  
    ```  
    targetMethod(Of Integer)(1, "2")  
    ```  
  
## 참고 항목  
 [Option Strict Statement](../Topic/Option%20Strict%20Statement.md)   
 [Generic Procedures in Visual Basic](../Topic/Generic%20Procedures%20in%20Visual%20Basic.md)