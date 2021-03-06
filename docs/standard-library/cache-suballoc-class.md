---
title: "cache_suballoc 클래스 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- allocators/stdext::cache_suballoc
- allocators/stdext::cache_suballoc::allocate
- allocators/stdext::cache_suballoc::deallocate
dev_langs: C++
helpviewer_keywords:
- stdext::cache_suballoc
- stdext::cache_suballoc [C++], allocate
- stdext::cache_suballoc [C++], deallocate
ms.assetid: 9ea9c5e9-1dcc-45d0-b3a7-a56a93d88898
caps.latest.revision: "17"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: d53e0438d73aa73a32f26d417ea60c4540162125
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cachesuballoc-class"></a>cache_suballoc 클래스
단일 크기의 메모리 블록을 할당하고 할당 취소하는 [블록 할당자](../standard-library/allocators-header.md)를 정의합니다.  
  
## <a name="syntax"></a>구문  
  
```
template <std::size_t Sz, size_t Nelts = 20>  
class cache_suballoc
```  
  
#### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`Sz`|할당할 배열의 요소 수입니다.|  
  
## <a name="remarks"></a>설명  
 cache_suballoc 템플릿 클래스는 `freelist<sizeof(Type), max_unbounded>`를 사용하여 제한 없는 길이의 사용 가능한 목록에 할당 취소된 메모리 블록을 저장하고, 사용 가능한 목록이 비어 있는 경우 `operator new`를 사용하여 할당되어 있는 보다 큰 청크의 메모리 블록을 하위 할당합니다.  
  
 각 청크는 `operator new`와 `operator delete`에서 필요로 하는 `Sz * Nelts`바이트의 사용 가능한 메모리 및 데이터를 포함합니다. 할당된 청크는 해제되지 않습니다.  
  
### <a name="constructors"></a>생성자  
  
|||  
|-|-|  
|[cache_suballoc](#cache_suballoc)|`cache_suballoc` 형식의 개체를 생성합니다.|  
  
### <a name="member-functions"></a>멤버 함수  
  
|||  
|-|-|  
|[allocate](#allocate)|메모리 블록을 할당합니다.|  
|[deallocate](#deallocate)|지정된 위치부터 시작하여 저장소에서 지정된 개수의 개체를 해제합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<allocators>  
  
 **네임스페이스:** stdext  
  
##  <a name="allocate"></a>  cache_suballoc::allocate  
 메모리 블록을 할당합니다.  
  
```
void *allocate(std::size_t count);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`count`|할당할 배열의 요소 수입니다.|  
  
### <a name="return-value"></a>반환 값  
 할당된 개체에 대한 포인터입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="cache_suballoc"></a>  cache_suballoc::cache_suballoc  
 `cache_suballoc` 형식의 개체를 생성합니다.  
  
```
cache_suballoc();
```  
  
### <a name="remarks"></a>설명  
  
##  <a name="deallocate"></a>  cache_suballoc::deallocate  
 지정된 위치부터 시작하여 저장소에서 지정된 개수의 개체를 해제합니다.  
  
```
void deallocate(void* ptr, std::size_t count);
```  
  
### <a name="parameters"></a>매개 변수  
  
|매개 변수|설명|  
|---------------|-----------------|  
|`ptr`|저장소에서 할당을 취소할 첫 번째 개체에 대한 포인터입니다.|  
|`count`|저장소에서 할당을 취소할 개체의 수입니다.|  
  
### <a name="remarks"></a>설명  
  
## <a name="see-also"></a>참고 항목  
 [\<allocators>](../standard-library/allocators-header.md)



