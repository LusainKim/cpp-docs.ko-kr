---
title: "freopen, _wfreopen | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname:
- freopen
- _wfreopen
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
- api-ms-win-crt-stdio-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- _wfreopen
- _tfreopen
- freopen
dev_langs: C++
helpviewer_keywords:
- _wfreopen function
- file pointers [C++], reassigning
- _tfreopen function
- freopen function
- tfreopen function
- wfreopen function
ms.assetid: de4b73f8-1043-4d62-98ee-30d2022da885
caps.latest.revision: "27"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: d3eb18b70ea672b095dc6d24dfd45e1bdda8f88b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="freopen-wfreopen"></a>freopen, _wfreopen
파일 포인터를 다시 할당합니다. 이러한 함수의 더 안전한 버전을 사용할 수 있습니다. [freopen_s, _wfreopen_s](../../c-runtime-library/reference/freopen-s-wfreopen-s.md)를 참조하세요.  
  
## <a name="syntax"></a>구문  
  
```  
FILE *freopen(   
   const char *path,  
   const char *mode,  
   FILE *stream   
);  
FILE *_wfreopen(   
   const wchar_t *path,  
   const wchar_t *mode,  
   FILE *stream   
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `path`  
 새 파일의 경로입니다.  
  
 `mode`  
 허용되는 액세스 형식입니다.  
  
 `stream`  
 `FILE` 구조체에 대한 포인터입니다.  
  
## <a name="return-value"></a>반환 값  
 각 함수는 새로 열린 파일에 대한 포인터를 반환합니다. 오류가 발생하면 원래 파일이 닫히고 함수에서 `NULL` 포인터 값을 반환합니다. `path`, `mode` 또는 `stream`이 null 포인터이거나 `filename`이 빈 문자열인 경우 이러한 함수는 [매개 변수 유효성 검사](../../c-runtime-library/parameter-validation.md)에 설명된 대로 잘못된 매개 변수 처리기를 호출합니다. 계속해서 실행하도록 허용된 경우 이러한 함수는 `errno`를 `EINVAL`로 설정하고 `NULL`을 반환합니다.  
  
 이러한 오류 코드 및 기타 오류 코드에 대한 자세한 내용은 [_doserrno, errno, _sys_errlist 및 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)를 참조하세요.  
  
## <a name="remarks"></a>설명  
 이러한 함수의 더 안전한 버전이 있습니다. [freopen_s, _wfreopen_s](../../c-runtime-library/reference/freopen-s-wfreopen-s.md)를 참조하세요.  
  
 `freopen` 함수는 현재 연결 된 파일을 닫습니다 `stream` 재지정 `stream` 로 지정 된 파일에 `path`합니다. `_wfreopen`은 와이드 문자 버전의 `_freopen`이며, `_wfreopen`에 대한 `path` 및 `mode` 인수는 와이드 문자열입니다. 그렇지 않으면 `_wfreopen`과 `_freopen`이 동일하게 작동합니다.  
  
### <a name="generic-text-routine-mappings"></a>제네릭 텍스트 루틴 매핑  
  
|TCHAR.H 루틴|_UNICODE 및 _MBCS 정의되지 않음|_MBCS 정의됨|_UNICODE 정의됨|  
|---------------------|------------------------------------|--------------------|-----------------------|  
|`_tfreopen`|`freopen`|`freopen`|`_wfreopen`|  
  
 `freopen`은 보통 미리 열린 `stdin`, `stdout` 및 `stderr` 파일을 사용자가 지정한 파일로 리디렉션하는 데 사용됩니다. 와 연결 된 새 파일 `stream` 으로 연 `mode`이며 다음과 같이 파일에 대해 요청 된 액세스 형식을 지정 하는 문자 문자열:  
  
 `"r"`  
 읽기 위해 엽니다. 파일이 없거나 찾을 수 없는 경우 `freopen` 호출이 실패합니다.  
  
 `"w"`  
 쓰기 위해 빈 파일을 엽니다. 지정한 파일이 있으면 이 파일의 내용은 삭제됩니다.  
  
 `"a"`  
 새 데이터를 파일에 쓰기 전에 EOF(파일 끝) 표식을 제거하지 않고 파일의 끝에 쓰기(추가)하기 위해 엽니다. 존재하지 않을 경우 먼저 파일을 만듭니다.  
  
 `"r+"`  
 읽고 쓰기 위해 엽니다. 파일이 있어야 합니다.  
  
 `"w+"`  
 읽고 쓰기 위해 빈 파일을 엽니다. 지정한 파일이 있으면 이 파일의 내용은 삭제됩니다.  
  
 `"a+"`  
 읽고 추가하기 위해 엽니다. 추가 작업에는 새 데이터를 파일에 쓰기 전에 EOF 표식을 제거하는 작업이 포함되고 EOF 표식은 쓰기가 완료된 후 복원됩니다. 존재하지 않을 경우 먼저 파일을 만듭니다.  
  
 `"w"` 및 `"w+"` 형식은 기존 파일을 삭제할 수 있으므로 이 형식을 사용할 때는 주의합니다.  
  
 파일이 `"a"` 또는 `"a+"` 액세스 형식으로 열려 있으면 모든 쓰기 작업이 파일 끝에서 발생합니다. `fseek` 또는 `rewind`를 사용하여 파일 포인터의 위치를 변경할 수 있지만, 파일 포인터는 쓰기 작업을 수행하기 전에 항상 파일 끝으로 다시 이동합니다. 따라서 기존 데이터를 덮어쓸 수 없습니다.  
  
 `"a"` 모드에서는 파일에 추가하기 전에 EOF 표식을 제거하지 않습니다. 추가 작업이 수행된 이후에는 MS-DOS TYPE 명령은 원래 EOF 표식까지만 데이터를 표시하고 파일에 추가된 데이터는 표시하지 않습니다. `"a+"` 모드에서는 파일에 추가하기 전에 EOF 표식을 제거합니다. 추가 후에는 MS-DOS TYPE 명령으로 파일의 모든 데이터를 표시합니다. `"a+"` 모드에서는 Ctrl+Z EOF 표식으로 종료되는 스트림 파일에 추가해야 합니다.  
  
 `"r+"`, `"w+"` 또는 `"a+"` 액세스 형식을 지정한 경우 읽기와 쓰기가 모두 허용됩니다. 즉, 파일이 "업데이트"용으로 열립니다. 그러나 읽기와 쓰기를 전환할 때는 먼저 [fsetpos](../../c-runtime-library/reference/fsetpos.md), [fseek](../../c-runtime-library/reference/fseek-fseeki64.md) 또는 [rewind](../../c-runtime-library/reference/rewind.md) 작업이 있어야 합니다. 원하는 경우 `fsetpos` 또는 `fseek` 작업에 대한 현재 위치를 지정할 수 있습니다. 위의 값 외에도, 다음 문자 중 하나를 `mode` 문자열에 포함하여 새 줄에 대해 변환 모드를 지정할 수 있습니다.  
  
 `t`  
 텍스트에서 열기 (변환 됨) 모드입니다. 캐리지 리턴-줄 바꿈 (CR-LF) 조합은 입력에서 단일 줄 바꿈 (LF) 문자로 변환 됩니다. LF 문자는 출력 시 CR-LF 조합으로 변환 합니다. 또한 CTRL+Z는 입력 시 파일 끝 문자로 변환됩니다. `"a+"`를 통해 읽기용으로나 쓰기 및 읽기용으로 열려 있는 파일에서 런타임 라이브러리는 파일 끝에 Ctrl+Z가 있는지 확인하고 가능한 경우 이를 제거합니다. 이렇게 처리되는 이유는 `fseek` 및 `ftell`을 사용하여 파일 내에서 이동하면 `fseek`가 파일 끝 부분에서 제대로 동작하지 않을 수 있기 때문입니다. `t` 옵션은 ANSI 포팅 기능을 원할 경우 사용하면 안 되는 Microsoft 확장입니다.  
  
 `b`  
 이진(변환되지 않음) 모드로 엽니다. 위에서 설명한 변환은 표시되지 않습니다.  
  
 `t` 또는 `b` 가 `mode`에 지정되지 않은 경우, 기본 변환 모드는 전역 변수 [_fmode](../../c-runtime-library/fmode.md)로 정의됩니다. `t` 또는 `b` 가 인수에 접두어로 추가되면 이 함수는 실행되지 못하고 `NULL`을 반환합니다.  
  
 텍스트 모드와 이진 모드에 대한 자세한 내용은 [텍스트 및 이진 모드 파일 I/O](../../c-runtime-library/text-and-binary-mode-file-i-o.md)를 참조하세요.  
  
## <a name="requirements"></a>요구 사항  
  
|함수|필수 헤더|  
|--------------|---------------------|  
|`freopen`|\<stdio.h>|  
|`_wfreopen`|\<stdio.h> 또는 \<wchar.h>|  
  
 콘솔은 [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)] 응용 프로그램에서 지원되지 않습니다. 콘솔에 연결된 표준 스트림 핸들 `stdin`, `stdout` 및 `stderr`은 [!INCLUDE[win8_appname_long](../../build/includes/win8_appname_long_md.md)] 앱의 C 런타임 함수에서 사용되기 전에 리디렉션되어야 합니다. 호환성에 대한 자세한 내용은 [호환성](../../c-runtime-library/compatibility.md)을 참조하세요.  
  
## <a name="example"></a>예  
  
```  
// crt_freopen.c  
// compile with: /W3  
// This program reassigns stderr to the file  
// named FREOPEN.OUT and writes a line to that file.  
#include <stdio.h>  
#include <stdlib.h>  
  
