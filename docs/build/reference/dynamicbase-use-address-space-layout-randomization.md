---
title: "-DYNAMICBASE (사용 하 여 주소 공간 레이아웃 불규칙화) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: VC.Project.VCLinkerTool.RandomizedBaseAddress
dev_langs: C++
helpviewer_keywords:
- -DYNAMICBASE linker option
- /DYNAMICBASE linker option
- DYNAMICBASE linker option
ms.assetid: 6c0ced8e-fe9c-4b63-b956-eb8a55fbceb2
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 1458070f85678d30c716622bf57740d90feb65d8
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="dynamicbase-use-address-space-layout-randomization"></a>/DYNAMICBASE(주소 공간 레이아웃을 임의로 지정)
주소 공간 레이아웃 불규칙화 (ASLR) 기능을 사용 하 여 로드 시간에 임의로 지정할 수 있는 실행 가능 이미지를 생성할지 여부를 지정 [!INCLUDE[windowsver](../../build/reference/includes/windowsver_md.md)]합니다.  
  
## <a name="syntax"></a>구문  
  
```  
/DYNAMICBASE[:NO]  
```  
  
## <a name="remarks"></a>설명  
 기본적으로 /DYNAMICBASE 켜져 있습니다.  
  
 이 옵션을 로드할 때 응용 프로그램을 임의로 지정할 해야 하는지 여부를 나타내는 실행 파일의 헤더를 수정 합니다.  
  
 주소 공간 레이아웃 불규칙화 사용할 [!INCLUDE[windowsver](../../build/reference/includes/windowsver_md.md)]합니다.  
  
### <a name="to-set-this-linker-option-in-visual-studio"></a>Visual Studio에서 이 링커 옵션을 설정하려면  
  
1.  프로젝트 **속성 페이지** 대화 상자를 엽니다. 자세한 내용은 참조 [프로젝트 속성 작업](../../ide/working-with-project-properties.md)합니다.  
  
2.  확장 된 **구성 속성** 노드.  
  
3.  확장 된 **링커** 노드.  
  
4.  선택 된 **고급** 속성 페이지.  
  
5.  수정 된 **임의 기준 주소** 속성입니다.  
  
### <a name="to-set-this-linker-option-programmatically"></a>프로그래밍 방식으로 이 링커 옵션을 설정하려면  
  
1.  <xref:Microsoft.VisualStudio.VCProjectEngine.VCLinkerTool.RandomizedBaseAddress%2A>을 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [링커 옵션 설정](../../build/reference/setting-linker-options.md)   
 [링커 옵션](../../build/reference/linker-options.md)