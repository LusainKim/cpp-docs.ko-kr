---
title: "컴파일러 오류 CS0057 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0057"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0057"
ms.assetid: 0bdd628f-7a1f-4209-bb28-c4a66eb3bf1d
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0057
일관성 없는 접근성: 'type' 매개 변수 형식이 'operator' 연산자보다 접근성이 부족합니다.  
  
 공용 구문은 공개적으로 액세스 가능한 개체를 반환해야 합니다. 자세한 내용은 [액세스 한정자](../Topic/Access%20Modifiers%20\(C%23%20Programming%20Guide\).md)을 참조하세요.  
  
 다음 샘플에서는 CS0057을 생성합니다.  
  
```  
// CS0057.cs class MyClass //defaults to private accessibility // try the following line instead // public class MyClass { } public class MyClass2 { public static implicit operator MyClass2(MyClass iii)   // CS0057 { return new MyClass2(); } public static void Main() { } }  
```