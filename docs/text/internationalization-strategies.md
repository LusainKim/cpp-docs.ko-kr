---
title: "국제화 전략 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- globalization [C++], character sets
- language-portable code [C++]
- MBCS [C++], internationalization strategies
- Windows API [C++], international programming strategies
- Win32 [C++], international programming strategies
- Unicode [C++], globalizing applications
- character sets [C++], international programming strategies
- localization [C++], character sets
ms.assetid: b09d9854-0709-4b9a-a00c-b0b8bc4199b1
caps.latest.revision: "8"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6b7ab27bb7a6458efde84451febaeb6f3ef37115
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="internationalization-strategies"></a>국제화 전략
대상 운영 체제와 시장에 따라 몇 가지 국제화 전략 해야 합니다.  
  
-   응용 프로그램에서는 유니코드를 따라서 Windows 95 또는 Windows 98에는 없지만 Windows 2000 및 Windows NT를 실행 합니다.  
  
     유니코드 관련 기능을 사용 하 고 모든 문자는 너비가 16 비트 (특별 한 용도로 프로그램의 일부에서 ANSI 문자를 사용할 수 있습니다). C 런타임 라이브러리 함수, 매크로 및 데이터 형식을 유니코드 전용 프로그래밍 제공합니다. MFC는 완전히 유니코드를 지원 합니다.  
  
-   응용 프로그램 MBCS를 사용 하 고 모든 Win32 플랫폼에서 실행할 수 있습니다.  
  
     MBCS 특정 기능을 사용 합니다. 문자열에는 단일 바이트 문자, 더블 바이트 문자 또는 둘 다 포함 될 수 있습니다. C 런타임 라이브러리 함수, 매크로 및 데이터 형식을 MBCS 전용 프로그래밍 제공합니다. MFC는 MBCS를 완벽 하 게 지원 합니다.  
  
-   전체 이식성에 대 한 응용 프로그램에 대 한 소스 코드를 작성-기호로 다시 컴파일하여 **_UNICODE** 또는 기호 **_MBCS** 정의 중 하나를 사용 하는 버전 생성할 수 있습니다. 자세한 내용은 참조 [Tchar.h의 제네릭 텍스트 매핑](../text/generic-text-mappings-in-tchar-h.md)합니다.  
  
-   응용 프로그램에서 설명 하는 것 처럼 Windows 95, Windows 98 및 Windows ME에서 유니코드 함수에 누락 된 래퍼 라이브러리를 사용 하 여 [모두 Windows 98 및 Windows 2000에서 실행 되는 단일 유니코드 앱 디자인](http://go.microsoft.com/fwlink/p/?LinkId=250770)합니다. 상업적으로 래퍼 라이브러리를 사용할 수 수도 있습니다.  
  
     완전히 이식 가능한 C 런타임 함수, 매크로 및 데이터 형식을 사용. MFC의 유연성 다음이 전략 중 하나를 지원합니다.  
  
 이 항목의 나머지 부분에서는 MBCS 또는 유니코드로 빌드할 수 있는 완전히 이식 가능한 코드 작성에 집중 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [유니코드 및 MBCS](../text/unicode-and-mbcs.md)   
 [로캘 및 코드 페이지](../text/locales-and-code-pages.md)