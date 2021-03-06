---
title: "ios_base 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- xiosbase/std::ios_base
- ios/std::ios_base::event_callback
- xiosbase/std::ios_base::fmtflags
- xiosbase/std::ios_base::iostate
- xiosbase/std::ios_base::openmode
- xiosbase/std::ios_base::seekdir
- xiosbase/std::ios_base::event
- xiosbase/std::ios_base::adjustfield
- xiosbase/std::ios_base::app
- xiosbase/std::ios_base::ate
- xiosbase/std::ios_base::badbit
- xiosbase/std::ios_base::basefield
- xiosbase/std::ios_base::beg
- xiosbase/std::ios_base::binary
- xiosbase/std::ios_base::boolalpha
- xiosbase/std::ios_base::cur
- xiosbase/std::ios_base::dec
- xiosbase/std::ios_base::end
- xiosbase/std::ios_base::eofbit
- xiosbase/std::ios_base::failbit
- xiosbase/std::ios_base::fixed
- xiosbase/std::ios_base::floatfield
- xiosbase/std::ios_base::goodbit
- xiosbase/std::ios_base::hex
- xiosbase/std::ios_base::in
- xiosbase/std::ios_base::internal
- xiosbase/std::ios_base::left
- xiosbase/std::ios_base::oct
- xiosbase/std::ios_base::out
- xiosbase/std::ios_base::right
- xiosbase/std::ios_base::scientific
- xiosbase/std::ios_base::showbase
- xiosbase/std::ios_base::showpoint
- xiosbase/std::ios_base::showpos
- xiosbase/std::ios_base::skipws
- xiosbase/std::ios_base::trunc
- xiosbase/std::ios_base::unitbuf
- xiosbase/std::ios_base::uppercase
- xiosbase/std::ios_base::failure
- xiosbase/std::ios_base::flags
- xiosbase/std::ios_base::getloc
- xiosbase/std::ios_base::imbue
- xiosbase/std::ios_base::Init
- xiosbase/std::ios_base::iword
- xiosbase/std::ios_base::precision
- xiosbase/std::ios_base::pword
- ios/std::ios_base::register_callback
- xiosbase/std::ios_base::setf
- xiosbase/std::ios_base::sync_with_stdio
- xiosbase/std::ios_base::unsetf
- xiosbase/std::ios_base::width
- xiosbase/std::ios_base::xalloc
dev_langs: C++
helpviewer_keywords:
- std::ios_base [C++]
- std::ios_base [C++], event_callback
- std::ios_base [C++], fmtflags
- std::ios_base [C++], iostate
- std::ios_base [C++], openmode
- std::ios_base [C++], seekdir
- std::ios_base [C++], event
- std::ios_base [C++], adjustfield
- std::ios_base [C++], app
- std::ios_base [C++], ate
- std::ios_base [C++], badbit
- std::ios_base [C++], basefield
- std::ios_base [C++], beg
- std::ios_base [C++], binary
- std::ios_base [C++], boolalpha
- std::ios_base [C++], cur
- std::ios_base [C++], dec
- std::ios_base [C++], end
- std::ios_base [C++], eofbit
- std::ios_base [C++], failbit
- std::ios_base [C++], fixed
- std::ios_base [C++], floatfield
- std::ios_base [C++], goodbit
- std::ios_base [C++], hex
- std::ios_base [C++], in
- std::ios_base [C++], internal
- std::ios_base [C++], left
- std::ios_base [C++], oct
- std::ios_base [C++], out
- std::ios_base [C++], right
- std::ios_base [C++], scientific
- std::ios_base [C++], showbase
- std::ios_base [C++], showpoint
- std::ios_base [C++], showpos
- std::ios_base [C++], skipws
- std::ios_base [C++], trunc
- std::ios_base [C++], unitbuf
- std::ios_base [C++], uppercase
- std::ios_base [C++], failure
- std::ios_base [C++], flags
- std::ios_base [C++], getloc
- std::ios_base [C++], imbue
- std::ios_base [C++], Init
- std::ios_base [C++], iword
- std::ios_base [C++], precision
- std::ios_base [C++], pword
- std::ios_base [C++], register_callback
- std::ios_base [C++], setf
- std::ios_base [C++], sync_with_stdio
- std::ios_base [C++], unsetf
- std::ios_base [C++], width
- std::ios_base [C++], xalloc
ms.assetid: 0f9e0abc-f70f-49bc-aa1f-003859f56cfe
caps.latest.revision: "21"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 39098fc501ba94c4fa2cd6cf779e7c5c71cc2f1d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="iosbase-class"></a>ios_base 클래스
이 클래스는 템플릿 매개 변수에 따라 달라지지 않는 입력 및 출력 스트림에 공통된 저장소 및 멤버 함수를 설명합니다. (템플릿 클래스 [basic_ios](../standard-library/basic-ios-class.md)는 공통된 항목과 템플릿 매개 변수에 따라 달라지는 항목에 대해 설명합니다.)  
  
 Ios_base 클래스의 개체는 다음 항목으로 구성되는 형식 지정 정보를 저장합니다.  
  
