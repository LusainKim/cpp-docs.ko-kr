---
title: _stat, _stat32, _stat64, _stati64, _stat32i64, _stat64i32, _wstat, _wstat32, _wstat64, _wstati64, _wstat32i64, _wstat64i32 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- _wstat64
- _stati64
- _stat32
- _stat32i64
- _stat
- _wstati64
- _wstat32
- _wstat64i32
- _wstat
- _stat64
- _stat64i32
- _wstat32i64
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
- api-ms-win-crt-filesystem-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- tstat32
- tstat
- _tstat64i32
- tstati64
- _wstat64
- _wstat32
- wstati64
- tstat64
- _stati64
- _wstat
- wstat64i32
- stat32i64
- tstat32i64
- _tstat
- _wstati64
- _tstati64
- _wstat32i64
- wstat32
- _wstat64i32
- _stat
- _tstat32
- stat64i32
- wstat64
- stat
- _stat32i64
- _stat32
- stati64
- wstat
- _stat64i32
- stat32
- _tstat32i64
- tstat64i32
- _tstat64
- _stat64
- stat/_stat
- stat/_stat32
- stat/_stat64
- stat/_stati64
- stat/_stat32i64
- stat/_stat64i32
- stat/_wstat
- stat/_wstat32
- stat/_wstat64
- stat/_wstati64
- stat/_wstat32i64
- stat/_wstat64i32
dev_langs: C++
helpviewer_keywords:
- files [C++], status information
- _stat function
- _wstat function
- _stat64i32 function
- tstat function
- _tstat64i32 function
- _stati64 function
- _stat64 function
- tstati64 function
- wstati64 function
- wstat64 function
- _wstat64i32 function
- _tstat32i64 function
- _stat32i64 function
- stat function
- status of files
- _tstat32 function
- tstat64 function
- _wstat64 function
- _tstat function
- _stat32 function
- wstat function
- _wstat32i64 function
- _tstati64 function
- _wstat32 function
- stat64 function
- stati64 function
- _wstati64 function
- _tstat64 function
- files [C++], getting status information
ms.assetid: 99a75ae6-ff26-47ad-af70-5ea7e17226a5
caps.latest.revision: "26"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: ed4a232cc5d563a724adf29500e70aa28cf36432
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="stat-stat32-stat64-stati64-stat32i64-stat64i32-wstat-wstat32-wstat64-wstati64-wstat32i64-wstat64i32"></a>_stat, _stat32, _stat64, _stati64, _stat32i64, _stat64i32, _wstat, _wstat32, _wstat64, _wstati64, _wstat32i64, _wstat64i32
파일의 상태 정보를 가져옵니다.  
  
## <a name="syntax"></a>구문  
  
