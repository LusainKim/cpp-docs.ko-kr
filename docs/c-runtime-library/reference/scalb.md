---
title: _scalb | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: _scalb
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
- api-ms-win-crt-math-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- scalb
- _scalb
dev_langs: C++
helpviewer_keywords:
- exponential calculations
- _scalb function
- scalb function
ms.assetid: 148cf5a8-b405-44bf-a1f0-7487adba2421
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: c6434ee3c2f2ad7a1c1d4e263f4548e5dd22e630
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="scalb"></a>_scalb
2의 거듭제곱으로 인수의 크기를 조정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
double _scalb(  
   double x,  
   long exp   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `x`  
 배정밀도, 부동 소수점 값입니다.  
  
 `exp`  
 정수(Long) 지수입니다.  
  
## <a name="return-value"></a>반환 값  
 성공하는 경우 지수 값을 반환합니다. 오버플로에서 (의 부호에 따라 `x`), `_scalb` + /-반환 `HUGE_VAL`; `errno` 변수가로 설정 된 `ERANGE`합니다.  
  
 이러한 반환 코드 및 기타 반환 코드에 대한 자세한 내용은 [_doserrno, errno, _sys_errlist 및 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)를 참조하세요.  
  
## <a name="remarks"></a>설명  
 `_scalb` 함수는 `x *` 2exp의 값을 계산합니다.  
  
## <a name="requirements"></a>요구 사항  
  
|루틴에서 반환된 값|필수 헤더|  
|-------------|---------------------|  
|`_scalb`|\<float.h>|  
  
 호환성에 대한 자세한 내용은 소개 단원의 [호환성](../../c-runtime-library/compatibility.md) 부분을 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [부동 소수점 지원](../../c-runtime-library/floating-point-support.md)   
 [ldexp](../../c-runtime-library/reference/ldexp.md)