---
title: "CLS 규격 경고 CLS03603 | Microsoft Docs"
ms.custom: ""
ms.date: "10/29/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "CLS03603"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CLS03603"
ms.assetid: 8bd74395-6b44-427d-8fe0-648dd946e6d2
caps.latest.revision: 8
caps.handback.revision: 8
author: "corob-msft"
ms.author: "corob"
manager: "douge"
---
# CLS 규격 경고 CLS03603
전역 정적 필드는 CLS 규격입니다.  
  
 전역 정적 필드 및 메서드는 CLS 규격입니다.  
  
 CLS\(공용 언어 하위 집합\) 규격 검사에 대한 자세한 내용은 [CLS 규격 어셈블리](http://msdn.microsoft.com/ko-kr/3320b57e-ea55-4697-a17d-f509a36a3c93)를 참조하세요.  
  
 다음 샘플에서는 CLS03603을 생성합니다.  
  
```  
// CLS03603.cpp // compile with: /clr /LD // CLS03603 expected using namespace System; using namespace System::Reflection; [assembly:CLSCompliant (true)]; [assembly:AssemblyKeyFile("clscompliance.snk")]; int i;   // CLS03603 public ref class MyClass { public: int i;   // OK };  
```