```  
int _stat(  
   const char *path,  
   struct _stat *buffer   
);  
int _stat32(  
   const char *path,  
   struct __stat32 *buffer   
);  
int _stat64(  
   const char *path,  
   struct __stat64 *buffer   
);  
int _stati64(  
   const char *path,  
   struct _stati64 *buffer   
);  
int _stat32i64(  
   const char *path,  
   struct _stat32i64 *buffer   
);  
int _stat64i32(  
   const char *path,  
   struct _stat64i32 *buffer   
);  
int _wstat(  
   const wchar_t *path,  
   struct _stat *buffer   
);  
int _wstat32(  
   const wchar_t *path,  
   struct __stat32 *buffer   
);  
int _wstat64(  
   const wchar_t *path,  
   struct __stat64 *buffer   
);  
int _wstati64(  
   const wchar_t *path,  
   struct _stati64 *buffer   
);  
int _wstat32i64(  
   const wchar_t *path,  
   struct _stat32i64 *buffer   
);  
int _wstat64i32(  
   const wchar_t *path,  
   struct _stat64i32 *buffer   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `path`  
 기존 파일 또는 디렉터리의 경로가 포함된 문자열에 대한 포인터입니다.  
  
 `buffer`  
 결과를 저장하는 구조에 대한 포인터입니다.  
  
## <a name="return-value"></a>반환 값  
 파일 상태 정보를 가져오는 경우 이러한 함수는 각각 0을 반환합니다. 반환 값이-1은 오류를 나타내며이 경우 `errno` 로 설정 된 `ENOENT`는 파일 이름 또는 경로 수 찾을 수 없음을 나타냅니다. `EINVAL` 의 반환 값은 잘못된 매개 변수를 나타냅니다. 또한 이 경우 `errno` 는 `EINVAL` 로 설정됩니다.  
  
 이러한 반환 코드 및 기타 반환 코드에 대한 자세한 내용은 [_doserrno, errno, _sys_errlist 및 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md) 을 참조하세요.  
  
 `_stat32` 또는 `_wstat32`를 사용하지 않거나 `_USE_32BIT_TIME_T`를 정의(이 경우 날짜는 UTC 시간 2038년 1월 18일 23:59:59까지만 표시될 수 있음)하지 않는 한, 파일의 날짜 스탬프가 1970년 1월 1일 자정 이후이고 3000년 12월 31일 23:59:59 이전인 경우 표시될 수 있습니다.  
  
## <a name="remarks"></a>설명  
 `_stat` 함수는 `path` 에서 지정한 파일 또는 디렉터리에 대한 정보를 가져와 `buffer`에서 가리키는 구조에 저장합니다. `_stat` 는 현재 사용 중인 멀티바이트 코드 페이지에 따라 멀티바이트 문자 시퀀스를 인식하며 멀티바이트 문자열 인수를 자동으로 적절히 처리합니다.  
  
 `_wstat` 은 `_stat`의 와이드 문자 버전이며, `path` 에 대한 `_wstat` 인수는 와이드 문자열입니다. `_wstat` 및 `_stat` 는 동일하게 작동합니다. 단, `_wstat` 는 멀티바이트 문자열을 처리하지 않습니다.  
  
 이러한 함수의 변형은 32비트 또는 64비트 시간 형식 및 32비트 또는 64비트 파일 길이를 지원합니다. 첫 번째 숫자 접미사(`32` 또는 `64`)는 사용된 시간 형식의 크기를 나타내며, 두 번째 접미사( `i32` 또는 `i64`)는 파일 크기가 32비트 정수로 표시되는지 아니면 64비트 정수로 표시되는지를 나타냅니다.  
  
 `_stat`는 `_stat64i32`와 동일하며, `struct _stat`는 64비트 시간을 포함합니다. `_USE_32BIT_TIME_T` 가 정의되지 않는 한 그러하며, 이 경우 이전 동작이 적용됩니다. `_stat` 는 32비트 시간을 사용하고 `struct _stat` 는 32비트 시간을 포함합니다. 이는 `_stati64`의 경우에도 마찬가지입니다.  
  
> [!NOTE]
>  `_wstat`는 [!INCLUDE[wiprlhext](../../c-runtime-library/reference/includes/wiprlhext_md.md)] 바로 가기 링크에서 작동하지 않습니다. 이러한 경우 `_wstat` 는 항상 0의 파일 크기를 보고합니다. `_stat` 는 바로 가기 링크와 제대로 작동합니다.  
  
 이 함수는 해당 매개 변수의 유효성을 검사합니다. `path` 또는 `buffer`가 `NULL`인 경우 [매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md)에 설명된 대로 잘못된 매개 변수 처리기가 호출됩니다.  
  
### <a name="time-type-and-file-length-type-variations-of-stat"></a>_stat의 시간 형식 및 파일 길이 형식 변형  
  
|함수|_USE_32BIT_TIME_T 정의 여부|시간 형식|파일 길이 형식|  
|---------------|------------------------------------|---------------|----------------------|  
|`_stat`, `_wstat`|정의되지 않음|64비트|32비트|  
|`_stat`, `_wstat`|정의됨|32비트|32비트|  
|`_stat32`, `_wstat32`|매크로 정의의 영향을 받지 않음|32비트|32비트|  
|`_stat64`, `_wstat64`|매크로 정의의 영향을 받지 않음|64비트|64비트|  
|`_stati64`, `_wstati64`|정의되지 않음|64비트|64비트|  
|`_stati64`, `_wstati64`|정의됨|32비트|64비트|  
|`_stat32i64`, `_wstat32i64`|매크로 정의의 영향을 받지 않음|32비트|64비트|  
|`_stat64i32`, `_wstat64i32`|매크로 정의의 영향을 받지 않음|64비트|32비트|  
  
### <a name="generic-text-routine-mappings"></a>제네릭 텍스트 루틴 매핑  
  
|TCHAR.H 루틴|_UNICODE 및 _MBCS 정의되지 않음|_MBCS 정의됨|_UNICODE 정의됨|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tstat`|`_stat`|`_stat`|`_wstat`|  
|`_tstat64`|`_stat64`|`_stat64`|`_wstat64`|  
|`_tstati64`|`_stati64`|`_stati64`|`_wstati64`|  
|`_tstat32i64`|`_stat32i64`|`_stat32i64`|`_wstat32i64`|  
|`_tstat64i32`|`_stat64i32`|`_stat64i32`|`_wstat64i32`|  
  
 SYS\STAT.H에 정의된 `_stat` 구조로, 다음 필드를 포함합니다.  
  
 `st_gid`  
 파일(UNIX 관련)을 소유하는 그룹의 숫자 식별자입니다. 이 필드는 Windows 시스템에서 항상 0입니다. 리디렉션된 파일은 Windows 파일로 분류됩니다.  
  
 `st_atime`  
 파일의 마지막 액세스 시간입니다. NTFS에서는 유효하지만, FAT로 포맷한 디스크 드라이브에서는 유효하지 않습니다.  
  
 `st_ctime`  
 파일 생성 시간입니다. NTFS에서는 유효하지만, FAT로 포맷한 디스크 드라이브에서는 유효하지 않습니다.  
  
 `st_dev`  
 파일이 포함된 디스크의 드라이브 번호( `st_rdev`와 동일)입니다.  
  
 `st_ino`  
 파일(UNIX 관련)의 정보 노드( `inode`) 수입니다. UNIX 파일 시스템에서 `inode` 는 파일 날짜 및 시간 스탬프, 권한, 내용 등을 설명합니다. 파일이 서로 하드 링크된 경우 동일한 `inode`를 공유합니다. 따라서 `inode`즉, `st_ino`는 FAT, HPFS 또는 NTFS 파일 시스템 간 차이가 무의미합니다.  
  
 `st_mode`  
 파일 모드 정보의 비트 마스크입니다. `_S_IFDIR` 에서 디렉터리를 지정한 경우 `path` 비트가 설정되며, `_S_IFREG` 에서 일반 파일 또는 장치를 지정한 경우 `path` 비트가 설정됩니다. 파일의 사용 권한 모드에 따라 사용자 읽기/쓰기 비트가 설정됩니다. 파일 이름 확장명에 따라 사용자 실행 비트가 설정됩니다.  
  
 `st_mtime`  
 파일의 마지막 수정 시간입니다.  
  
 `st_nlink`  
 NTFS가 아닌 파일 시스템에서 항상 1입니다.  
  
 `st_rdev`  
 파일이 포함된 디스크의 드라이브 번호( `st_dev`와 동일)입니다.  
  
 `st_size`  
 파일의 크기(바이트)입니다. 접미사가 `i64` 인 변형의 64비트 정수입니다**.**  
  
 `st_uid`  
 파일(UNIX 관련)을 소유하는 사용자의 숫자 식별자입니다. 이 필드는 Windows 시스템에서 항상 0입니다. 리디렉션된 파일은 Windows 파일로 분류됩니다.  
  
 `path` 에서 장치를 참조하는 경우 `st_size`구조의 `st_dev`, 다양한 시간 필드, `st_rdev` 및 `_stat` 필드는 의미가 없습니다. STAT.H는 TYPES.H에 정의된 [_dev_t](../../c-runtime-library/standard-types.md) 형식을 사용하므로 코드에서 STAT.H 앞에 TYPES.H를 포함해야 합니다.  
  
