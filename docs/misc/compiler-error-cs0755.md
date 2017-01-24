---
title: "컴파일러 오류 CS0755 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CS0755"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0755"
ms.assetid: 80613029-a009-4bdf-b1c2-1eec1e60c7b4
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0755
두 부분 메서드\(Partial Method\) 선언 모두 확장 메서드이거나 확장 메서드가 아니어야 합니다.  
  
 부분 메서드\(Partial Method\)는 하나의 정의 선언\(서명\)과 선택적 구현 선언\(본문\)으로 구성됩니다. 정의 선언이 확장 메서드인 경우 구현 선언\(정의된 경우\)도 확장 메서드여야 합니다. 또한 정의 메서드가 확장 메서드가 아닌 경우 구현 메서드도 확장 메서드가 아니어야 합니다.  
  
### 이 오류를 해결하려면  
  
1.  부분 중 하나에서 `this` 한정자를 제거하거나 다른 부분에 추가합니다.  
  
## 예제  
 다음 예제에서는 CS0755를 생성합니다.  
  
```  
// cs0755.cs public static partial class Ext { static partial void Part(this C c); //Extension method // Typically the implementing declaration is in a separate file. static partial void Part(C c) //CS0755 { } } public partial class C { public static int Main() { return 1; } }  
```  
  
## 참고 항목  
 [확장 메서드](../Topic/Extension%20Methods%20\(C%23%20Programming%20Guide\).md)