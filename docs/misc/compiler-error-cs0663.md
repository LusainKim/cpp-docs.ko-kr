---
title: "컴파일러 오류 CS0663 | Microsoft Docs"
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
  - "CS0663"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0663"
ms.assetid: 9f96c42b-dcc8-4a0f-8404-289fc88dba5e
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS0663
ref 및 out만 다른 오버로드된 메서드를 정의할 수 없습니다.  
  
 매개 변수에서 [ref](../Topic/ref%20\(C%23%20Reference\).md) 및 [out](../Topic/out%20\(C%23%20Reference\).md) 사용만 다른 메서드는 허용되지 않습니다.  
  
 다음 샘플에서는 CS0663을 생성합니다.  
  
```  
// CS0663.cs class TestClass { public static void Main() { } public void Test(ref int i) { } public void Test(out int i)   // CS0663 { } }  
```