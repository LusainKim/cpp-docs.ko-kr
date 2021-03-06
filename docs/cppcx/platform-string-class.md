---
title: "Platform:: string 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 12/30/2016
ms.technology: cpp-windows
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords:
- VCCORLIB/Platform::String::String
- VCCORLIB/Platform::String::Begin
- VCCORLIB/Platform::String::CompareOrdinal
- VCCORLIB/Platform::String::Concat
- VCCORLIB/Platform::String::Data
- VCCORLIB/Platform::String::Dispose
- VCCORLIB/Platform::String::End
- VCCORLIB/Platform::String::Equals
- VCCORLIB/Platform::String::GetHashCode
- VCCORLIB/Platform::String::IsEmpty
- VCCORLIB/Platform::String::IsFastPass
- VCCORLIB/Platform::String::Length
- VCCORLIB/Platform::String::ToString
dev_langs: C++
helpviewer_keywords: Platform::String
ms.assetid: 72dd04a4-a694-40d3-b899-eaa0b503eab8
caps.latest.revision: "7"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 2bf0a8e9c768425fc55b1c819b01d6c3cf4b88dd
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="platformstring-class"></a>Platform::String 클래스
텍스트를 나타내는 데 사용되는 유니코드 문자의 순차적인 컬렉션을 나타냅니다. 자세한 내용 및 예제에 대 한 참조 [문자열](../cppcx/strings-c-cx.md)합니다.  
  
## <a name="syntax"></a>구문  
  
```cpp  
  
public ref class String sealed : Object,  
    IDisposable,  
    IEquatable,  
    IPrintable  
```  
  
## <a name="iterators"></a>반복기  
 String 클래스의 멤버가 아닌 두 반복기 함수를 `std::for_each` 템플릿 함수와 함께 사용하여 String 개체의 문자를 열거할 수 있습니다.  
  
|멤버|설명|  
|------------|-----------------|  
|`const char16* begin(String^ s)`|지정된 String 개체의 시작 부분에 대한 포인터를 반환합니다.|  
|`const char16* end(String^ s)`|지정된 String 개체의 끝을 지나는 포인터를 반환합니다.|  
  
### <a name="members"></a>멤버  
 String 클래스는 Object 및 IDisposable, IEquatable 및 IPrintable 인터페이스에서 상속합니다.  
  
 String 클래스에는 다음 형식의 멤버도 있습니다.  
  
 **생성자**  
  
