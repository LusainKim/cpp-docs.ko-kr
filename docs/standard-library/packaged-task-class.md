---
title: "packaged_task 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- future/std::packaged_task
- future/std::packaged_task::packaged_task
- future/std::packaged_task::get_future
- future/std::packaged_task::make_ready_at_thread_exit
- future/std::packaged_task::reset
- future/std::packaged_task::swap
- future/std::packaged_task::valid
- future/std::packaged_task::operator()
- future/std::packaged_task::operator bool
dev_langs: C++
ms.assetid: 0a72cbe3-f22a-4bfe-8e50-dcb268c98780
caps.latest.revision: "9"
author: corob-msft
ms.author: corob
manager: ghogen
helpviewer_keywords:
- std::packaged_task [C++]
- std::packaged_task [C++], packaged_task
- std::packaged_task [C++], get_future
- std::packaged_task [C++], make_ready_at_thread_exit
- std::packaged_task [C++], reset
- std::packaged_task [C++], swap
- std::packaged_task [C++], valid
ms.workload: cplusplus
ms.openlocfilehash: e060a7d9a73cd275810541fc57ad34a2c62c4097
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="packagedtask-class"></a>packaged_task 클래스
*비동기 공급자*(해당 호출 시그니처가 `Ty(ArgTypes...)`인 호출 래퍼)를 설명합니다. 비동기 공급자의 *연결된 비동기 상태*에는 잠재적 결과와 함께 호출 가능 개체의 복사본이 포함됩니다.  
  
## <a name="syntax"></a>구문  
  
```
template <class>
class packaged_task;
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[packaged_task](#packaged_task)|`packaged_task` 개체를 생성합니다.|  
|[packaged_task::~packaged_task 소멸자](#dtorpackaged_task_destructor)|`packaged_task` 개체를 제거합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[get_future](#get_future)|동일한 연결된 비동기 상태가 있는 [future](../standard-library/future-class.md) 개체를 반환합니다.|  
|[make_ready_at_thread_exit](#make_ready_at_thread_exit)|연결된 비동기 상태에 저장되어 있는 호출 가능 개체를 호출하고 반환된 값을 원자 단위로 저장합니다.|  
|[reset](#reset)|연결된 비동기 상태를 대체합니다.|  
|[swap](#swap)|연결된 비동기 상태를 지정한 개체의 연결된 비동기 상태와 교환합니다.|  
|[유효한](#valid)|개체에 연결된 비동기 상태가 있는지를 지정합니다.|  
  
### <a name="public-operators"></a>Public 연산자  
  
|이름|설명|  
|----------|-----------------|  
|[packaged_task::operator=](#op_eq)|지정된 개체에서 연결된 비동기 상태를 전송합니다.|  
|[packaged_task::operator()](#op_call)|연결된 비동기 상태에 저장되어 있는 호출 가능 개체를 호출하고 반환된 값을 원자 단위로 저장한 후에 상태를 *ready*로 설정합니다.|  
|[packaged_task::operator bool](#op_bool)|개체에 연결된 비동기 상태가 있는지를 지정합니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<이후 >  
  
 **네임스페이스:** std  
  
##  <a name="get_future"></a>  packaged_task::get_future  
 동일한 *연결된 비동기 상태*가 있는 `future<Ty>` 형식의 개체를 반환합니다.  
  
```
future<Ty> get_future();
```  
  
### <a name="remarks"></a>설명  
 `packaged_task` 개체에 연결된 비동기 상태가 없는 경우 이 메서드는 오류 코드가 `no_state`인 [future_error](../standard-library/future-error-class.md)를 throw합니다.  
  
 이 메서드는 연결된 비동기 상태가 동일한 `packaged_task` 개체에 대해 이미 호출된 경우 오류 코드가 `future_already_retrieved`인 `future_error`를 thorw합니다.  
  
##  <a name="make_ready_at_thread_exit"></a>  packaged_task::make_ready_at_thread_exit  
 *연결된 비동기 상태*에 저장되어 있는 호출 가능 개체를 호출하고 반환된 값을 원자 단위로 저장합니다.  
  
```
void make_ready_at_thread_exit(ArgTypes... args);
```  
  
### <a name="remarks"></a>설명  
 `packaged_task` 개체에 연결된 비동기 상태가 없는 경우 이 메서드는 오류 코드가 `no_state`인 [future_error](../standard-library/future-error-class.md)를 throw합니다.  
  
 이 메서드 또는 [make_ready_at_thread_exit](#make_ready_at_thread_exit)가 동일한 연관 비동기 상태의 `packaged_task` 개체에 대해 이미 호출된 경우 이 메서드는 오류 코드가 `promise_already_satisfied`인 `future_error`를 throw합니다.  
  
 그렇지 않으면 이 연산자는 `INVOKE(fn, args..., Ty)`를 호출합니다. 여기서 *fn*은 연결된 비동기 상태에 저장되어 있는 호출 가능 개체입니다. 반환된 모든 값은 연결된 비동기 상태에서 반환된 결과로 원자 단위로 저장됩니다.  
  
 [packaged_task::operator()](#op_call)와 달리 호출 스레드에서 모든 스레드 로컬 개체가 제거될 때까지는 연결된 비동기 상태가 `ready`로 설정되지 않습니다. 일반적으로 연결된 비동기 상태에서 차단된 스레드는 호출 스레드가 종료될 때까지 차단 해제되지 않습니다.  
  
##  <a name="op_eq"></a>  packaged_task::operator=  
 지정된 개체에서 *연결된 비동기 상태*를 전송합니다.  
  
```
packaged_task& operator=(packaged_task&& Right);
```  
  
### <a name="parameters"></a>매개 변수  
 `Right`  
 `packaged_task` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
 `*this`  
  
### <a name="remarks"></a>설명  
 작업 후 `Right`에는 더 이상 연결된 비동기 상태가 없습니다.  
  
##  <a name="op_call"></a>  packaged_task::operator()  
 *연결된 비동기 상태*에 저장되어 있는 호출 가능 개체를 호출하고 반환된 값을 원자 단위로 저장한 후에 상태를 *ready*로 설정합니다.  
  
```
void operator()(ArgTypes... args);
```  
  
### <a name="remarks"></a>설명  
 `packaged_task` 개체에 연결된 비동기 상태가 없는 경우 이 메서드는 오류 코드가 `no_state`인 [future_error](../standard-library/future-error-class.md)를 throw합니다.  
  
 이 메서드 또는 [make_ready_at_thread_exit](#make_ready_at_thread_exit)가 동일한 연관 비동기 상태의 `packaged_task` 개체에 대해 이미 호출된 경우 이 메서드는 오류 코드가 `promise_already_satisfied`인 `future_error`를 throw합니다.  
  
 그렇지 않으면 이 연산자는 `INVOKE(fn, args..., Ty)`를 호출합니다. 여기서 *fn*은 연결된 비동기 상태에 저장되어 있는 호출 가능 개체입니다. 반환된 모든 값은 연결된 비동기 상태에서 반환된 결과로 원자 단위로 저장되며 상태는 ready로 설정됩니다. 그 결과로 연결된 비동기 상태에서 차단된 모든 스레드의 차단은 해제됩니다.  
  
##  <a name="op_bool"></a>  packaged_task::operator bool  
 개체에 `associated asynchronous state`가 있는지를 지정합니다.  
  
```
operator bool() const noexcept;
```  
  
### <a name="return-value"></a>반환 값  
 개체가 연결된 비동기 상태이면 `true`이고, 그렇지 않으면 `false`입니다.  
  
##  <a name="packaged_task"></a>  packaged_task::packaged_task 생성자  
 `packaged_task` 개체를 생성합니다.  
  
```
packaged_task() noexcept;
packaged_task(packaged_task&& Right) noexcept;
template <class Fn>
   explicit packaged_task(Fn&& fn);

