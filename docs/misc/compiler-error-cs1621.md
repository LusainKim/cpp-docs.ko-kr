---
title: "컴파일러 오류 CS1621 | Microsoft Docs"
ms.custom: ""
ms.date: "11/23/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS1621"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1621"
ms.assetid: 11b4fb94-0dd7-4484-99aa-e06eacc6a658
caps.latest.revision: 10
caps.handback.revision: 10
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS1621
yield 문은 무명 메서드 또는 람다 식 안에 사용할 수 없습니다.  
  
 yield 문은 반복기의 무명 메서드 블록 안에 있을 수 없습니다.  
  
## 예제  
 다음 샘플에서는 CS1621을 생성합니다.  
  
```  
// CS1621.cs using System.Collections; delegate object MyDelegate(); class C : IEnumerable { public IEnumerator GetEnumerator() { MyDelegate d = delegate { yield return this; // CS1621 return this; }; d(); // Try this instead: // MyDelegate d = delegate { return this; }; // yield return d(); } public static void Main() { } }  
```  
  
## 참고 항목  
 [반복기](../Topic/Iterators%20\(C%23%20and%20Visual%20Basic\).md)   
 [yield](../Topic/yield%20\(C%23%20Reference\).md)   
 [람다 식](../Topic/Lambda%20Expressions%20\(C%23%20Programming%20Guide\).md)   
 [무명 메서드](../Topic/Anonymous%20Methods%20\(C%23%20Programming%20Guide\).md)