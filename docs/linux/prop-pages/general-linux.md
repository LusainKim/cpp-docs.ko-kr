---
title: "일반 속성(Linux C++ 프로젝트)| Microsoft Docs"
ms.custom: 
ms.date: 9/26/2017
ms.reviewer: 
ms.suite: 
ms.technology: vs-ide-general
ms.tgt_pltfrm: 
ms.topic: article
ms.assetid: 56c800a9-3df9-4196-87b2-81adb00e4767
author: mikeblome
ms.author: mblome
manager: ghogen
f1_keywords:
- VC.Project.VCConfiguration.OutputDirectory
- VC.Project.VCConfiguration.IntermediateDirectory
- VC.Project.VCConfiguration.TargetName
- VC.Project.VCConfiguration.TargetExt
- VC.Project.VCConfiguration.DeleteExtensionsOnClean
- VC.Project.VCConfiguration.PlatformToolset
- VC.Project.VCConfiguration.BuildLogFile
- VC.Project.VCConfiguration.ConfigurationType
- VC.Project.VCConfiguration.UseOfSTL
ms.openlocfilehash: 4de08a00ddedf1eec97d1872646a986e09c22547
ms.sourcegitcommit: ca2f94dfd015e0098a6eaf5c793ec532f1c97de1
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/31/2017
---
# <a name="general-properties-linux-c"></a>일반 속성(Linux C++)

속성 | 설명 | 선택 항목
--- | ---| ---
출력 디렉터리 | 출력 파일 디렉터리에 대한 상대 경로를 지정하며 환경 변수를 포함할 수 있습니다.
중간 디렉터리 | 중간 파일 디렉터리에 대한 상대 경로를 지정하며 환경 변수를 포함할 수 있습니다.
대상 이름 | 이 프로젝트에서 생성할 파일 이름을 지정합니다.
대상 확장명 | 이 프로젝트에서 생성할 파일 확장자를 지정합니다. (예: .a)
정리할 때 삭제할 확장명 | 정리하거나 다시 빌드할 때 삭제할 중간 디렉터리에 있는 파일에 대한 세미콜론으로 구분된 와일드카드 규칙입니다.
빌드 로그 파일 | 빌드 로깅을 사용하도록 설정된 경우 작성할 빌드 로그 파일을 지정합니다.
플랫폼 도구 집합 | 현재 구성을 빌드하는 데 사용하는 도구 집합을 지정합니다. 지정하지 않으면 기본 도구 집합이 사용됩니다.
원격 빌드 컴퓨터 | 원격 빌드, 배포 및 디버그에 사용할 대상 컴퓨터 또는 장치입니다.
원격 빌드 루트 디렉터리 | 원격 컴퓨터 또는 장치의 디렉터리에 대한 경로를 지정합니다.
원격 빌드 프로젝트 디렉터리 | 원격 컴퓨터 또는 장치의 디렉터리에 대한 경로를 지정합니다.
구성 형식 | 이 구성에서 생성하는 출력 형식을 지정합니다. | **동적 라이브러리(.so)** - 동적 라이브러리(.so)<br>**정적 라이브러리(.a)** - 정적 라이브러리(.a)<br>**응용 프로그램(.out)** - 응용 프로그램(.out)<br>**메이크파일** - 메이크파일<br>
STL 사용 | 이 구성에 대해 사용할 C++ 표준 라이브러리를 지정합니다. | **공유 GNU 표준 C++ 라이브러리**<br>**정적 GNU 표준 C++ 라이브러리(-static)**<br>