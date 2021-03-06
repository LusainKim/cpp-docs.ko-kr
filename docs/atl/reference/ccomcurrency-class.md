---
title: "CComCurrency 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CComCurrency
- ATLCUR/ATL::CComCurrency
- ATLCUR/ATL::CComCurrency::CComCurrency
- ATLCUR/ATL::CComCurrency::GetCurrencyPtr
- ATLCUR/ATL::CComCurrency::GetFraction
- ATLCUR/ATL::CComCurrency::GetInteger
- ATLCUR/ATL::CComCurrency::Round
- ATLCUR/ATL::CComCurrency::SetFraction
- ATLCUR/ATL::CComCurrency::SetInteger
- ATLCUR/ATL::CComCurrency::m_currency
dev_langs: C++
helpviewer_keywords: CComCurrency class
ms.assetid: a1c3d10a-bba6-40cc-8bcf-aed9023c8a9e
caps.latest.revision: "21"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: c3ef0cdc45d4f3b84c738e5eec24d76a1f9b7fe2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ccomcurrency-class"></a>CComCurrency 클래스
`CComCurrency`에는 CURRENCY 개체를 만들고 관리하는 메서드 및 연산자가 있습니다.  
  
## <a name="syntax"></a>구문  
  
```
class CComCurrency
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CComCurrency::CComCurrency](#ccomcurrency)|`CComCurrency` 개체에 대한 생성자입니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CComCurrency::GetCurrencyPtr](#getcurrencyptr)|`m_currency` 데이터 멤버의 주소를 반환합니다.|  
|[Ccomcurrency:: Getfraction](#getfraction)|`CComCurrency` 개체의 소수 부분을 반환하려면 이 메서드를 호출합니다.|  
|[CComCurrency::GetInteger](#getinteger)|`CComCurrency` 개체의 정수 부분을 반환하려면 이 메서드를 호출합니다.|  
|[CComCurrency::Round](#round)|`CComCurrency` 개체를 가장 가까운 정수 값으로 반올림하려면 이 메서드를 호출합니다.|  
|[CComCurrency::SetFraction](#setfraction)|`CComCurrency` 개체의 소수 부분을 설정하려면 이 메서드를 호출합니다.|  
|[CComCurrency::SetInteger](#setinteger)|`CComCurrency` 개체의 정수 부분을 설정하려면 이 메서드를 호출합니다.|  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|[CComCurrency::operator-](#operator_-)|이 연산자는 `CComCurrency` 개체에 대해 빼기를 수행하는 데 사용됩니다.|  
|[CComCurrency::operator! =](#operator_neq)|두 `CComCurrency` 개체가 다른지 비교합니다.|  
|[CComCurrency::operator *](#operator_star)|이 연산자는 `CComCurrency` 개체에 대해 곱하기를 수행하는 데 사용됩니다.|  
|[CComCurrency::operator * =](#operator_star_eq)|이 연산자는 `CComCurrency` 개체에 대해 곱하기를 수행하고 결과를 할당하는 데 사용됩니다.|  
|[CComCurrency::operator /](#operator_div)|이 연산자는 `CComCurrency` 개체에 대해 나누기를 수행하는 데 사용됩니다.|  
|[CComCurrency::operator / =](#operator_div_eq)|이 연산자는 `CComCurrency` 개체에 대해 나누기를 수행하고 결과를 할당하는 데 사용됩니다.|  
|[CComCurrency::operator +](#operator_add)|이 연산자는 `CComCurrency` 개체에 대해 더하기를 수행하는 데 사용됩니다.|  
|[CComCurrency::operator + =](#operator_add_eq)|이 연산자는 `CComCurrency` 개체에 대해 더하기를 수행하고 결과를 현재 개체에 할당하는 데 사용됩니다.|  
|[CComCurrency::operator <](#operator_lt)|이 연산자는 두 `CComCurrency` 개체를 비교하여 더 작은 값을 확인합니다.|  
|[CComCurrency::operator < =](#operator_lt_eq)|이 연산자는 두 `CComCurrency` 개체를 비교하여 더 작거나 같은 값을 확인합니다.|  
|[CComCurrency::operator =](#operator_eq)|다음 연산자는 `CComCurrency` 개체에 새 값을 할당합니다.|  
|[-= CComCurrency::operator](#operator_-_eq)|이 연산자는 `CComCurrency` 개체에 대해 빼기를 수행하고 결과를 할당하는 데 사용됩니다.|  
|[CComCurrency::operator = =](#operator_eq_eq)|이 연산자는 두 `CComCurrency` 개체가 같은지 비교합니다.|  
|[CComCurrency::operator >](#operator_gt)|이 연산자는 두 `CComCurrency` 개체를 비교하여 더 큰 값을 확인합니다.|  
|[CComCurrency::operator > =](#operator_gt_eq)|이 연산자는 두 `CComCurrency` 개체를 비교하여 더 크거나 같은 값을 확인합니다.|  
|[CComCurrency::operator 통화](#operator_currency)|`CURRENCY` 개체를 캐스트합니다.|  
  
### <a name="public-data-members"></a>공용 데이터 멤버  
  
|이름|설명|  
|----------|-----------------|  
|[CComCurrency::m_currency](#m_currency)|`CURRENCY` 변수는 클래스 인스턴스에 의해 만들어집니다.|  
  
## <a name="remarks"></a>설명  
 `CComCurrency`에 대 한 래퍼 인지는 **통화** 데이터 형식입니다. **통화** 10,000 단위 배율의 8 바이트 2의 보수 정수 값으로 구현 됩니다. 소수점 기호 왼쪽에는 15자리 고정 소수점 번호가 있고 오른쪽에는 4자리 고정 소수점 번호가 있습니다. **통화** 데이터 형식이 포함 된, 계산 또는 모든 고정 소수점 계산에 대 한 매우 유용한 정확도 중요 합니다.  
  
 **CComCurrency** 래퍼는이 고정 소수점 형식에 대 한 산술 연산, 할당 및 비교 작업을 구현 합니다. 지원되는 응용 프로그램은 고정 소수점 계산 시 발생할 수 있는 반올림 오류를 제어하도록 선택했습니다.  
  
 `CComCurrency` 개체는 두 부분(소수점 기호 왼쪽 값을 저장하는 정수 부분과 소수점 기호 오른쪽 값을 저장하는 소수 부분)으로 된 소수점 기호의 한 쪽에 있는 숫자에 대한 액세스를 제공합니다. 소수 부분이-9999 사이의 정수 값으로 내부적으로 저장 됩니다 ( **CY_MIN_FRACTION**)에서 + 9999 ( **CY_MAX_FRACTION**). 메서드가 [ccomcurrency:: Getfraction](#getfraction) 10000 계수로 값을 반환 ( **CY_SCALE**).  
  
 정수 및 소수로 계산 된 구성 요소를 지정 하는 경우는 **CComCurrency** 개체, 소수 부분이 0에서 9999 범위의 숫자입니다. 이는 소수점 뒤 두 자리의 유효 숫자만 사용하여 금액을 표현하는 미국 달러와 같은 통화를 처리할 때 중요합니다. 마지막 두 자리가 표시되지 않는 경우에도 이를 고려해야 합니다.  
  
|값|가능한 CComCurrency 할당|  
|-----------|---------------------------------------|  
|$10.50|CComCurrency(10,5000) *또는* ccomcurrency (10.50)|  
|$10.05|Ccomcurrency (10500) *또는* ccomcurrency (10.05)|  
  
 값 **CY_MIN_FRACTION**, **CY_MAX_FRACTION**, 및 **CY_SCALE** 은 atlcur.h에 정의 됩니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atlcur.h  
  
##  <a name="ccomcurrency"></a>CComCurrency::CComCurrency  
 생성자입니다.  
  
```
CComCurrency() throw();
CComCurrency(const CComCurrency& curSrc) throw();
CComCurrency(CURRENCY cySrc) throw();
CComCurrency(DECIMAL dSrc);
CComCurrency(ULONG ulSrc);  
CComCurrency(USHORT usSrc);  
CComCurrency(CHAR cSrc);  
CComCurrency(DOUBLE dSrc);  
CComCurrency(FLOAT fSrc);  
CComCurrency(LONG lSrc);  
CComCurrency(SHORT sSrc);  
CComCurrency(BYTE bSrc);  
CComCurrency(LONGLONG nInteger, SHORT nFraction);  
explicit CComCurrency(LPDISPATCH pDispSrc);  
explicit CComCurrency(const VARIANT& varSrc);  
explicit CComCurrency(LPCWSTR szSrc);  
explicit CComCurrency(LPCSTR szSrc);
```  
  
### <a name="parameters"></a>매개 변수  
 `curSrc`  
 기존 `CComCurrency` 개체입니다.  
  
 `cySrc`  
 형식의 변수 **통화**합니다.  
  
 `bSrc``dSrc`, `fSrc`, `lSrc`, *sSrc*, *ulSrc, usSrc*  
 멤버 변수를 제공 하는 초기 값 `m_currency`합니다.  
  
 `cSrc`  
 멤버 변수를 지정 된 초기 값을 포함 하는 문자 `m_currency`합니다.  
  
 `nInteger`*nFraction*  
 정수 및 초기 통화 값의 소수 자릿수 구성 요소입니다. 참조는 [CComCurrency](../../atl/reference/ccomcurrency-class.md) 대 한 자세한 내용은 합니다.  
  
 `pDispSrc`  
 `IDispatch` 포인터입니다.  
  
 *varSrc*  
 형식의 변수 **VARIANT**합니다. 현재 스레드의 로캘은 변환을 수행 하기 위해 사용 됩니다.  
  
 `szSrc`  
 초기 값을 포함 하는 ANSI 또는 유니코드 문자열입니다. 현재 스레드의 로캘은 변환을 수행 하기 위해 사용 됩니다.  
  
### <a name="remarks"></a>설명  
 초기 값을 설정 하는 생성자 [CComCurrency::m_currency](#m_currency), 다양 한 범위의 데이터 형식, 정수, 문자열, 부동 소수점 숫자를 포함 하 여 허용 및 **통화** 변수, 오류 코드 및 기타 `CComCurrency` 개체입니다. 값이 제공 하는 경우 `m_currency` 0으로 설정 됩니다.  
  
 빈 예외 사양이 없는 생성자 오버플로와 같이 오류 발생 시 ( **throw ()**) 호출 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
 부동 소수점 또는 double 값을 사용 하 여 값을 할당 때 **ccomcurrency (10.50)** 같습니다 **CComCurrency(10,5000)** 아닌 **CComCurrency(10,50)**.  
  
##  <a name="getcurrencyptr"></a>CComCurrency::GetCurrencyPtr  
 `m_currency` 데이터 멤버의 주소를 반환합니다.  
  
```
CURRENCY* GetCurrencyPtr() throw();
```  
  
### <a name="return-value"></a>반환 값  
 주소를 반환 하는 `m_currency` 데이터 멤버  
  
##  <a name="getfraction"></a>Ccomcurrency:: Getfraction  
 소수 부분을 반환 하려면이 메서드를 호출 하는 `CComCurrency` 개체입니다.  
  
```
SHORT GetFraction() const;
```  
  
### <a name="return-value"></a>반환 값  
 소수 부분이 반환는 `m_currency` 데이터 멤버입니다.  
  
### <a name="remarks"></a>설명  
 소수 부분이-9999 사이의 4 자리 정수 값 ( **CY_MIN_FRACTION**)에서 + 9999 ( **CY_MAX_FRACTION**). `GetFraction`10000으로 조정 된이 값을 반환 합니다 ( **CY_SCALE**). 값 **CY_MIN_FRACTION**, **CY_MAX_FRACTION**, 및 **CY_SCALE** 은 atlcur.h에 정의 됩니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#50](../../atl/codesnippet/cpp/ccomcurrency-class_1.cpp)]  
  
##  <a name="getinteger"></a>CComCurrency::GetInteger  
 정수 부분을 가져오려면이 메서드를 호출 하는 `CComCurrency` 개체입니다.  
  
```
LONGLONG GetInteger() const;
```  
  
### <a name="return-value"></a>반환 값  
 정수 부분을 반환 합니다.는 `m_currency` 데이터 멤버입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#51](../../atl/codesnippet/cpp/ccomcurrency-class_2.cpp)]  
  
##  <a name="m_currency"></a>CComCurrency::m_currency  
 **통화** 데이터 멤버입니다.  
  
```
CURRENCY m_currency;
```  
  
### <a name="remarks"></a>설명  
 이 멤버에 액세스 하 고이 클래스의 메서드에 의해 조작 통화를 보유 합니다.  
  
##  <a name="operator_-"></a>CComCurrency::operator-  
 이 연산자는 `CComCurrency` 개체에 대해 빼기를 수행하는 데 사용됩니다.  
  
```
CComCurrency operator-() const;
CComCurrency operator-(const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 된 `CComCurrency` 빼기의 결과 나타내는 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#55](../../atl/codesnippet/cpp/ccomcurrency-class_3.cpp)]  
  
##  <a name="operator_neq"></a>CComCurrency::operator! =  
 이 연산자는 두 개체가 같지 않은지 비교합니다.  
  
```
bool operator!= (const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 비교할 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 비교 되는 항목에 같은지는 `CComCurrency` 개체; 그렇지 않으면 **false**합니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#56](../../atl/codesnippet/cpp/ccomcurrency-class_4.cpp)]  
  
##  <a name="operator_star"></a>CComCurrency::operator *  
 이 연산자는 `CComCurrency` 개체에 대해 곱하기를 수행하는 데 사용됩니다.  
  
```
CComCurrency operator*(long nOperand) const;
CComCurrency operator*(const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `nOperand`  
 승수입니다.  
  
 `cur`  
 `CComCurrency` 의 승수로 사용 되는 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 된 `CComCurrency` 곱하기의 결과 나타내는 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#57](../../atl/codesnippet/cpp/ccomcurrency-class_5.cpp)]  
  
##  <a name="operator_star_eq"></a>CComCurrency::operator * =  
 이 연산자는 `CComCurrency` 개체에 대해 곱하기를 수행하고 결과를 할당하는 데 사용됩니다.  
  
```
const CComCurrency& operator*= (long nOperand);
const CComCurrency& operator*= (const CComCurrency& cur);
```  
  
### <a name="parameters"></a>매개 변수  
 `nOperand`  
 승수입니다.  
  
 `cur`  
 `CComCurrency` 의 승수로 사용 되는 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 업데이트 된 반환 `CComCurrency` 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#58](../../atl/codesnippet/cpp/ccomcurrency-class_6.cpp)]  
  
##  <a name="operator_div"></a>CComCurrency::operator /  
 이 연산자는 `CComCurrency` 개체에 대해 나누기를 수행하는 데 사용됩니다.  
  
```
CComCurrency operator/(long nOperand) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `nOperand`  
 제수입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 된 `CComCurrency` 나누기의 결과 나타내는 개체입니다. 제 수 0 인 어설션 실패 발생 합니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#59](../../atl/codesnippet/cpp/ccomcurrency-class_7.cpp)]  
  
##  <a name="operator_div_eq"></a>CComCurrency::operator / =  
 이 연산자는 `CComCurrency` 개체에 대해 나누기를 수행하고 결과를 할당하는 데 사용됩니다.  
  
```
const CComCurrency& operator/= (long nOperand);
```  
  
### <a name="parameters"></a>매개 변수  
 `nOperand`  
 제수입니다.  
  
### <a name="return-value"></a>반환 값  
 업데이트 된 반환 `CComCurrency` 개체입니다. 제 수 0 인 어설션 실패 발생 합니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#60](../../atl/codesnippet/cpp/ccomcurrency-class_8.cpp)]  
  
##  <a name="operator_add"></a>CComCurrency::operator +  
 이 연산자는 `CComCurrency` 개체에 대해 더하기를 수행하는 데 사용됩니다.  
  
```
CComCurrency operator+(const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 원래 개체에 추가할 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 된 `CComCurrency` 덧셈의 결과 나타내는 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#61](../../atl/codesnippet/cpp/ccomcurrency-class_9.cpp)]  
  
##  <a name="operator_add_eq"></a>CComCurrency::operator + =  
 이 연산자는 `CComCurrency` 개체에 대해 더하기를 수행하고 결과를 현재 개체에 할당하는 데 사용됩니다.  
  
```
const CComCurrency& operator+= (const CComCurrency& cur);
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체  
  
### <a name="return-value"></a>반환 값  
 업데이트 된 반환 `CComCurrency` 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#62](../../atl/codesnippet/cpp/ccomcurrency-class_10.cpp)]  
  
##  <a name="operator_lt"></a>CComCurrency::operator&lt;  
 이 연산자는 두 `CComCurrency` 개체를 비교하여 더 작은 값을 확인합니다.  
  
```
bool operator<(const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 작으면 첫 번째 개체가 두 번째 보다 **false** 그렇지 않은 경우.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#63](../../atl/codesnippet/cpp/ccomcurrency-class_11.cpp)]  
  
##  <a name="operator_lt_eq"></a>CComCurrency::operator&lt;=  
 이 연산자는 두 `CComCurrency` 개체를 비교하여 더 작거나 같은 값을 확인합니다.  
  
```
bool operator<= (const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 첫 번째 개체가 두 번째 보다 작은 경우 **false** 그렇지 않은 경우.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#64](../../atl/codesnippet/cpp/ccomcurrency-class_12.cpp)]  
  
##  <a name="operator_eq"></a>CComCurrency::operator =  
 다음 연산자는 `CComCurrency` 개체에 새 값을 할당합니다.  
  
```
const CComCurrency& operator= (const CComCurrency& curSrc) throw();
const CComCurrency& operator= (CURRENCY cySrc) throw();
const CComCurrency& operator= (FLOAT fSrc);
const CComCurrency& operator= (SHORT sSrc);
const CComCurrency& operator= (LONG lSrc);
const CComCurrency& operator= (BYTE bSrc);
const CComCurrency& operator= (USHORT usSrc);
const CComCurrency& operator= (DOUBLE dSrc);
const CComCurrency& operator= (CHAR cSrc);
const CComCurrency& operator= (ULONG ulSrc);
const CComCurrency& operator= (DECIMAL dSrc);
```  
  
### <a name="parameters"></a>매개 변수  
 `curSrc`  
 A **CComCurrency** 개체입니다.  
  
 `cySrc`  
 형식의 변수 **통화**합니다.  
  
 *sSrc*, `fSrc`, `lSrc`, *bSrc*, *usSrc*, `dSrc`, *cSrc*, *ulSrc*,`dSrc`  
 숫자 값에 할당 하는 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 업데이트 된 반환 `CComCurrency` 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#65](../../atl/codesnippet/cpp/ccomcurrency-class_13.cpp)]  
  
##  <a name="operator_-_eq"></a>-= CComCurrency::operator  
 이 연산자는 `CComCurrency` 개체에 대해 빼기를 수행하고 결과를 할당하는 데 사용됩니다.  
  
```
const CComCurrency& operator-= (const CComCurrency& cur);
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 업데이트 된 반환 `CComCurrency` 개체입니다. 이 연산자는 호출, 오버플로와 같이 오류 발생 시 `AtlThrow` 오류를 설명 하는 hresult입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#66](../../atl/codesnippet/cpp/ccomcurrency-class_14.cpp)]  
  
##  <a name="operator_eq_eq"></a>CComCurrency::operator = =  
 이 연산자는 두 `CComCurrency` 개체가 같은지 비교합니다.  
  
```
bool operator== (const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 비교할 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 는 개체가 같으면 (즉,는 `m_currency` 데이터 멤버, 두 정수 부분과 소수 부분 모두에 동일한 값을 포함 하는 개체), **false** 그렇지 않은 경우.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#67](../../atl/codesnippet/cpp/ccomcurrency-class_15.cpp)]  
  
##  <a name="operator_gt"></a>CComCurrency::operator&gt;  
 이 연산자는 두 `CComCurrency` 개체를 비교하여 더 큰 값을 확인합니다.  
  
```
bool operator>(const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 첫 번째 개체가 두 번째 보다 큰 경우 **false** 그렇지 않은 경우.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#68](../../atl/codesnippet/cpp/ccomcurrency-class_16.cpp)]  
  
##  <a name="operator_gt_eq"></a>CComCurrency::operator&gt;=  
 이 연산자는 두 `CComCurrency` 개체를 비교하여 더 크거나 같은 값을 확인합니다.  
  
```
bool operator>= (const CComCurrency& cur) const;
```  
  
### <a name="parameters"></a>매개 변수  
 `cur`  
 `CComCurrency` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 첫 번째 개체가 두 번째 보다 크거나 **false** 그렇지 않은 경우.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#69](../../atl/codesnippet/cpp/ccomcurrency-class_17.cpp)]  
  
##  <a name="operator_currency"></a>CComCurrency::operator 통화  
 이러한 연산자는 캐스팅 하는 데 사용 되는 `CComCurrency` 개체는 **통화** 데이터 형식입니다.  
  
```  
operator CURRENCY&() throw();
operator const CURRENCY&() const throw();
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 참조를 반환 합니다.는 **통화** 개체입니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#70](../../atl/codesnippet/cpp/ccomcurrency-class_18.cpp)]  
  
##  <a name="round"></a>CComCurrency::Round  
 통화를 지정 된 소수 자릿수로 반올림 하려면이 메서드를 호출 합니다.  
  
```
HRESULT Roundint nDecimals);
```  
  
### <a name="parameters"></a>매개 변수  
 *nDecimals*  
 에 있는 자릿수 `m_currency` 0에서 4 사이의 범위에서 반올림 됩니다.  
  
### <a name="return-value"></a>반환 값  
 반환 `S_OK` 성공 또는 오류에 `HRESULT` 실패 합니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#52](../../atl/codesnippet/cpp/ccomcurrency-class_19.cpp)]  
  
##  <a name="setfraction"></a>CComCurrency::SetFraction  
 `CComCurrency` 개체의 소수 부분을 설정하려면 이 메서드를 호출합니다.  
  
```
HRESULT SetFraction(SHORT nFraction);
```  
  
### <a name="parameters"></a>매개 변수  
 *nFraction*  
 값의 소수 부분에 할당할 수는 `m_currency` 데이터 멤버입니다. 소수 부분이 부호 정수 구성 요소와 동일 해야 하며 값 범위는-에 있어야 합니다. ( **CY_MIN_FRACTION**)에서 + 9999를 ( **CY_MAX_FRACTION**).  
  
### <a name="return-value"></a>반환 값  
 반환 `S_OK` 성공 또는 오류에 `HRESULT` 실패 합니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#53](../../atl/codesnippet/cpp/ccomcurrency-class_20.cpp)]  
  
##  <a name="setinteger"></a>CComCurrency::SetInteger  
 `CComCurrency` 개체의 정수 부분을 설정하려면 이 메서드를 호출합니다.  
  
```
HRESULT SetInteger(LONGLONG nInteger);
```  
  
### <a name="parameters"></a>매개 변수  
 `nInteger`  
 값의 정수 구성 요소에 할당할 수는 `m_currency` 데이터 멤버입니다. 정수 구성 요소 부호 기호 기존 소수 부분이 일치 해야 합니다.  
  
 `nInteger`범위에 있어야 **CY_MIN_INTEGER** 를 **CY_MAX_INTEGER** 포함 합니다. 이러한 값은 atlcur.h에 정의 됩니다.  
  
### <a name="return-value"></a>반환 값  
 반환 `S_OK` 성공 또는 오류에 `HRESULT` 실패 합니다.  
  
### <a name="example"></a>예  
 [!code-cpp[NVC_ATL_Utilities#54](../../atl/codesnippet/cpp/ccomcurrency-class_21.cpp)]  
  
## <a name="see-also"></a>참고 항목  
 [COleCurrency 클래스](../../mfc/reference/colecurrency-class.md)   
 [통화](http://msdn.microsoft.com/en-us/5e81273c-7289-45c7-93c0-32c1553f708e)   
 [클래스 개요](../../atl/atl-class-overview.md)
