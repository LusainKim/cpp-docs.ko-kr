---
title: "is_assignable 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: type_traits/std::is_assignable
dev_langs: C++
helpviewer_keywords: is_assignable
ms.assetid: 53444287-c8be-4ad2-9487-a85c066a4f84
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: ba99c19328b576900b1c269c24949baa832c8be7
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="isassignable-class"></a>is_assignable 클래스
`From` 형식의 값을 `To` 형식에 할당할 수 있는지 여부를 테스트합니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class To, class From>  
struct is_assignable;
```  
  
#### <a name="parameters"></a>매개 변수  
 후  
 할당을 받는 개체의 형식입니다.  
  
 보낸 사람  
 값을 제공하는 개체의 형식입니다.  
  
## <a name="remarks"></a>설명  
 평가되지 않은 `declval<To>() = declval<From>()` 식은 올바른 형식이어야 합니다. `From`과 `To`는 둘 다 완전한 형식이거나, `void`이거나, 범위를 알 수 없는 배열이어야 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<type_traits>  
  
 **네임스페이스:** std  
  
## <a name="see-also"></a>참고 항목  
 [<type_traits>](../standard-library/type-traits.md)



