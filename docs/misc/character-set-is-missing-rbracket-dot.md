---
title: "Character set is missing &#39;]&#39;. | Microsoft Docs"
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
  - "vs.message.VS_E_RE_SETMISSINGCLOSE"
  - "vs.message.0x800A00C0"
ms.assetid: 97d2436c-498d-4eb0-a08c-8efcc7797fc0
caps.latest.revision: 6
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "douge"
---
# Character set is missing &#39;]&#39;.
이 오류는 찾기 또는 바꾸기 문자열에 지정한 정규식에 닫는 대괄호\(`]`\)가 없는 경우 발생합니다.  
  
### 이 오류를 해결하려면  
  
1.  리터럴 문자 `]`를 찾으려면 `\]`를 사용하십시오.  
  
2.  문자 집합을 찾으려면 누락된 대괄호 `]`를 입력하십시오.  
  
## 참고 항목  
 [Visual Studio에서 정규식 사용](../Topic/Using%20Regular%20Expressions%20in%20Visual%20Studio.md)   
 [NIB: Find and Replace, Quick Find](http://msdn.microsoft.com/ko-kr/dad03582-4931-4893-83ba-84b37f5b1600)   
 [파일에서 찾기](../Topic/Find%20in%20Files.md)