---
title: "컴파일러 오류 CS1517 | Microsoft Docs"
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
  - "CS1517"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1517"
ms.assetid: 3b0201fb-8fab-4e6a-9ad9-f04c0de89517
caps.latest.revision: 7
caps.handback.revision: 7
author: "BillWagner"
ms.author: "wiwagn"
manager: "wpickett"
---
# 컴파일러 오류 CS1517
전처리기 식이 잘못되었습니다.  
  
 컴파일러가 잘못된 전처리기 식을 발견했습니다.  
  
 자세한 내용은 [전처리기 지시문](../Topic/C%23%20Preprocessor%20Directives.md)을 참조하세요.  
  
 다음 샘플에서는 유효한 전처리기 식과 잘못된 전처리기 식을 보여 줍니다.  
  
```  
// CS1517.cs #if symbol      // OK #endif #if !symbol     // OK #endif #if (symbol)    // OK #endif #if true        // OK #endif #if false       // OK #endif #if 1           // CS1517 #endif #if ~symbol     // CS1517 #endif #if *           // CS1517 #endif class x { public static void Main() { } }  
```