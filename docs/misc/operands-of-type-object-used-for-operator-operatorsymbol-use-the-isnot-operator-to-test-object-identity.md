---
title: "&#39;&lt;operatorsymbol&gt;&#39; 연산자에 대해 Object 형식의 피연산자를 사용했습니다. 개체 ID를 테스트하려면 &#39;IsNot&#39; 연산자를 사용하세요. | Microsoft Docs"
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
  - "vbc42032"
  - "bc42032"
helpviewer_keywords: 
  - "BC42032"
ms.assetid: f43b163b-f8f6-489d-ba9e-df6398ccc553
caps.latest.revision: 8
caps.handback.revision: 8
author: "stevehoag"
ms.author: "shoag"
manager: "wpickett"
---
# &#39;&lt;operatorsymbol&gt;&#39; 연산자에 대해 Object 형식의 피연산자를 사용했습니다. 개체 ID를 테스트하려면 &#39;IsNot&#39; 연산자를 사용하세요.
식은 [Object Data Type](../Topic/Object%20Data%20Type.md)의 하나 혹은 두 피연산자로 `<>` 연산자를 사용합니다.  
  
 `Is` 또는 `IsNot` 연산자를 사용하여 두 개체 참조가 동일한 개체 인스턴스를 참조하는지 확인합니다.[Comparison Operators in Visual Basic](../Topic/Comparison%20Operators%20in%20Visual%20Basic.md)에서 "개체 비교"를 참조하세요.  
  
 변수나 식이 `Object`로 평가되는 경우 컴파일러가 *런타임에 바인딩*을 수행해야 하므로 런타임에 추가 작업이 필요합니다. 또한 응용 프로그램이 잠재적인 런타임 오류에 노출됩니다. 예를 들어 `Object` 변수에 <xref:System.Windows.Forms.Form>을 할당하여 `<>` 연산자에서 사용하려고 하는 경우 Visual Basic은 <xref:System.Windows.Forms.Form> 개체를 값 비교에 적합한 데이터 형식으로 변환할 수 없기 때문에 런타임이 <xref:System.InvalidCastException>을 throw합니다. 두 피연산자가 <xref:System.Windows.Forms.Form> 형식으로 평가되더라도 `<>`가 <xref:System.Windows.Forms.Form> 피연산자에 대해 정의되지 않았기 때문에 작업이 실패합니다.  
  
 이 메시지는 기본적으로 경고입니다. 경고를 숨기거나 오류로 처리하는 방법에 대한 자세한 내용은 [Visual Basic에서 경고 구성](../Topic/Configuring%20Warnings%20in%20Visual%20Basic.md)을 참조하세요.  
  
 **오류 ID:** BC42032  
  
### 이 오류를 해결하려면  
  
-   두 개체 참조가 동일한 개체 인스턴스를 참조하는지 확인하려면 `Is` 또는 `IsNot` 연산자를 사용합니다.  
  
## 참고 항목  
 [Comparison Operators in Visual Basic](../Topic/Comparison%20Operators%20in%20Visual%20Basic.md)   
 [IsNot Operator](../Topic/IsNot%20Operator%20\(Visual%20Basic\).md)   
 [How to: Determine Whether Two Objects Are Related](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Related%20\(Visual%20Basic\).md)   
 [How to: Determine Whether Two Objects Are Identical](../Topic/How%20to:%20Determine%20Whether%20Two%20Objects%20Are%20Identical%20\(Visual%20Basic\).md)