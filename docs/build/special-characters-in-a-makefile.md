---
title: "메이크파일의 특수 문자 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- NMAKE program, special characters
- makefiles, special characters
- special characters, in NMAKE macros
- macros, special characters
ms.assetid: 92c34ab5-ca6b-4fc0-bcf4-3172eaeda9f0
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6c574040d6004516682379a5e64b87c1b92388ec
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="special-characters-in-a-makefile"></a>메이크파일의 특수 문자
NMAKE 특수 문자를 리터럴 문자로 사용 하려면 문자 앞에 캐럿 (^) 합니다. NMAKE 다른 문자 앞에 있는 캐럿을 무시 합니다. 특수 문자에는  
  
 `:  ;  #  (  )  $  ^  \  {  }  !  @  —`  
  
 따옴표 붙은 문자열 내에서 캐럿 (^) 캐럿 리터럴 문자로 처리 됩니다. 줄의 끝에 캐럿 문자열이 나 매크로 리터럴 줄 바꿈 문자를 삽입합니다.  
  
 백슬래시는 매크로 (\\) 뒤에 줄 바꿈을 하 여 문자는 공백으로 바뀝니다.  
  
 명령, 백분율 기호 (%)이 파일 지정자입니다. % 명령에 리터럴로 나타낼 한 파일만 대신 두 개의 백분율 기호 (%)를 지정 합니다. NMAKE 다른 상황에서는 단일 % 리터럴로 해석 하지만 double를 항상 해석 % % 하나의 %로 합니다. 따라서 리터럴 나타내기 위해 % %, 3% 기호 중 하나를 지정 %%%, 또는 네 개의 백분율 기호 %%%입니다.  
  
 명령에서 리터럴 문자로 달러 기호 ($)를 사용 하려면 두 개의 달러 기호 ($$)를 지정 합니다. 다른 경우에도이 메서드를 사용할 수 있는 ^ $ 작동 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [메이크파일의 내용](../build/contents-of-a-makefile.md)