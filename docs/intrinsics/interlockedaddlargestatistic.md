---
title: _InterlockedAddLargeStatistic | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- _InterlockedAddLargeStatistic
- _InterlockedAddLargeStatistic_cpp
dev_langs: C++
helpviewer_keywords:
- _InterlockedAddLargeStatistic intrinsic
- InterlockedAddLargeStatistic intrinsic
ms.assetid: 2802e74b-bcee-46e4-b562-894908d44409
caps.latest.revision: "14"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 1d9e61abc6ac531fe489465b1d81e167bdde5242
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="interlockedaddlargestatistic"></a>_InterlockedAddLargeStatistic
**Microsoft 전용**  
  
 첫 번째 피연산자의 64 비트 값에 연관된 추가 수행 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
long _InterlockedAddLargeStatistic(  
   __int64 volatile * Addend,  
   long Value  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [in, out] `Addend`  
 추가 작업의 첫 번째 피연산자에 대 한 포인터입니다. 가리키는 값 수의 결과로 대체 됩니다.  
  
 [in] `Value`  
 두 번째 피연산자입니다. 첫 번째 피연산자에 추가할 값입니다.  
  
## <a name="return-value"></a>반환 값  
 두 번째 피연산자의 값입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|  
|---------------|------------------|  
|`_InterlockedAddLargeStatistic`|x86|  
  
 **헤더 파일** \<. h >  
  
## <a name="remarks"></a>설명  
 별도 두 잠긴된 지침으로 구현 되기 때문에 내장 함수는 원자성 되지 않습니다. 다른 스레드에서 실행 중에 발생이 내장 함수는 원자성 64 비트 읽기 읽혀질는 일관 되지 않은 값 될 수 있습니다.  
  
 이 함수는 읽기 / 쓰기 장벽으로 작동합니다. 자세한 내용은 참조 [_ReadWriteBarrier](../intrinsics/readwritebarrier.md)합니다.  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)   
 [x86 컴파일러와 충돌](../build/conflicts-with-the-x86-compiler.md)