---
title: "_CrtGetReportHook | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _CrtGetReportHook
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- CrtGetReportHook
- _CrtGetReportHook
dev_langs:
- C++
helpviewer_keywords:
- CrtGetReportHook function
- _CrtGetReportHook function
ms.assetid: 922758ed-7edd-4359-9c92-0535192dc11a
caps.latest.revision: 
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload:
- cplusplus
ms.openlocfilehash: 94b92ee2bc6f30df99db23cb1417f1e490d24fa5
ms.sourcegitcommit: 185e11ab93af56ffc650fe42fb5ccdf1683e3847
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2018
---
# <a name="crtgetreporthook"></a>_CrtGetReportHook
디버그 보고 프로세스에서 C 런타임에 클라이언트 정의 보고 함수를 연결하기 위해 해당 함수를 검색합니다(디버그 버전에만 해당).  
  
## <a name="syntax"></a>구문  
  
```  
_CRT_REPORT_HOOK _CrtGetReportHook( void );  
```  
  
## <a name="return-value"></a>반환 값  
 현재 클라이언트 정의 보고 함수를 반환합니다.  
  
## <a name="remarks"></a>설명  
 `_CrtGetReportHook`를 사용하면 응용 프로그램이 C 런타임 디버그 라이브러리 보고 프로세스에서 현재 보고 함수를 검색할 수 있습니다.  
  
 다른 후크 가능 런타임 함수를 사용하고 고유한 클라이언트 정의 후크 함수를 작성하는 방법에 대한 자세한 내용은 [디버그 후크 함수 작성](/visualstudio/debugger/debug-hook-function-writing)을 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
  
|루틴에서 반환된 값|필수 헤더|  
|-------------|---------------------|  
|`_CrtGetReportHook`|\<crtdbg.h>|  
  
 호환성에 대한 자세한 내용은 소개 단원의 [호환성](../../c-runtime-library/compatibility.md) 부분을 참조하세요.  
  
## <a name="libraries"></a>라이브러리  
 [C 런타임 라이브러리](../../c-runtime-library/crt-library-features.md)의 디버그 버전만 해당됩니다.  
  
## <a name="example"></a>예  
 `_CrtSetReportHook`를 사용하는 방법에 대한 샘플은 [report 샘플: C 런타임 디버깅 보고서 함수](https://github.com/Microsoft/VCSamples/tree/master/VC2010Samples/crt/report)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [디버그 루틴](../../c-runtime-library/debug-routines.md)   
 [_CrtSetReportHook](../../c-runtime-library/reference/crtsetreporthook.md)