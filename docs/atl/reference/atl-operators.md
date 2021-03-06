---
title: "ATL 연산자 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: 'index-page '
dev_langs: C++
helpviewer_keywords: operators [ATL]
ms.assetid: 58ccd252-2869-45ee-8a5c-3ca40ee7f8a2
caps.latest.revision: "16"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: bcd8ce5e46617958f0188a3563771061a37d22c6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="atl-operators"></a>ATL 연산자
이 섹션에는 ATL 전역 연산자에 대 한 참조 항목이 포함 되어 있습니다.  
  
|연산자|설명|  
|--------------|-----------------|  
|[연산자 = =](#operator_eq_eq)|두 `CSid` 개체 또는 `SID` 같음에 대 한 구조입니다.|  
|[operator! =](#operator_neq)|두 `CSid` 개체 또는 `SID` 같지 않음에 대 한 구조입니다.|  
|[연산자 <](#operator_lt)|테스트는 `CSid` 개체 또는 `SID` 연산자의 왼쪽에는 구조는 보다 작은 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.|  
|[연산자 >](#operator_gt)|테스트는 `CSid` 개체 또는 `SID` 연산자의 좌 변에 구조 보다 크면는 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.|  
|[연산자 < =](#operator_lt__eq)|테스트는 `CSid` 개체 또는 `SID` 연산자의 좌 변에 구조 보다 작거나 같음는 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.|  
|[연산자 > =](#operator_gt__eq)|테스트는 `CSid` 개체 또는 `SID` 보다 크거나 같음 연산자의 왼쪽에는 구조는는 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atlsecurity.h 합니다.  
  
##  <a name="operator_eq_eq"></a>연산자 = =  
 비교 `CSid` 개체 또는 `SID` 같음에 대 한 구조 (보안 식별자)입니다.  
  
```   
bool operator==(const CSid& lhs, const CSid& rhs) throw(); 
```  
  
### <a name="parameters"></a>매개 변수  
 `lhs`  
 첫 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
 `rhs`  
 두 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 개체가 동일 하면 **false** 경우 같지 않은 것입니다.  
  
##  <a name="operator_neq"></a>operator! =  
 비교 `CSid` 개체 또는 `SID` 같지 않음에 대 한 구조 (보안 식별자)입니다.  
  
```   
bool operator==(const CSid& lhs, const CSid& rhs) throw(); 
```  
  
### <a name="parameters"></a>매개 변수  
 `lhs`  
 첫 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
 `rhs`  
 두 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 개체가 같지 않으면 **false** 같으면 합니다.  
  
##  <a name="operator_lt"></a>연산자 <  
 테스트는 `CSid` 개체 또는 `SID` 연산자의 왼쪽에는 구조는 보다 작은 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.  
  
```   
bool operator<(const CSid& lhs, const CSid& rhs) throw(); 
```  
  
### <a name="parameters"></a>매개 변수  
 `lhs`  
 첫 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
 `rhs`  
 두 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 경우의 주소는 `lhs` 개체의 주소 보다 작으면는 `rhs` 개체 **false** 그렇지 않은 경우.  
  
### <a name="remarks"></a>설명  
 이 연산자의 주소에 적용 된 `CSid` 개체 또는 `SID` 구조체와 c + + 표준 라이브러리 컬렉션 클래스와의 호환성을 제공 하기 위해 구현 됩니다.  
  
##  <a name="operator_gt"></a>연산자 >  
 테스트는 `CSid` 개체 또는 `SID` 연산자의 좌 변에 구조 보다 크면는 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.  
  
```   
bool operator<(const CSid& lhs, const CSid& rhs) throw(); 
```  
  
### <a name="parameters"></a>매개 변수  
 `lhs`  
 첫 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
 `rhs`  
 두 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 경우의 주소는 `lhs` 의 주소 보다 큰는 `rhs`, **false** 그렇지 않은 경우.  
  
### <a name="remarks"></a>설명  
 이 연산자의 주소에 적용 된 `CSid` 개체 또는 `SID` 구조체와 c + + 표준 라이브러리 컬렉션 클래스와의 호환성을 제공 하기 위해 구현 됩니다.  
  
##  <a name="operator_lt__eq"></a>연산자 < =  
 테스트는 `CSid` 개체 또는 `SID` 연산자의 좌 변에 구조 보다 작거나 같음는 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.  
  
```   
bool operator<(const CSid& lhs, const CSid& rhs) throw(); 
```  
  
### <a name="parameters"></a>매개 변수  
 `lhs`  
 첫 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
 `rhs`  
 두 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 경우의 주소는 `lhs` 보다 작거나 같으면의 주소에는 `rhs`, **false** 그렇지 않은 경우.  
  
### <a name="remarks"></a>설명  
 이 연산자의 주소에 적용 된 `CSid` 개체 또는 `SID` 구조체와 c + + 표준 라이브러리 컬렉션 클래스와의 호환성을 제공 하기 위해 구현 됩니다.  
  
##  <a name="operator_gt__eq"></a>연산자 > =  
 테스트는 `CSid` 개체 또는 `SID` 보다 크거나 같음 연산자의 왼쪽에는 구조는는 `CSid` 개체 또는 `SID` (c + + 표준 라이브러리 호환성)에 대 한 오른쪽에는 구조입니다.  
  
```   
bool operator<(const CSid& lhs, const CSid& rhs) throw(); 
```  
  
### <a name="parameters"></a>매개 변수  
 `lhs`  
 첫 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
 `rhs`  
 두 번째 `CSid` 개체 또는 `SID` 비교할 구조체입니다.  
  
### <a name="return-value"></a>반환 값  
 반환 **true** 경우의 주소는 `lhs` 의 주소로 보다 크거나는 `rhs`, **false** 그렇지 않은 경우.  
  
### <a name="remarks"></a>설명  
 이 연산자의 주소에 적용 된 `CSid` 개체 또는 `SID` 구조체와 c + + 표준 라이브러리 컬렉션 클래스와의 호환성을 제공 하기 위해 구현 됩니다.



