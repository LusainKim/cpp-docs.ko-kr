---
title: "is_trivially_default_constructible 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: type_traits/std::is_trivially_default_constructible
dev_langs: C++
helpviewer_keywords: is_trivially_default_constructible
ms.assetid: 653ecd73-909f-4dd8-b95a-d1164d1c2da4
caps.latest.revision: "17"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6b936e6cfa3557591a5be9ec2cafda36920039c3
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="istriviallydefaultconstructible-class"></a>is_trivially_default_constructible 클래스
형식에 Trivial 기본 생성자가 있는지 여부를 테스트합니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class Ty>
struct is_trivially_default_constructible;
```  
  
#### <a name="parameters"></a>매개 변수  
 `Ty`  
 형식이 쿼리입니다.  
  
## <a name="remarks"></a>설명  
 형식 조건자의 인스턴스는 `Ty` 형식이 Trivial 생성자가 있는 클래스인 경우 true이고 그렇지 않은 경우 false입니다.  
  
 클래스 `Ty`에 대한 기본 생성자는 다음의 경우 Trivial입니다.  
  
-   암시적으로 선언된 기본 생성자인 경우  
  
-   클래스 `Ty`에 가상 함수가 없는 경우  
  
-   클래스 `Ty`에 가상 기본이 없는 경우  
  
-   클래스 `Ty`의 모든 직접 기본에 Trivial 생성자가 있는 경우  
  
-   클래스 형식의 모든 비정적 데이터 멤버의 클래스에 Trivial 생성자가 있는 경우  
  
-   클래스 배열 형식의 모든 비정적 데이터 멤버의 클래스에 Trivial 생성자가 있는 경우  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<type_traits>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [<type_traits>](../standard-library/type-traits.md)



