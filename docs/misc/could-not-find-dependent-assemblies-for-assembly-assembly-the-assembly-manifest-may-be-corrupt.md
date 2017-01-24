---
title: "어셈블리 &#39;assembly&#39;에 대한 종속 어셈블리를 찾을 수 없습니다. 어셈블리 매니페스트가 손상되었을 수 있습니다. | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.tasklisterror.cannotfinddependencies"
ms.assetid: 6d6e6dda-6cec-49d0-9659-63dfdbd7d247
caps.latest.revision: 8
caps.handback.revision: 8
author: "mikeblome"
ms.author: "mblome"
manager: "douge"
---
# 어셈블리 &#39;assembly&#39;에 대한 종속 어셈블리를 찾을 수 없습니다. 어셈블리 매니페스트가 손상되었을 수 있습니다.
프로젝트 시스템에서 어셈블리의 종속성을 확인할 수 없기 때문에 프로젝트가 참조하는 어셈블리를 프로젝트 시스템이 읽지 못했습니다. 이 오류가 발생해도 프로젝트는 빌드됩니다. 그러나 런타임 오류가 발생할 수 있습니다.  
  
 **이 오류를 해결하려면**  
  
-   Visual Studio를 다시 설치하세요\(어셈블리가 [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] 또는 [!INCLUDE[dnprdnshort](../Token/dnprdnshort_md.md)]과 함께 제공된 경우\).  
  
     또는  
  
-   적절한 타사 컨트롤을 다시 설치하세요.  
  
## 참고 항목  
 [끊어진 참조 문제 해결](../Topic/Troubleshooting%20Broken%20References.md)   
 [NIB 방법: 참조 추가 대화 상자를 사용하여 참조 추가 또는 제거](http://msdn.microsoft.com/ko-kr/3bd75d61-f00c-47c0-86a2-dd1f20e231c9)   
 [Assemblies in the Common Language Runtime](http://msdn.microsoft.com/ko-kr/33a0bc6a-6bb3-44c7-ada7-4a046e8c0945)