---
title: "메모리 할당 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: c.memory
dev_langs: C++
helpviewer_keywords:
- memory allocation, routines
- memory, managing
- memory, allocation
ms.assetid: b4470556-a128-4782-9943-2ccf7a7d9979
caps.latest.revision: "10"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: e419cbd30b523121ae1902b49a25d60c0b9d21eb
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: HT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="memory-allocation"></a>메모리 할당
다음 루틴을 사용하여 메모리를 할당, 확보 및 다시 할당합니다.  
  
### <a name="memory-allocation-routines"></a>메모리 할당 루틴  
  
|루틴|사용|  
|-------------|---------|  
|[_alloca](../c-runtime-library/reference/alloca.md), [_malloca](../c-runtime-library/reference/malloca.md)|스택에서 메모리 할당|  
|[calloc](../c-runtime-library/reference/calloc.md)|할당된 블록에서 모든 바이트를 0으로 초기화하는 배열에 저장소 할당|  
|[_calloc_dbg](../c-runtime-library/reference/calloc-dbg.md)|`calloc`의 디버그 버전,런타임 라이브러리의 디버그 버전에서만 사용 가능|  
|[operator delete](../c-runtime-library/operator-delete-crt.md)|할당된 블록 확보|  
|[operator delete&#91;&#93;](../c-runtime-library/delete-operator-crt.md)|할당된 블록 확보|  
|[_expand](../c-runtime-library/reference/expand.md)|이동하지 않고 메모리 블록을 확장명 또는 축소|  
|[_expand_dbg](../c-runtime-library/reference/expand-dbg.md)|`_expand`의 디버그 버전,런타임 라이브러리의 디버그 버전에서만 사용 가능|  
|[free](../c-runtime-library/reference/free.md)|할당된 블록 확보|  
|[_free_dbg](../c-runtime-library/reference/free-dbg.md)|`free`의 디버그 버전,런타임 라이브러리의 디버그 버전에서만 사용 가능|  
|[_freea](../c-runtime-library/reference/freea.md)|스택에서 할당된 블록 확보|  
|[_get_heap_handle](../c-runtime-library/reference/get-heap-handle.md)|CRT 힙의 Win32 HANDLE을 가져옵니다.|  
|[_heapadd](../c-runtime-library/heapadd.md)|힙에 메모리 추가|  
|[_heapchk](../c-runtime-library/reference/heapchk.md)|일관성을 위한 힙 검사|  
|[_heapmin](../c-runtime-library/reference/heapmin.md)|힙에서 사용하지 않는 메모리 해제|  
|[_heapset](../c-runtime-library/heapset.md)|지정된 값으로 빈 힙 항목 채우기|  
|[_heapwalk](../c-runtime-library/reference/heapwalk.md)|힙의 각 항목에 대한 정보 반환|  
|[malloc](../c-runtime-library/reference/malloc.md)|힙에서 메모리 블록 할당|  
|[_malloc_dbg](../c-runtime-library/reference/malloc-dbg.md)|`malloc`의 디버그 버전,런타임 라이브러리의 디버그 버전에서만 사용 가능|  
|[_msize](../c-runtime-library/reference/msize.md)|할당된 블록 크기 반환|  
|[_msize_dbg](../c-runtime-library/reference/msize-dbg.md)|`_msize`의 디버그 버전,런타임 라이브러리의 디버그 버전에서만 사용 가능|  
|[new](../c-runtime-library/operator-new-crt.md)|힙에서 메모리 블록 할당|  
|[new&#91;&#93;](../c-runtime-library/new-operator-crt.md)|힙에서 메모리 블록 할당|  
|[_query_new_handler](../c-runtime-library/reference/query-new-handler.md)|`_set_new_handler`가 설정한 대로 현재 새 처리기 루틴 주소 반환|  
|[_query_new_mode](../c-runtime-library/reference/query-new-mode.md)|`_set_new_mode`에 대한 `malloc`로 설정된 새 처리기 모드를 나타내는 정수 반환|  
|[realloc](../c-runtime-library/reference/realloc.md)|새 크기로 블록 다시 할당|  
|[_realloc_dbg](../c-runtime-library/reference/realloc-dbg.md)|`realloc`의 디버그 버전,런타임 라이브러리의 디버그 버전에서만 사용 가능|  
|[_set_new_handler](../c-runtime-library/reference/set-new-handler.md)|`new` 연산자가 메모리 할당에 실패하고 C++ 표준 라이브러리의 컴파일을 사용하도록 설정한 경우 오류 처리 메커니즘 사용|  
|[_set_new_mode](../c-runtime-library/reference/set-new-mode.md)|`malloc`에 대해 새 처리기 모드 설정|  
  
## <a name="see-also"></a>참고 항목  
 [범주별 런타임 루틴](../c-runtime-library/run-time-routines-by-category.md)