---
title: __CxxFrameHandler | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: __CxxFrameHandler
apilocation:
- msvcr110.dll
- msvcrt.dll
- msvcr80.dll
- msvcr100.dll
- msvcr110_clr0400.dll
- msvcr90.dll
- msvcr120.dll
apitype: DLLExport
f1_keywords: __CxxFrameHandler
dev_langs: C++
helpviewer_keywords: __CxxFrameHandler
ms.assetid: b79ac97f-425a-42ae-9b91-8beaef935333
caps.latest.revision: "3"
author: corob-msft
ms.author: corob
manager: ghogen
ms.openlocfilehash: 75f900560f226557bc160bdf74df4467b0c7aa32
ms.sourcegitcommit: ebec1d449f2bd98aa851667c2bfeb7e27ce657b2
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/24/2017
---
# <a name="cxxframehandler"></a>__CxxFrameHandler
내부 CRT 함수입니다. CRT에서 구조화된 예외 프레임을 처리하는 데 사용됩니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
EXCEPTION_DISPOSITION __CxxFrameHandler(  
      EHExceptionRecord  *pExcept,  
      EHRegistrationNode *pRN,  
      void               *pContext,   
      DispatcherContext  *pDC  
   )  
```  
  
#### <a name="parameters"></a>매개 변수  
 `pExcept`  
 가능한 `catch` 문에 전달되는 예외 레코드입니다.  
  
 `pRN`  
 예외를 처리하는 데 사용되는 스택 프레임에 대한 동적 정보입니다. 자세한 내용은 ehdata.h를 참조하세요.  
  
 `pContext`  
 컨텍스트입니다. Intel 프로세서에는 사용되지 않습니다.  
  
 `pDC`  
 함수 시작 및 스택 프레임에 대한 추가 정보입니다.  
  
## <a name="return-value"></a>반환 값  
 [try-except Statement](../cpp/try-except-statement.md)에서 사용하는 *필터 식* 값 중 하나입니다.  
  
## <a name="remarks"></a>설명  
  
## <a name="requirements"></a>요구 사항  
  
|루틴|필수 헤더|  
|-------------|---------------------|  
|__CxxFrameHandler|excpt.h, ehdata.h|