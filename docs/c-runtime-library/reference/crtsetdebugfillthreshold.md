---
title: "_CrtSetDebugFillThreshold | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: _CrtSetDebugFillThreshold
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
- _CrtSetDebugFillThreshold
- CrtSetDebugFillThreshold
dev_langs: C++
helpviewer_keywords:
- debug, buffer-filling behavior
- CrtSetDebugFillThreshold function
- _CrtSetDebugFillThreshold function
- buffer-filling behavior
- 0xFD
ms.assetid: 6cb360e8-56ae-4248-b17f-e28aee3e0ed7
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 0d8fcbf7f354def49056c1e519e910edccde56cd
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="crtsetdebugfillthreshold"></a>_CrtSetDebugFillThreshold
디버그 함수에서 버퍼 채우기 동작을 제어하는 임계값을 검색하고 수정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
size_t _CrtSetDebugFillThreshold(  
   size_t _NewThreshold  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `newThreshold`  
 새 임계값입니다.  
  
## <a name="return-value"></a>반환 값  
 이전 임계값입니다.  
  
## <a name="remarks"></a>설명  
 보안이 강화 된 CRT 함수는 일부의 디버그 버전은 특수 문자를 사용 하 여 전달 된 버퍼를 채웁니다 (0xFE). 이를 통해 잘못된 크기가 함수에 전달된 경우를 찾을 수 있습니다. 그러나 성능 또한 줄어듭니다. 성능을 향상시키기 위해서는 `_CrtSetDebugFillThreshold`를 사용하여 임계값보다 큰 버퍼에 대한 버퍼 채우기를 비활성화해야 합니다. 임계값이 0이면 모든 버퍼에 대해 비활성화됩니다.  
  
 기본 임계값은 `SIZE_T_MAX`입니다.  
  
 영향을 미치는 함수의 목록은 다음과 같습니다.  
  
-   [strcpy_s, wcscpy_s, _mbscpy_s](../../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md)  
  
-   [strncpy_s, _strncpy_s_l, wcsncpy_s, _wcsncpy_s_l, _mbsncpy_s, _mbsncpy_s_l](../../c-runtime-library/reference/strncpy-s-strncpy-s-l-wcsncpy-s-wcsncpy-s-l-mbsncpy-s-mbsncpy-s-l.md)  
  
-   [_mbsnbcpy_s, _mbsnbcpy_s_l](../../c-runtime-library/reference/mbsnbcpy-s-mbsnbcpy-s-l.md)  
  
-   [strcat_s, wcscat_s, _mbscat_s](../../c-runtime-library/reference/strcat-s-wcscat-s-mbscat-s.md)  
  
-   [strncat_s, _strncat_s_l, wcsncat_s, _wcsncat_s_l, _mbsncat_s, _mbsncat_s_l](../../c-runtime-library/reference/strncat-s-strncat-s-l-wcsncat-s-wcsncat-s-l-mbsncat-s-mbsncat-s-l.md)  
  
-   [_mbsnbcat_s, _mbsnbcat_s_l](../../c-runtime-library/reference/mbsnbcat-s-mbsnbcat-s-l.md)  
  
-   [_strset_s, _strset_s_l, _wcsset_s, _wcsset_s_l, _mbsset_s, _mbsset_s_l](../../c-runtime-library/reference/strset-s-strset-s-l-wcsset-s-wcsset-s-l-mbsset-s-mbsset-s-l.md)  
  
-   [_strnset_s, _strnset_s_l, _wcsnset_s, _wcsnset_s_l, _mbsnset_s, _mbsnset_s_l](../../c-runtime-library/reference/strnset-s-strnset-s-l-wcsnset-s-wcsnset-s-l-mbsnset-s-mbsnset-s-l.md)  
  
-   [_mbsnbset_s, _mbsnbset_s_l](../../c-runtime-library/reference/mbsnbset-s-mbsnbset-s-l.md)  
  
-   [_makepath_s, _wmakepath_s](../../c-runtime-library/reference/makepath-s-wmakepath-s.md)  
  
-   [_splitpath_s, _wsplitpath_s](../../c-runtime-library/reference/splitpath-s-wsplitpath-s.md)  
  
-   [_strlwr_s, _strlwr_s_l, _mbslwr_s, _mbslwr_s_l, _wcslwr_s, _wcslwr_s_l](../../c-runtime-library/reference/strlwr-s-strlwr-s-l-mbslwr-s-mbslwr-s-l-wcslwr-s-wcslwr-s-l.md)  
  
-   [_strupr_s, _strupr_s_l, _mbsupr_s, _mbsupr_s_l, _wcsupr_s, _wcsupr_s_l](../../c-runtime-library/reference/strupr-s-strupr-s-l-mbsupr-s-mbsupr-s-l-wcsupr-s-wcsupr-s-l.md)  
  
-   [strerror_s, _strerror_s, _wcserror_s, \__wcserror_s](../../c-runtime-library/reference/strerror-s-strerror-s-wcserror-s-wcserror-s.md)  
  
-   [_itoa_s, _i64toa_s, _ui64toa_s, _itow_s, _i64tow_s, _ui64tow_s](../../c-runtime-library/reference/itoa-s-i64toa-s-ui64toa-s-itow-s-i64tow-s-ui64tow-s.md)  
  
-   [_ecvt_s](../../c-runtime-library/reference/ecvt-s.md)  
  
-   [_fcvt_s](../../c-runtime-library/reference/fcvt-s.md)  
  
-   [_gcvt_s](../../c-runtime-library/reference/gcvt-s.md)  
  
## <a name="requirements"></a>요구 사항  
  
|루틴에서 반환된 값|필수 헤더|  
|-------------|---------------------|  
|`_CrtSetDebugFillThreshold`|\<crtdbg.h>|  
  
 호환성에 대한 자세한 내용은 소개 단원의 [호환성](../../c-runtime-library/compatibility.md) 부분을 참조하세요.  
  
## <a name="libraries"></a>라이브러리  
 [C 런타임 라이브러리](../../c-runtime-library/crt-library-features.md)의 디버그 버전만 해당됩니다.  
  
## <a name="example"></a>예  
  
```C  
// crt_crtsetdebugfillthreshold.c  
// compile with: cl /MTd crt_crtsetdebugfillthreshold.c  
#include <stdio.h>  
#include <stdlib.h>  
#include <string.h>  
#include <crtdbg.h>  
  
void Clear( char buff[], size_t size )  
{  
   for( int i=0; i<size; ++i )  
      buff[i] = 0;  
}  
  
void Print( char buff[], size_t size )  
{  
   for( int i=0; i<size; ++i )  
      printf( "%02x  %c\n", (unsigned char)buff[i], buff[i] );  
}  
  
int main( void )  
{  
   char buff[10];  
  
   printf( "With buffer-filling on:\n" );  
   strcpy_s( buff, _countof(buff), "howdy" );  
   Print( buff, _countof(buff) );  
  
   _CrtSetDebugFillThreshold( 0 );  
  
   printf( "With buffer-filling off:\n" );  
   Clear( buff, _countof(buff) );  
   strcpy_s( buff, _countof(buff), "howdy" );  
   Print( buff, _countof(buff) );  
}  
```  
  
```Output  
With buffer-filling on:  
68  h  
6f  o  
77  w  
64  d  
79  y  
00  
fe  ■  
fe  ■  
fe  ■  
fe  ■  
With buffer-filling off:  
68  h  
6f  o  
77  w  
64  d  
79  y  
00  
00  
00  
00  
00  
```  
  
## <a name="see-also"></a>참고 항목  
 [디버그 루틴](../../c-runtime-library/debug-routines.md)