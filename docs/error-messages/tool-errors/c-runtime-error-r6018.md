---
title: "C 런타임 오류 R6018 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: R6018
dev_langs: C++
helpviewer_keywords: R6018
ms.assetid: f6dd40d1-a119-4d8b-b39e-97350ea23349
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0102739bb4fa8961e089d348e1ff93f62fdde6b6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="c-runtime-error-r6018"></a>C 런타임 오류 R6018
예기치 않은 힙 오류입니다.  
  
> [!NOTE]
>  응용 프로그램을 실행 하는 동안이 오류 메시지를 발생 하는 경우 응용 프로그램 종료가 내부 문제가 있기 때문입니다. 이 오류에 대 한 여러 가지가 있지만 응용 프로그램의 코드에서 결함으로 인 경우가 많습니다.  
>   
>  이 오류를 해결하려면 다음 단계를 시도할 수 있습니다.  
>   
>  -   사용 하 여는 **앱 및 기능** 또는 **프로그램 및 기능** 페이지에 **제어판** 를 복구 하거나 프로그램을 다시 설치 합니다.  
> -   확인 **Windows Update** 에 **제어판** 소프트웨어 업데이트에 대 한 합니다.  
> -   응용 프로그램의 업데이트 된 버전을 확인 합니다. 문제가 지속 되는 경우 앱 공급 업체에 문의 합니다.  
  
 **프로그래머에 대 한 정보**  
  
 프로그램은 메모리 관리 작업을 수행 하는 동안 예기치 않은 오류가 발생 했습니다.  
  
 이 오류는 일반적으로 프로그램 실행 시 힙 데이터를 부주의 하 게 변경할 경우에 발생 합니다. 그러나 런타임 또는 운영 체제 코드의 내부 오류로 인해 발생할 수도 있습니다.  
  
 이 문제를 해결 하려면 코드에서 힙 손상 버그를 확인 합니다. 자세한 내용 및 예제에 대 한 참조 [CRT 디버그 힙 정보](/visualstudio/debugger/crt-debug-heap-details)합니다. 다음으로 응용 프로그램 배포에 대 한 최신 재배포 가능 패키지를 사용 하 고 있는지 확인 합니다. 자세한 내용은 참조 [Visual c + +에서 배포](../../ide/deployment-in-visual-cpp.md)합니다.