template <class Fn, class Alloc>
   explicit packaged_task(
      allocator_arg_t, const Alloc& alloc, Fn&& fn);
```  
  
### <a name="parameters"></a>매개 변수  
 `Right`  
 `packaged_task` 개체입니다.  
  
 `alloc`  
 메모리 할당자입니다. 자세한 내용은 [\<allocators>](../standard-library/allocators-header.md)를 참조하세요.  
  
 `fn`  
 함수 개체입니다.  
  
### <a name="remarks"></a>설명  
 첫 번째 생성자는 *연결된 비동기 상태*가 없는 `packaged_task` 개체를 생성합니다.  
  
 두 번째 생성자는 `packaged_task` 개체를 생성하며 `Right`로부터 연결된 비동기 상태를 전송합니다. 작업 후 `Right`에는 더 이상 연결된 비동기 상태가 없습니다.  
  
 세 번째 생성자는 연결된 비동기 상태로 저장된 `packaged_task`의 복사본이 있는 `fn` 개체를 생성합니다.  
  
 네 번째 생성자는 비동기적 연결 상태로 저장된 `packaged_task`의 복사본이 있는 `fn` 개체를 생성하고, 메모리 할당을 위해 `alloc`을 사용합니다.  
  
##  <a name="dtorpackaged_task_destructor"></a>  packaged_task::~packaged_task 소멸자  
 `packaged_task` 개체를 제거합니다.  
  
```
~packaged_task();
```  
  
### <a name="remarks"></a>설명  
 *연결된 비동기 상태*가 *ready* 상태가 아니면 소멸자는 오류 코드가 `broken_promise`인 [future_error](../standard-library/future-error-class.md) 예외를 연결된 비동기 상태에 결과로 저장하며, 연결된 비동기 상태에서 차단되었던 모든 스레드의 차단은 해제됩니다.  
  
##  <a name="reset"></a>  packaged_task::reset  
 기존의 *연결된 비동기 상태*를 교체할 새 연결된 비동기 상태를 만듭니다.  
  
```
void reset();
```  
  
### <a name="remarks"></a>설명  
 실제로 이 메서드는 `*this = packaged_task(move(fn))`를 실행합니다. 여기서 *fn*은 이 개체에 대한 연결된 비동기 상태에 저장되는 함수 개체입니다. 따라서 개체의 상태는 지워지며 새로 생성한 개체에 대해 호출하는 것처럼 [get_future](#get_future), [operator()](#op_call) 및 [make_ready_at_thread_exit](#make_ready_at_thread_exit)를 호출할 수 있습니다.  
  
##  <a name="swap"></a>  packaged_task::swap  
 연결된 비동기 상태를 지정한 개체의 연결된 비동기 상태와 교환합니다.  
  
```
void swap(packaged_task& Right) noexcept;
```  
  
### <a name="parameters"></a>매개 변수  
 `Right`  
 `packaged_task` 개체입니다.  
  
##  <a name="valid"></a>  packaged_task::valid  
 개체에 `associated asynchronous state`가 있는지를 지정합니다.  
  
```
bool valid() const;
```  
  
### <a name="return-value"></a>반환 값  
 개체가 연결된 비동기 상태이면 `true`이고, 그렇지 않으면 `false`입니다.  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [\<future>](../standard-library/future.md)



