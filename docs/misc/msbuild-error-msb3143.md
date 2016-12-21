---
title: "MSBuild 오류 MSB3143 | Microsoft Docs"
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
  - "MSBuild.GenerateBootstrapper.CopyPackageError"
helpviewer_keywords: 
  - "MSB3143"
ms.assetid: b4278c8c-31df-4b4f-9ef9-7b9327e8ee77
caps.latest.revision: 6
caps.handback.revision: 6
author: "mikeblome"
ms.author: "mblome"
manager: "douge"
---
# MSBuild 오류 MSB3143
**MSB3143: '\<package\>' 항목에 대해 '\<file\>'을\(를\) 복사하는 동안 오류가 발생했습니다. '\<error\>'**  
  
 이 오류는 부트스트래퍼 패키지를 빌드 출력 디렉터리에 복사할 때 발생합니다.  이 오류가 발생하는 원인은 다음과 같습니다.  
  
-   빌드 출력 디렉터리에 복사하는 데 필요한 권한이 없습니다.  
  
-   디스크가 꽉 찼습니다.  
  
 file.copy 또는 directory.createdirectory 실패 시에도 동일한 원인을 의심해 볼 수 있습니다.  
  
## 참고 항목  
 [제품 및 패키지 스키마 참조](../Topic/Product%20and%20Package%20Schema%20Reference.md)   
 [\<PackageFiles\> 요소](../Topic/%3CPackageFiles%3E%20Element%20\(Bootstrapper\).md)