## <a name="requirements"></a>요구 사항  
  
|루틴에서 반환된 값|필수 헤더|선택적 헤더|  
|-------------|---------------------|----------------------|  
|`_stat`, `_stat32`, `_stat64`, `_stati64`, `_stat32i64`, `_stat64i32`|\<sys/types.h> 다음에 \<sys/stat.h>|\<errno.h>|  
|`_wstat`, `_wstat32`, `_wstat64`, `_wstati64`, `_wstat32i64`, `_wstat64i32`|\<sys/types.h> 다음에 \<sys/stat.h> 또는 \<wchar.h>|\<errno.h>|  
  
 호환성에 대한 자세한 내용은 소개 단원의 [호환성](../../c-runtime-library/compatibility.md) 부분을 참조하십시오.  
  
## <a name="example"></a>예  
  
```  
// crt_stat.c  
// This program uses the _stat function to  
// report information about the file named crt_stat.c.  
  
#include <time.h>  
#include <sys/types.h>  
#include <sys/stat.h>  
#include <stdio.h>  
#include <errno.h>  
  
int main( void )  
{  
   struct _stat buf;  
   int result;  
   char timebuf[26];  
   char* filename = "crt_stat.c";  
   errno_t err;  
  
   // Get data associated with "crt_stat.c":   
   result = _stat( filename, &buf );  
  
   // Check if statistics are valid:   
   if( result != 0 )  
   {  
      perror( "Problem getting information" );  
      switch (errno)  
      {  
         case ENOENT:  
           printf("File %s not found.\n", filename);  
           break;  
         case EINVAL:  
           printf("Invalid parameter to _stat.\n");  
           break;  
         default:  
           /* Should never be reached. */  
           printf("Unexpected error in _stat.\n");  
      }  
   }  
   else  
   {  
      // Output some of the statistics:   
      printf( "File size     : %ld\n", buf.st_size );  
      printf( "Drive         : %c:\n", buf.st_dev + 'A' );  
      err = ctime_s(timebuf, 26, &buf.st_mtime);  
      if (err)  
      {  
         printf("Invalid arguments to ctime_s.");  
         exit(1);  
      }  
      printf( "Time modified : %s", timebuf );  
   }  
}  
```  
  
```Output  
File size     : 732  
Drive         : C:  
Time modified : Thu Feb 07 14:39:36 2002  
```  
  
## <a name="see-also"></a>참고 항목  
 [파일 처리](../../c-runtime-library/file-handling.md)   
 [_access, _waccess](../../c-runtime-library/reference/access-waccess.md)   
 [_fstat, _fstat32, _fstat64, _fstati64, _fstat32i64, _fstat64i32](../../c-runtime-library/reference/fstat-fstat32-fstat64-fstati64-fstat32i64-fstat64i32.md)   
 [_getmbcp](../../c-runtime-library/reference/getmbcp.md)   
 [_setmbcp](../../c-runtime-library/reference/setmbcp.md)