|멤버|설명|  
|------------|-----------------|  
|[String:: string](#ctor)|String 클래스의 새 인스턴스를 초기화합니다.|  
  
 **메서드**  
  
 String 클래스는 [Platform::Object Class](../cppcx/platform-object-class.md)의 Equals(), Finalize(), GetHashCode(), GetType(), MemberwiseClose() 및 ToString() 메서드를 상속합니다. String에는 다음 메서드도 있습니다.  
  
|메서드|설명|  
|------------|-----------------|  
|[String:: begin](#begin)|현재 문자열의 시작 부분에 대한 포인터를 반환합니다.|  
|[String:: compareordinal](#compareordinal)|개체가 나타내는 두 문자열 값에서 해당 문자의 숫자 값을 계산하여 두 `String` 개체를 비교합니다.|  
|[String:: concat](#concat)|두 String 개체의 값을 연결합니다.|  
|[String:: data](#data)|현재 문자열의 시작 부분에 대한 포인터를 반환합니다.|  
|[String:: dispose](#dispose)|리소스를 확보하거나 해제합니다.|  
|[String:: end](#end)|현재 문자열의 끝을 지나는 포인터를 반환합니다.|  
|[String:: equals](#equals)|지정된 개체가 현재 개체와 같은지 여부를 나타냅니다.|  
|[String:: gethashcode](#gethashcode)|이 인스턴스의 해시 코드를 반환합니다.|  
|[String:: isempty](#isempty)|현재 String 개체가 비어 있는지 여부를 나타냅니다.|  
|[String:: isfastpass](#isfastpass)|현재 String 개체가 *빠른 전달* 작업에 참여하고 있는지를 나타냅니다. 빠른 전달 작업에서는 참조 횟수가 일시 중단됩니다.|  
|[String:: length](#length)|현재 String 개체의 길이를 검색합니다.|  
|[String:: tostring](#tostring)|현재 문자열과 같은 값을 갖는 String 개체를 반환합니다.|  
  
 **연산자**  
  
 String 클래스에는 다음과 같은 연산자입니다.  
  
|멤버|설명|  
|------------|-----------------|  
|[String:: operator = = 연산자](#operator-equality)|지정된 두 String 개체의 값이 같은지 여부를 나타냅니다.|  
|[operator+ Operator](#operator-plus)|두 String 개체를 새 String 개체에 연결합니다.|  
|[String:: operator > 연산자](#operator-greater-than)|String 개체 값이 두 번째 String 개체 값보다 큰지 여부를 나타냅니다.|  
|[String:: operator > = 연산자](#operator-greater-than-or-equals)|String 개체 값이 두 번째 String 개체 값보다 크거나 같은지 여부를 나타냅니다.|  
|[String:: operator! = 연산자](#operator-inequality)|지정된 두 String 개체의 값이 다른지 여부를 나타냅니다.|  
|[String:: operator < 연산자](#operator-less-than)|String 개체 값이 두 번째 String 개체 값보다 작은지 여부를 나타냅니다.|  
  
### <a name="requirements"></a>요구 사항  
 **지원 되는 최소 클라이언트:** Windows 8  
  
 **지원 되는 최소 서버:** Windows Server 2012  
  
 **네임스페이스:** Platform  
  
 **헤더** vccorlib.h(기본적으로 포함)  

 
## <a name="begin"></a>String:: begin 메서드
현재 문자열의 시작 부분에 대한 포인터를 반환합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
  
char16* Begin()  
```  
  
### <a name="return-value"></a>반환 값  
 현재 문자열의 시작 부분에 대한 포인터입니다.  
  
## <a name="compareordinal"></a>String:: compareordinal 메서드
개체가 나타내는 두 문자열 값에서 해당 문자의 숫자 값을 계산하여 두 `String` 개체를 비교합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
  
int CompareOrdinal(  
           String^ str1,   
           String^ str2)  
  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 첫 번째 String 개체입니다.  
  
 `str2`  
 두 번째 String 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 두 비교 대상 간의 어휘 관계를 나타내는 정수입니다. 다음 표에서는 가능한 반환 값을 보여 줍니다.  
  
|값|조건|  
|-----------|---------------|  
|-1|`str1`가 `str2`보다 작은 경우|  
|0|`str1`이 `str2`와 같은 경우|  
|1|`str1`가 `str2`보다 큰 경우|  
  


## <a name="concat"></a>String:: concat 메서드
두 String 개체의 값을 연결합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
String^ Concat( String^ str1, String^ str2)  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 첫 번째 String 개체 또는 `null`입니다.  
  
 `str2`  
 두 번째 String 개체 또는 `null`입니다.  
  
### <a name="return-value"></a>반환 값  
 `str1` 값과 `str2` 값의 연결을 값으로 하는 새로운 String^ 개체입니다.  
  
 경우 `str1` 은 `null` 및 `str2` 는 사용 되지 않는 `str1` 반환 됩니다. 경우 `str2` 은 `null` 및 `str1` 는 사용 되지 않는 `str2` 반환 됩니다. `str1`과 `str2`가 모두 `null`이면 빈 문자열(L"")이 반환됩니다.  
  


## <a name="data"></a>String:: data 메서드
개체의 데이터 버퍼 시작에 대한 포인터를 `char16`(`wchar_t`) 요소의 C 스타일 배열로 반환합니다.  
  
### <a name="syntax"></a>구문  
  
```  
const char16* Data()  
```  
  
### <a name="return-value"></a>반환 값  
 시작 부분에 대 한 포인터는 `const char16` 유니코드 문자 배열 (`char16` 에 대 한 typedef `wchar_t`).  
  
### <a name="remarks"></a>설명  
 이 메서드를 사용하여 `Platform::String^`에서 `wchar_t*`로 변환합니다. `String` 개체가 범위를 벗어나는 경우 데이터 포인터의 유효성이 더 이상 보장되지 않습니다. 원래의 수명 넘어서는 데이터를 저장 하려면 `String` 개체를 가져오려면 [wcscpy_s](../c-runtime-library/reference/strcpy-s-wcscpy-s-mbscpy-s.md) 직접 할당 한 메모리로 배열을 복사 합니다.  
  


## <a name="dispose"></a>String:: dispose 메서드
리소스를 확보하거나 해제합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
  
virtual override void Dispose()  
```  

## <a name="end"></a>String:: end 메서드
현재 문자열의 끝을 지나는 포인터를 반환합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
  
char16* End()  
```  
  
### <a name="return-value"></a>반환 값  
 현재 문자열의 끝을 지나는 포인터입니다.  
  
### <a name="remarks"></a>설명  
 End ()는 begin () + Length를 반환 합니다.  
  


## <a name="equals"></a>String:: equals 메서드
지정된 String의 값이 현재 개체와 동일한지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
  
bool String::Equals(Object^ str);  
  
bool String::Equals(String^ str);  
  
```  
  
### <a name="parameters"></a>매개 변수  
 `str`  
 비교할 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `true`이 현재 개체와 같으면 `str`이고, 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 해당 하는 [string:: compareordinal](#compareordinal)합니다. 첫 번째 오버로드에서는 `str` 매개 변수가 String^ 개체로 캐스팅될 수 있어야 합니다.  
  


## <a name="gethashcode"></a>String:: gethashcode 메서드
이 인스턴스의 해시 코드를 반환합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
  
virtual override int GetHashCode()  
```  
  
### <a name="return-value"></a>반환 값  
 이 인스턴스의 해시 코드입니다.  
  


## <a name="isempty"></a>String:: isempty 메서드
현재 String 개체가 비어 있는지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
bool IsEmpty()  
```  
  
### <a name="return-value"></a>반환 값  
 현재 String 개체가 `true` 또는 빈 문자열(L"")이면 `null`이고, 그렇지 않으면 `false`입니다.  
  


## <a name="isfastpass"></a>String:: isfastpass 메서드
현재 String 개체가 *빠른 전달* 작업에 참여하고 있는지를 나타냅니다. 빠른 전달 작업에서는 참조 횟수가 일시 중단됩니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
bool IsFastPass();  
```  
  
### <a name="return-value"></a>반환 값  
 현재 String 개체가 fast-past이면 `true`이고, 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 참조 횟수가 계산된 개체가 매개 변수이고, 호출된 함수가 이 개체만 읽는 함수에 대한 호출인 경우 컴파일러는 참조 횟수를 안전하게 일시 중단하고 호출 성능을 향상시킬 수 있습니다. 코드에서 이 속성으로 할 수 있는 유용한 일은 없습니다. 시스템에서 모든 세부 사항을 처리합니다.  
  


## <a name="length"></a>String:: length 메서드
현재 String 개체의 문자 수를 검색합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
unsigned int Length()  
```  
  
### <a name="return-value"></a>반환 값  
 현재 String 개체의 문자 수입니다.  
  
### <a name="remarks"></a>설명  
 문자가 없는 String의 길이는 0입니다. 다음 String의 길이는 5입니다.  
  
```    
String^ str = "Hello";  
int len = str->Length(); //len = 5  
```  
  
 문자 배열에서 반환 되는 [string:: data](#data) 종결 NULL 또는 '\0' 인 추가 문자열이 하나 있습니다. 이 문자의 길이도 2바이트입니다.  
  


## <a name="operator-plus"></a>String:: operator + 연산자
두 개의 연결 [문자열](../cppcx/platform-string-class.md) 새 개체 [문자열](../cppcx/platform-string-class.md) 개체입니다.
  
### <a name="syntax"></a>구문  
  
```cpp  
  
bool String::operator+( String^ str1, String^ str2)  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 첫 번째 `String` 개체입니다.  
  
 `str2`  
 내용이 `String`에 추가될 두 번째`str1` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `true`가 `str1`와 같으면 `str2`이고, 그러지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 이 연산자는 두 피연산자의 데이터가 들어 있는 `String^` 개체를 만듭니다. 매우 높은 성능이 중요하지 않은 경우 편의를 위해 이를 사용합니다. 함수에서 "`+`"를 몇 번 호출하는 것은 그렇게 눈에 띄지 않지만 대행 개체나 텍스트 데이터를 연속해서 조작하는 경우 표준 C++ 매커니즘과 형식을 사용하십시오.  
  
##  <a name="operator-equality"></a>String:: operator = = 연산자
지정된 두 String 개체의 텍스트 값이 같은지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
bool String::operator==( String^ str1, String^ str2)  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 비교할 첫 번째 String 개체입니다.  
  
 `str2`  
 비교할 두 번째 String 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `true`의 내용이 `str1`와 같으면 `str2`이고, 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 이 연산자는 같음 [string:: compareordinal](#compareordinal)합니다.  
  


##  <a name="operator-greater-than"></a>String:: operator&gt; 
String 개체 값이 두 번째 String 개체 값보다 큰지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
bool String::operator>( String^ str1, String^ str2)  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 첫 번째 String 개체입니다.  
  
 `str2`  
 두 번째 String 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `str1`의 값이 `str2`의 값보다 크면 `true`이고, 그렇지 않으면 `false`입니다.  
  
### <a name="remarks"></a>설명  
 명시적으로 호출 하는 것이 연산자는 [string:: compareordinal](#compareordinal) 고 0 보다 큰 결과 가져오는 합니다.  
  


## <a name="operator-greater-than-or-equals"></a>String:: operator&gt;= 
String 개체 값이 두 번째 String 개체 값보다 크거나 같은지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
bool String::operator>=( String^ str1, String^ str2) 
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 첫 번째 String 개체입니다.  
  
 `str2`  
 두 번째 String 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `str1`의 값이 `str2`의 값보다 크거나 같으면 `true`이고, 그렇지 않으면 `false`입니다.  
  


## <a name="operator-inequality"></a>String:: operator! = 
지정된 두 String 개체의 값이 다른지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
bool String::operator!=( String^ str1, String^ str2)  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 비교할 첫 번째 String 개체입니다.  
  
 `str2`  
 비교할 두 번째 String 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `true`가 `str1`와 다르면 `str2`이고, 그러지 않으면 `false`입니다.   


## <a name="operator-less-than"></a>String:: operator&lt; 
String 개체 값이 두 번째 String 개체 값보다 작은지 여부를 나타냅니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
bool String::operator<( String^ str1, String^ str2)  
```  
  
### <a name="parameters"></a>매개 변수  
 `str1`  
 첫 번째 String 개체입니다.  
  
 `str2`  
 두 번째 String 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `str1`의 값이 `str2`의 값보다 작으면 `true`이고, 그렇지 않으면 `false`입니다.  
  
## <a name="ctor"></a>String:: string 생성자
입력 문자열 데이터의 복사본을 사용하여 String 클래스의 새 인스턴스를 초기화합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp    
String();    
String(char16* s)  
String(char16* s, unsigned int n)  
```  
  
### <a name="parameters"></a>매개 변수  
 `s`  
 문자열을 초기화하는 일련의 와이드 문자입니다. char16  
  
 `n`  
 문자열의 길이를 지정하는 숫자입니다.  
  
### <a name="remarks"></a>설명  
 성능이 중요 하며 소스 문자열의 수명을 제어 하는 경우 사용할 수 있습니다 [platform:: stringreference](../cppcx/platform-stringreference-class.md) 문자열 대신 합니다.  
### <a name="example"></a>예  
  
```cpp  
String^ s = L"Hello!";  
```  
  
## <a name="tostring"></a>String:: tostring
현재 문자열과 같은 값을 갖는 String 개체를 반환합니다.  
  
### <a name="syntax"></a>구문  
  
```cpp  
String^ String::ToString()  
```  
  
### <a name="return-value"></a>반환 값  
 현재 문자열과 같은 값을 갖는 String 개체입니다.  
  
## <a name="see-also"></a>참고 항목  
 [Platform 네임 스페이스](../cppcx/platform-namespace-c-cx.md)