FILE *stream;  
  
int main( void )  
{  
   // Reassign "stderr" to "freopen.out":   
   stream = freopen( "freopen.out", "w", stderr ); // C4996  
   // Note: freopen is deprecated; consider using freopen_s instead  
  
   if( stream == NULL )  
      fprintf( stdout, "error on freopen\n" );  
   else  
   {  
      fprintf( stdout, "successfully reassigned\n" ); fflush( stdout );  
      fprintf( stream, "This will go to the file 'freopen.out'\n" );  
      fclose( stream );  
   }  
   system( "type freopen.out" );  
}  
```  
  
```Output  
successfully reassigned  
This will go to the file 'freopen.out'  
```  
  
## <a name="see-also"></a>참고 항목  
 [스트림 I/O](../../c-runtime-library/stream-i-o.md)   
 [fclose, _fcloseall](../../c-runtime-library/reference/fclose-fcloseall.md)   
 [_fdopen, _wfdopen](../../c-runtime-library/reference/fdopen-wfdopen.md)   
 [_fileno](../../c-runtime-library/reference/fileno.md)   
 [fopen, _wfopen](../../c-runtime-library/reference/fopen-wfopen.md)   
 [_open, _wopen](../../c-runtime-library/reference/open-wopen.md)   
 [_setmode](../../c-runtime-library/reference/setmode.md)