-   [fmtflags](#fmtflags) 형식의 개체에 있는 형식 플래그.  
  
-   [iostate](#iostate) 형식의 개체에 있는 예외 마스크.  
  
-   형식의 개체에 있는 필드 너비 `int`합니다.  
  
-   `int` 형식의 개체에 있는 표시 자릿수.  
  
-   **locale** 형식의 개체에 있는 로캘 개체.  
  
-   **long** 형식의 요소와 `void` 포인터가 있는 두 개의 확장 가능한 배열.  
  
 ios_base 클래스의 개체는 [iostate](#iostate) 형식의 개체에 스트림 상태 정보와 콜백 스택도 저장합니다.  
  
### <a name="constructors"></a>생성자  
  
|||  
|-|-|  
|[ios_base](#ios_base)|`ios_base` 개체를 생성합니다.|  
  
### <a name="typedefs"></a>형식 정의  
  
|||  
|-|-|  
|[event_callback](#event_callback)|[register_call](#register_callback)에 전달된 함수에 대해 설명합니다.|  
|[fmtflags](#fmtflags)|출력의 모양을 지정하는 상수입니다.|  
|[iostate](#iostate)|스트림의 상태를 설명하는 상수를 정의합니다.|  
|[openmode](#openmode)|스트림과 상호 작용하는 방법을 설명합니다.|  
|[seekdir](#seekdir)|오프셋 작업에 대한 시작 지점을 지정합니다.|  
  
### <a name="enums"></a>열거형  
  
|||  
|-|-|  
|[event](#event)|이벤트 유형을 지정합니다.|  
  
### <a name="constants"></a>상수  
  
|||  
|-|-|  
|[adjustfield](#fmtflags)|`internal` &#124; `left` &#124; `right`로 정의된 비트 마스크입니다.|  
|[app](#openmode)|각 삽입 전에 스트림의 끝에 검색을 지정합니다.|  
|[ate](#openmode)|해당 제어 개체를 처음 만들 때 스트림의 끝에 검색을 지정합니다.|  
|[badbit](#iostate)|스트림 버퍼의 무결성 손실을 기록합니다.|  
|[basefield](#fmtflags)|`dec` &#124; `hex` &#124; `oct`로 정의된 비트 마스크입니다.|  
|[beg](#seekdir)|시퀀스의 시작을 기준으로 한 검색을 지정합니다.|  
|[binary](#openmode)|파일을 텍스트 스트림이 아니라 이진 스트림으로 읽도록 지정합니다.|  
|[boolalpha](#fmtflags)|숫자 값이 아닌 이름(예: `true` 및 `false`)으로서 `bool` 형식의 개체를 삽입 또는 추출하도록 지정합니다.|  
|[cur](#seekdir)|시퀀스 내에서 현재 위치를 기준으로 하는 검색을 지정합니다.|  
|[dec](#fmtflags)|10진수 형식의 정수 값을 삽입 또는 추출하도록 지정합니다.|  
|[end](#seekdir)|시퀀스의 끝을 기준으로 한 검색을 지정합니다.|  
|[eofbit](#iostate)|스트림에서 추출할 때 파일 끝을 기록합니다.|  
|[failbit](#iostate)|스트림에서 유효한 필드를 추출하지 못하는 경우를 기록합니다.|  
|[fixed](#fmtflags)|고정 소수점 형식(지수 필드 없음)의 부동 소수점 값을 삽입하도록 지정합니다.|  
|[floatfield](#fmtflags)|`fixed` &#124; `scientific`으로 정의된 비트 마스크입니다.|  
|[goodbit](#iostate)|모든 상태 비트를 지웁니다.|  
|[hex](#fmtflags)|16진수 형식의 정수 값을 삽입 또는 추출하도록 지정합니다.|  
|[in](#openmode)|스트림에서 추출하도록 지정합니다.|  
|[internal](#fmtflags)|생성된 숫자 필드의 내부에 있는 점에서 채우기 문자를 삽입하여 필드 너비를 채웁니다.|  
|[left](#fmtflags)|왼쪽 맞춤을 지정합니다.|  
|[oct](#fmtflags)|8진수 형식의 정수 값을 삽입 또는 추출하도록 지정합니다.|  
|[out](#openmode)|스트림에 삽입하도록 지정합니다.|  
|[right](#fmtflags)|오른쪽 맞춤을 지정합니다.|  
|[scientific](#fmtflags)|공학용 형식(지수 필드 사용)의 부동 소수점 값을 삽입하도록 지정합니다.|  
|[showbase](#fmtflags)|생성된 정수 필드의 기수를 표시하는 접두사를 삽입하도록 지정합니다.|  
|[showpoint](#fmtflags)|생성된 부동 소수점 필드에서 소수점을 무조건 삽입하도록 지정합니다.|  
|[showpos](#fmtflags)|생성된 음수가 아닌 숫자 필드에 더하기 기호를 삽입하도록 지정합니다.|  
|[skipws](#fmtflags)|특정 추출 전에 선행 공백은 건너뛰도록 지정합니다.|  
|[trunc](#openmode)|해당 제어 개체가 만들어지면 기존 파일의 콘텐츠를 삭제하도록 지정합니다.|  
|[unitbuf](#fmtflags)|각 삽입 후 출력이 플러시되도록 합니다.|  
|[uppercase](#fmtflags)|특정 삽입의 소문자에 해당하는 대문자를 삽입하도록 지정합니다.|  
  
### <a name="member-functions"></a>멤버 함수  
  
|||  
|-|-|  
|[failure](#failure)|멤버 클래스는 템플릿 클래스 [basic_ios](../standard-library/basic-ios-class.md)에서 멤버 함수 [clear](../standard-library/basic-ios-class.md#clear)에 의해 throw된 모든 예외에 대한 기본 클래스로 사용됩니다.|  
|[flags](#flags)|현재 플래그 설정을 설정하거나 반환합니다.|  
|[getloc](#getloc)|저장된 로캘 개체를 반환합니다.|  
|[imbue](#imbue)|로캘을 변경합니다.|  
|[Init](#init)|생성될 때 표준 iostream 개체를 만듭니다.|  
|[iword](#iword)|`iword`로 저장할 수 있는 값을 할당합니다.|  
|[precision](#precision)|부동 소수점 숫자에 표시할 자릿수를 지정합니다.|  
|[pword](#pword)|`pword`로 저장할 수 있는 값을 할당합니다.|  
|[register_callback](#register_callback)|콜백 함수를 지정합니다.|  
|[setf](#setf)|지정된 플래그를 설정합니다.|  
|[sync_with_stdio](#sync_with_stdio)|iostream 및 C 런타임 라이브러리 작업이 소스 코드에 표시되는 순서로 수행되도록 합니다.|  
|[unsetf](#unsetf)|지정된 플래그가 해제되도록 합니다.|  
|[width](#width)|출력 스트림의 길이를 설정합니다.|  
|[xalloc](#xalloc)|변수가 스트림에 포함된다고 지정합니다.|  
  
### <a name="operators"></a>연산자  
  
|||  
|-|-|  
|[operator=](#op_eq)|`ios_base` 개체에 사용할 대입 연산자입니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<ios>  
  
 **네임스페이스:** std  
  
##  <a name="event"></a>  ios_base::event  
 이벤트 유형을 지정합니다.  
  
```  
enum event {
    erase_event,
    imbue_event,
    copyfmt_event};  
```  
  
### <a name="remarks"></a>설명  
 이 형식은 [register_callback](#register_callback)에 등록된 함수의 인수로 사용되는 콜백 이벤트를 저장할 수 있는 개체에 대해 설명하는 열거 형식입니다. 고유 이벤트 값은 다음과 같습니다.  
  
- **copyfmt_event** - [copyfmt](../standard-library/basic-ios-class.md#copyfmt) 호출이 거의 끝나고 [예외 마스크](../standard-library/ios-base-class.md)가 복사되기 바로 전에 발생하는 콜백을 식별합니다.  
  
- **erase_event** - [copyfmt](../standard-library/basic-ios-class.md#copyfmt) 호출이 시작될 때 또는 **\*this**에 대한 소멸자 호출이 시작될 때 발생하는 콜백을 식별합니다.  
  
- **imbue_event**- [imbue](#imbue) 호출이 끝나고 함수가 반환되기 바로 전에 발생하는 콜백을 식별합니다.  
  
### <a name="example"></a>예  
  
  예제는 [register_callback](#register_callback)을 참조하세요.  
  
##  <a name="event_callback"></a>  ios_base::event_callback  

 [register_call](#register_callback)에 전달된 함수에 대해 설명합니다.  
  
```  
typedef void (__cdecl *event_callback)(
    event _E,  
    ios_base& _Base,  
    int _I);
```  
  
### <a name="parameters"></a>매개 변수  
 *_E*  
 [이벤트](#event)입니다.  
  
 `_Base`  
 이벤트가 호출된 스트림입니다.  
  
 *_I*  
 사용자 정의 숫자입니다.  
  
### <a name="remarks"></a>설명  
  
 이 형식은 [register_callback](#register_callback)에 등록할 수 있는 함수에 대한 포인터를 설명합니다. 이러한 형식의 함수는 예외를 throw하면 안 됩니다.  
  
### <a name="example"></a>예  
  
  `event_callback`을 사용하는 예제는 [register_call](#register_callback)을 참조하세요.  
  
##  <a name="failure"></a>  ios_base::failure  
  
 `failure` 클래스는 예외로 throw된 모든 개체의 형식에 대한 기본 클래스를 `iostreams` 라이브러리의 함수별로 정의하여 스트림 버퍼 작업 중 검색된 오류를 보고합니다.  
  
```  
namespace std {  
    class failure : public system_error {  
    public:  
        explicit failure(
            const string& _Message,  
            const error_code& _Code = io_errc::stream);

        explicit failure(
            const char* str,  
            const error_code& _Code = io_errc::stream);
    };
}  
```  
  
### <a name="remarks"></a>설명  

 `what()`에서 반환된 값은 `_Message`의 복사본이며, `_Code`에 기반한 테스트로 확대될 수 있습니다. `_Code`를 지정하지 않은 경우 `make_error_code(io_errc::stream)`가 기본값입니다.  
  
### <a name="example"></a>예  
  
```cpp  
// ios_base_failure.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )  
{  
    using namespace std;  
    fstream file;  
    file.exceptions(ios::failbit);  
    try  
    {  
        file.open( "rm.txt", ios_base::in );  
        // Opens nonexistent file for reading  
    }  
    catch( ios_base::failure f )  
    {  
        cout << "Caught an exception: " << f.what() << endl;  
    }  
}  
```  
  
```Output  
Caught an exception: ios_base::failbit set  
```  
  
##  <a name="flags"></a>  ios_base::flags  
  
 현재 플래그 설정을 설정하거나 반환합니다.  
  
```  
fmtflags flags() const;
fmtflags flags(fmtflags fmtfl);
```  
  
### <a name="parameters"></a>매개 변수  
 `fmtfl`  
 새 `fmtflags` 설정입니다.  
  
### <a name="return-value"></a>반환 값  
  
 이전 또는 현재 `fmtflags` 설정입니다.  
  
### <a name="remarks"></a>설명  
  
 플래그 목록은 [ios_base:: fmtflags](#fmtflags)를 참조하세요.  
  
 첫 번째 멤버 함수는 저장된 형식 플래그를 반환합니다. 두 번째 멤버 함수는 `fmtfl`을 형식 플래그에 저장하고 이전에 저장된 값을 반환합니다.  
  
### <a name="example"></a>예  
  
```cpp  
// ios_base_flags.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )  
{  
    using namespace std;  
    cout << cout.flags( ) << endl;  
    cout.flags( ios::dec | ios::boolalpha );  
    cout << cout.flags( );  
}    
```  
  
```Output  
513  
16896  
```  
  
##  <a name="fmtflags"></a>  ios_base::fmtflags  
  
 출력의 모양을 지정하는 상수입니다.  
  
```
class ios_base {  
public:  
   typedef implementation-defined-bitmask-type fmtflags;  
   static const fmtflags boolalpha;  
   static const fmtflags dec;  
   static const fmtflags fixed;  
   static const fmtflags hex;  
   static const fmtflags internal;  
   static const fmtflags left;  
   static const fmtflags oct;  
   static const fmtflags right;  
   static const fmtflags scientific;  
   static const fmtflags showbase;  
   static const fmtflags showpoint;  
   static const fmtflags showpos;  
   static const fmtflags skipws;  
   static const fmtflags unitbuf;  
   static const fmtflags uppercase;  
   static const fmtflags adjustfield;  
   static const fmtflags basefield;  
   static const fmtflags floatfield;  
   // ...  
};  
```  
  
### <a name="remarks"></a>설명  
  
 [ios](../standard-library/ios.md)에서 조작자를 지원합니다.  
  
 형식은 서식 플래그를 저장할 수 있는 개체를 설명하는 비트 마스크 형식입니다. 고유 플래그 값(요소)은 다음과 같습니다.  
  
- `dec` - 10진수 형식의 정수 값을 삽입 또는 추출합니다.  
  
- `hex` - 16진수 형식의 정수 값을 삽입 또는 추출합니다.  
  
- `oct` - 18진수 형식의 정수 값을 삽입 또는 추출합니다.  
  
- `showbase` - 생성된 정수 필드의 기수를 표시하는 접두사를 삽입합니다.  
  
- `internal` - 생성된 숫자 필드의 내부에 있는 점에서 채우기 문자를 삽입하여 필요에 따라 필드 너비를 채웁니다. (필드 너비 설정에 대한 자세한 내용은 [setw](../standard-library/iomanip-functions.md#setw)를 참조하세요.)  
  
- `left` - 생성된 필드(왼쪽 맞춤)의 끝 부분에서 채우기 문자를 삽입하여 필요에 따라 필드 너비를 채웁니다.  
  
- `right` - 생성된 필드(오른쪽 맞춤)의 시작 부분에서 채우기 문자를 삽입하여 필요에 따라 필드 너비를 채웁니다.  
  
- `boolalpha` - 숫자 값이 아닌 이름(예: `true` 및 `false`)으로서 `bool` 형식의 개체를 삽입 또는 추출합니다.  
  
- `fixed` - 고정 소수점 형식(지수 필드 없음)의 부동 소수점 값을 삽입합니다.  
  
- `scientific` - 공학용 형식(지수 필드 사용)의 부동 소수점 값을 삽입합니다.  
  
- `showpoint` - 생성된 부동 소수점 필드에서 소수점을 무조건 삽입합니다.  
  
- `showpos` - 생성된 음수가 아닌 숫자 필드에 더하기 기호를 삽입합니다.  
  
- `skipws` - 특정 추출 전에 선행 공백을 건너뜁니다.  
  
- `unitbuf` - 각 삽입 후 출력을 플러시합니다.  
  
- `uppercase` - 특정 삽입의 소문자에 해당하는 대문자를 삽입합니다.  
  
 또한 다음 몇 개의 값이 유용합니다.  
  
- `adjustfield` - `internal` &#124; `left` &#124; `right`로 정의된 비트 마스크  
  
- `basefield` - `dec` &#124; `hex` &#124; `oct`로 정의됨  
  
- `floatfield` - `fixed` &#124; `scientific`으로 정의됨  
  
 이러한 형식 플래그를 수정하는 함수의 예는 [\<iomanip>](../standard-library/iomanip.md)를 참조하세요.  
  
##  <a name="getloc"></a>  ios_base::getloc  
  
 저장된 로캘 개체를 반환합니다.  
  
```  
locale getloc() const;
```  
  
### <a name="return-value"></a>반환 값  
  
 저장된 로캘 개체입니다.  
  
### <a name="example"></a>예  
  
```cpp  
// ios_base_getlock.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
    cout << cout.getloc( ).name( ).c_str( ) << endl;  
}  
```  
  
```Output  
C  
```  
  
##  <a name="imbue"></a>  ios_base::imbue  

 로캘을 변경합니다.  
  
```  
locale imbue(const locale& _Loc);
```  
  
### <a name="parameters"></a>매개 변수  
 `_Loc`  
 새 로캘 설정입니다.  
  
### <a name="return-value"></a>반환 값  
  
 이전 로캘입니다.  
  
### <a name="remarks"></a>설명  
  
 멤버 함수는 `_Loc`를 로캘 개체에 저장한 다음 콜백 이벤트 및 `imbue_event`를 보고합니다. 이전에 저장된 값을 반환합니다.  
  
### <a name="example"></a>예  
  
  샘플은 [basic_ios:: imbue](../standard-library/basic-ios-class.md#imbue)를 참조하세요.  
  
##  <a name="init"></a>  ios_base::Init  
  
 생성될 때 표준 iostream 개체를 만듭니다.  
  
```  
class Init { };  
```
  
### <a name="remarks"></a>설명  
  
 중첩 클래스는 임의의 정적 개체에 대한 생성자를 실행하기 전에도 생성을 통해 표준 iostreams 개체가 제대로 생성되도록 하는 개체에 대해 설명합니다.  
  
##  <a name="ios_base"></a>  ios_base::ios_base  
  
 ios_base 개체를 생성합니다.  
  
```  
ios_base();
```  
  
### <a name="remarks"></a>설명  
  
 (보호된) 생성자는 아무 작업도 수행하지 않습니다. 나중에 **basic_ios::**[init](../standard-library/basic-ios-class.md#init)를 호출할 경우 개체를 안전하게 삭제하려면 먼저 개체를 초기화해야 합니다. 따라서 ios_base 클래스를 안전하게 사용하려면 템플릿 클래스 [basic_ios](../standard-library/basic-ios-class.md)의 기본 클래스로 사용합니다.  
  
##  <a name="iostate"></a>  ios_base::iostate  
  
 스트림의 상태를 설명하는 상수의 형식입니다.  
  
```  
class ios_base {  
public:  
   typedef implementation-defined-bitmask-type iostate;  
   static const iostate badbit;  
   static const iostate eofbit;  
   static const iostate failbit;  
   static const iostate goodbit;  
   // ...  
};  
```  
  
### <a name="remarks"></a>설명  
  
 이 형식은 스트림 상태 정보를 저장할 수 있는 개체에 대해 설명하는 비트 마스크 형식입니다. 고유 플래그 값(요소)은 다음과 같습니다.  
  
- `badbit` - 스트림 버퍼의 무결성 손실을 기록합니다.  
  
- `eofbit` - 스트림에서 추출할 때 파일 끝을 기록합니다.  
  
- `failbit` - 스트림에서 유효한 필드를 추출하지 못하는 경우를 기록합니다.  
  
 또한 유용한 값은 `goodbit`입니다. 이때 앞에서 설명한 비트는 설정되지 않으며 `goodbit`는 0이 되도록 보장됩니다.  
  
##  <a name="iword"></a>  ios_base::iword  
  
 `iword`로 저장할 수 있는 값을 할당합니다.  
  
```  
long& iword(int idx);
```  
  
### <a name="parameters"></a>매개 변수  
 `idx`  
 `iword`로 저장할 값의 인덱스입니다.  
  
### <a name="remarks"></a>설명  
  
 멤버 함수는 **long** 형식의 요소와 함께 확장 가능한 배열의 `idx` 요소에 대한 참조를 반환합니다. 모든 요소는 효과적으로 존재하며 처음에는 0 값을 저장합니다. 반환된 참조는 개체에 대한 `iword`를 다음에 호출한 후, **basic_ios::**[copyfmt](../standard-library/basic-ios-class.md#copyfmt)를 호출하여 개체가 변경된 후 또는 개체가 삭제된 후에는 유효하지 않게 됩니다.  
  
 `idx`가 음수인 경우 또는 요소에 대해 고유한 저장소를 사용할 수 없는 경우 함수는 [setstate](../standard-library/basic-ios-class.md#setstate)**(badbit)**를 호출하고 고유하지 않을 수 있는 참조를 반환합니다.  
  
 `ios_base` 형식의 모든 개체에서 사용하도록 고유 인덱스를 가져오려면 [xalloc](#xalloc)를 호출합니다.  
  
### <a name="example"></a>예  
  
  `iword`를 사용하는 방법에 대한 샘플은 [xalloc](#xalloc)를 참조하세요.  
  
##  <a name="openmode"></a>  ios_base::openmode  
  
 스트림과 상호 작용하는 방법을 설명합니다.  
  
```  
class ios_base {  
public:  
   typedef implementation-defined-bitmask-type iostate;  
   static const iostate badbit;  
   static const iostate eofbit;  
   static const iostate failbit;  
   static const iostate goodbit;  
   // ...  
};  
```  
  
### <a name="remarks"></a>설명  
  
 이 형식은 여러 iostreams 개체에 대해 열기 모드를 저장할 수 있는 개체를 설명하는 `bitmask type`입니다. 고유 플래그 값(요소)은 다음과 같습니다.  
  
- **app** - 각 삽입 전에 스트림의 끝을 검색합니다.  
  
- **ate** -해당 제어 개체를 처음 만들 때 스트림의 끝을 검색합니다.  
  
- **binary** - 텍스트 스트림이 아니라 이진 스트림으로 파일을 읽습니다.  
  
- **in** - 스트림에서 추출을 허용합니다.  
  
- **out** - 스트림에 삽입을 허용합니다.  
  
- **trunc** - 해당 제어 개체를 만들 때 기존 파일의 콘텐츠를 삭제합니다.  
  
### <a name="example"></a>예  
  
```cpp  
// ios_base_openmode.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )  
{  
    using namespace std;  
    fstream file;  
    file.open( "rm.txt", ios_base::out | ios_base::trunc );  
    
    file << "testing";  
}    
```  
  
##  <a name="op_eq"></a>  ios_base::operator=  

 ios_base 개체에 대한 대입 연산자입니다.  
  
```  
ios_base& operator=(const ios_base& right);
```  
  
### <a name="parameters"></a>매개 변수  
 `right`  
 `ios_base` 형식의 개체입니다.  
  
### <a name="return-value"></a>반환 값  
  
 할당 중인 개체입니다.  
  
### <a name="remarks"></a>설명  
  
 연산자는 저장된 서식 정보를 복사하여 확장 가능한 배열의 새 복사본을 만듭니다. 그런 다음 **\*this**를 반환합니다. 콜백 스택은 복사되지 않습니다.  
  
 이 연산자는 `ios_base`에서 파생된 클래스에서만 사용됩니다.  
  
##  <a name="precision"></a>  ios_base::precision  
  
 부동 소수점 숫자에 표시할 자릿수를 지정합니다.  
  
```  
streamsize precision() const;
streamsize precision(streamsize _Prec);
```  
  
### <a name="parameters"></a>매개 변수  
 `_Prec`  
 표시할 유효 자릿수 또는 고정 표기법에서 소수점 뒤의 자릿수입니다.  
  
### <a name="return-value"></a>반환 값  
  
 첫 번째 멤버 함수는 저장된 [표시 자릿수](../standard-library/ios-base-class.md)를 반환합니다. 두 번째 멤버 함수는 `_Prec`를 표시 자릿수에 저장하고 이전에 저장된 값을 반환합니다.  
  
### <a name="remarks"></a>설명  
  
 부동 소수점 숫자는 [fixed](../standard-library/ios-functions.md#fixed)를 사용하여 고정 표기법으로 표시됩니다.  
  
### <a name="example"></a>예  
  
```cpp  
// ios_base_precision.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
    float i = 31.31234F;  
    
    cout.precision( 3 );  
    cout << i << endl;          // display three significant digits  
    cout << fixed << i << endl; // display three digits after decimal  
                                // point  
}  
```  
  
```Output  
31.3  
31.312  
```  
  
##  <a name="pword"></a>  ios_base::pword  
  
 `pword`로 저장할 수 있는 값을 할당합니다.  
  
```  
void *& pword(int _Idx);
```  
  
### <a name="parameters"></a>매개 변수  
 `_Idx`  
 `pword`로 저장할 값의 인덱스입니다.  
  
### <a name="remarks"></a>설명  
  
 멤버 함수는 `void` 포인터 형식의 요소와 함께 확장 가능한 배열의 _ *Idx* 요소에 대한 참조를 반환합니다. 모든 요소는 효과적으로 존재하며 처음에는 null 포인터를 저장합니다. 반환된 참조는 개체에 대한 `pword`를 다음에 호출한 후, **basic_ios::**[copyfmt](../standard-library/basic-ios-class.md#copyfmt)를 호출하여 개체가 변경된 후 또는 개체가 삭제된 후에는 유효하지 않게 됩니다.  
  
 _ *Idx*가 음수인 경우 또는 요소에 대해 고유한 저장소를 사용할 수 없는 경우 함수는 [setstate](../standard-library/basic-ios-class.md#setstate)**(badbit)**를 호출하고 고유하지 않을 수 있는 참조를 반환합니다.  
  
 `ios_base` 형식의 모든 개체에서 사용하도록 고유 인덱스를 가져오려면 [xalloc](#xalloc)를 호출합니다.  
  
### <a name="example"></a>예  
  
  `pword` 사용 예제는 [xalloc](#xalloc)를 참조하세요.  
  
##  <a name="register_callback"></a>  ios_base::register_callback  
  
 콜백 함수를 지정합니다.  
  
```  
void register_callback(
    event_callback pfn, int idx);
```  
  
### <a name="parameters"></a>매개 변수  
 `pfn`  
 콜백 함수에 대한 포인터입니다.  
  
 `idx`  
 사용자 정의 숫자입니다.  
  
### <a name="remarks"></a>설명  
  
 멤버 함수 쌍 푸시합니다 `{pfn, idx}` 저장된 콜백 스택으로 [콜백 스택을](../standard-library/ios-base-class.md)합니다. 콜백 이벤트를 **ev** 보고 되 면는 함수가 호출 된 순서와 반대로 레지스트리를 식으로 `(*pfn)(ev, *this, idx)`합니다.  
 
### <a name="example"></a>예  
  
```cpp  
// ios_base_register_callback.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
using namespace std;  
  
void callback1( ios_base::event e, ios_base& stream, int arg )  
{  
    cout << "in callback1" << endl;  
    switch ( e )  
    {  
    case ios_base::erase_event:  
        cout << "an erase event" << endl;  
        break;  
    case ios_base::imbue_event:  
        cout << "an imbue event" << endl;  
        break;  
    case ios_base::copyfmt_event:  
        cout << "an copyfmt event" << endl;  
        break;  
    };  
}  
  
void callback2( ios_base::event e, ios_base& stream, int arg )  
{  
    cout << "in callback2" << endl;  
    switch ( e )  
    {  
    case ios_base::erase_event:  
        cout << "an erase event" << endl;  
        break;  
    case ios_base::imbue_event:  
        cout << "an imbue event" << endl;  
        break;  
    case ios_base::copyfmt_event:  
        cout << "an copyfmt event" << endl;  
        break;  
    };  
}  
  
int main( )  
{  
    // Make sure the imbue will not throw an exception  
    // assert( setlocale( LC_ALL, "german" )!=NULL );  
    
    cout.register_callback( callback1, 0 );  
    cin.register_callback( callback2, 0 );  
    
    try  
    {  
        // If no exception because the locale's not found,  
        // generate an imbue_event on callback1  
        cout.imbue(locale("german"));  
    }  
    catch(...)  
    {  
        cout << "exception" << endl;  
    }  
    
    // This will  
    // (1) erase_event on callback1  
    // (2) copyfmt_event on callback2  
    cout.copyfmt(cin);  
    
    // We get two erase events from callback2 at the end because  
    // both cin and cout have callback2 registered when cin and cout  
    // are destroyed at the end of program.  
}  
```  
  
```Output  
in callback1  
an imbue event  
in callback1  
an erase event  
in callback2  
an copyfmt event  
in callback2  
an erase event  
in callback2  
an erase event  
```  
 
##  <a name="seekdir"></a> ios_base::seekdir  
  
오프셋 작업에 대한 시작 지점을 지정합니다.  
  
```  
namespace std {  
    class ios_base {  
    public:  
        typedef implementation-defined-enumerated-type seekdir;  
        static const seekdir beg;  
        static const seekdir cur;  
        static const seekdir end;  
        // ...  
    };  
}  
```  
 
### <a name="remarks"></a>설명  
  
유형 여러 iostream 클래스의 멤버 함수에 대 한 인수로 사용 되는 검색 모드를 저장할 수 있는 개체를 설명 하는 열거 형식이입니다. 고유 플래그 값은 다음과 같습니다.  
 
- **beg** - 시퀀스의 시작(배열, 스트림 또는 파일)을 기준으로 검색(현재 읽기 또는 쓰기 위치 변경)합니다.  
 
- **cur** - 시퀀스 내에서 현재 위치를 기준으로 검색합니다.  
 
- **end** - 시퀀스의 끝을 기준으로 검색합니다.  
 
### <a name="example"></a>예  
  
```cpp  
// ios_base_seekdir.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <fstream>  
  
int main ( )  
{  
    using namespace std;  
    fstream file;  
    file.open( "rm.txt", ios_base::out | ios_base::trunc );  
    
    file << "testing";  
    file.seekp( 0, ios_base::beg );  
    file << "a";  
    file.seekp( 0, ios_base::end );  
    file << "a";  
}  
```  
  
##  <a name="setf"></a> ios_base::setf  
  
지정된 플래그를 설정합니다.  

```    
fmtflags setf(  
    fmtflags _Mask  
);  
fmtflags setf(  
    fmtflags _Mask,  
    fmtflags _Unset  
);  
```  
 
### <a name="parameters"></a>매개 변수  
 `_Mask`  
    설정할 플래그입니다.  
 
 *_Unset* 플래그를 해제 합니다.  
 
### <a name="return-value"></a>반환 값  
    The previous format flags  
 
### <a name="remarks"></a>설명  
    The first member function effectively calls [flags](#flags)(_ *Mask* &#124; \_ *Flags*) (set selected bits) and then returns the previous format flags. The second member function effectively calls **flags**(\_ *Mask* **& fmtfl, flags& ~**`_Mask`) (replace selected bits under a mask) and then returns the previous format flags.  
 
### <a name="example"></a>예  
  
```cpp  
// ios_base_setf.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
    int i = 10;  
    cout << i << endl;  
    
    cout.unsetf( ios_base::dec );  
    cout.setf( ios_base::hex );  
    cout << i << endl;  
    
    cout.setf( ios_base::dec );  
    cout << i << endl;  
    cout.setf( ios_base::hex, ios_base::dec );  
    cout << i << endl;  
}  
```  
 
##  <a name="sync_with_stdio"></a> ios_base::sync_with_stdio  
  
iostream 및 C 런타임 라이브러리 작업이 소스 코드에 표시되는 순서로 수행되도록 합니다.  
  
```  
static bool sync_with_stdio(  
   bool _Sync = true  
);  
```  
 
### <a name="parameters"></a>매개 변수  
 `_Sync`  
    모든 스트림이 **stdio**와 동기화되는지 여부입니다.  
 
### <a name="return-value"></a>반환 값  
    Previous setting for this function.  
 
### <a name="remarks"></a>설명  
    The static member function stores a **stdio** sync flag, which is initially **true**. When **true**, this flag ensures that operations on the same file are properly synchronized between the [iostreams](../standard-library/iostreams-conventions.md) functions and those defined in the C++ Standard Library. Otherwise, synchronization may or may not be guaranteed, but performance may be improved. The function stores `_Sync` in the **stdio** sync flag and returns its previous stored value. You can call it reliably only before performing any operations on the standard streams.  
 
##  <a name="unsetf"></a> ios_base::unsetf  
  
지정된 플래그가 해제되도록 합니다.  
  
```  
void unsetf(  
   fmtflags _Mask  
);  
```  
 
### <a name="parameters"></a>매개 변수  
 `_Mask`  
    해제하려는 플래그입니다.  
 
### <a name="remarks"></a>설명  
    The member function effectively calls [flags](#flags)(`~`*_Mask* **& flags**) (clear selected bits).  
 
### <a name="example"></a>예  
    See [ios_base::setf](#setf) for a sample of using `unsetf`.  
 
##  <a name="width"></a> ios_base::width  
  
출력 스트림의 길이를 설정합니다.  
  
```  
streamsize width( ) const;  
streamsize width(  
   streamsize _Wide  
);  
```  
 
### <a name="parameters"></a>매개 변수  
 `_Wide`  
    출력 스트림의 원하는 크기입니다.  
 
### <a name="return-value"></a>반환 값  

    The current width setting.  
 
### <a name="remarks"></a>설명  

    The first member function returns the stored field width. The second member function stores `_Wide` in the field width and returns its previous stored value.  
 
### <a name="example"></a>예  
  
```cpp  
// ios_base_width.cpp  
// compile with: /EHsc  
#include <iostream>  
  
int main( ) {  
    using namespace std;  
    
    cout.width( 20 );  
    cout << cout.width( ) << endl;  
    cout << cout.width( ) << endl;  
}  
```  
  
```Output  
20  
0  
```  
 
##  <a name="xalloc"></a> ios_base::xalloc  
  
    Specifies that a variable is part of the stream.  
  
```  
static int xalloc( );  
```  
 
### <a name="return-value"></a>반환 값  
    The static member function returns a stored static value, which it increments on each call.  
 
### <a name="remarks"></a>설명  
    You can use the return value as a unique index argument when calling the member functions [iword](#iword) or [pword](#pword).  
 
### <a name="example"></a>예  
  
```cpp  
// ios_base_xalloc.cpp  
// compile with: /EHsc  
// Lets you store user-defined information.  
// iword, jword, xalloc  
#include <iostream>  
  
int main( )  
{  
    using namespace std;  
    
    static const int i = ios_base::xalloc();  
    static const int j = ios_base::xalloc();  
    cout.iword( i ) = 11;  
    cin.iword( i ) = 13;  
    cin.pword( j ) = "testing";  
    cout << cout.iword( i ) << endl;  
    cout << cin.iword( i ) << endl;  
    cout << ( char * )cin.pword( j ) << endl;  
}    
```  
  
```Output  
11  
13  
testing  
```  
  
## <a name="see-also"></a>참고 항목  
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [iostream 프로그래밍](../standard-library/iostream-programming.md)   
 [iostreams 규칙](../standard-library/iostreams-conventions.md)
