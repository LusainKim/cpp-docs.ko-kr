---
title: "EventTargetArray 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: event/Microsoft::WRL::Details::EventTargetArray
dev_langs: C++
helpviewer_keywords: EventTargetArray class
ms.assetid: e3cadb7c-2160-4cbb-a2f8-c28733d1e96d
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ac591a1d27792d3b825336ed46e38fa5d002fa73
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="eventtargetarray-class"></a>EventTargetArray 클래스
WRL 인프라를 지원하며 사용자 코드에서 직접 사용할 수 없습니다.  
  
## <a name="syntax"></a>구문  
  
```  
class EventTargetArray : public Microsoft::WRL::RuntimeClass<Microsoft::WRL::RuntimeClassFlags<ClassicCom>, IUnknown>;  
```  
  
## <a name="remarks"></a>설명  
 이벤트 처리기의 배열을 나타냅니다.  
  
 와 연결 된 이벤트 처리기는 [EventSource](../windows/eventsource-class.md) 개체 EventTargetArray 보호 된 데이터 멤버에 저장 됩니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[EventTargetArray::EventTargetArray 생성자](../windows/eventtargetarray-eventtargetarray-constructor.md)|EventTargetArray 클래스의 새 인스턴스를 초기화합니다.|  
|[EventTargetArray::~EventTargetArray 소멸자](../windows/eventtargetarray-tilde-eventtargetarray-destructor.md)|현재 EventTargetArray 클래스 초기화를 취소 합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[EventTargetArray::AddTail 메서드](../windows/eventtargetarray-addtail-method.md)|이벤트 처리기의 내부 배열의 끝에 지정된 된 이벤트 처리기를 추가합니다.|  
|[EventTargetArray::Begin 메서드](../windows/eventtargetarray-begin-method.md)|이벤트 처리기의 내부 배열에서 첫 번째 요소의 주소를 가져옵니다.|  
|[EventTargetArray::End 메서드](../windows/eventtargetarray-end-method.md)|이벤트 처리기의 내부 배열에 있는 마지막 요소의 주소를 가져옵니다.|  
|[EventTargetArray::Length 메서드](../windows/eventtargetarray-length-method.md)|이벤트 처리기의 내부 배열에 있는 현재 요소 수를 가져옵니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `EventTargetArray`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** event.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## <a name="see-also"></a>참고 항목  
 [Microsoft::WRL::Details 네임스페이스](../windows/microsoft-wrl-details-namespace.md)