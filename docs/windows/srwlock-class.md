---
title: "SRWLock 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: corewrappers/Microsoft::WRL::Wrappers::SRWLock
dev_langs: C++
helpviewer_keywords: SRWLock class
ms.assetid: 4fa250e3-5f29-4b06-ac24-61b6c04ade93
caps.latest.revision: "5"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 1325a089739b3820009aa239f56805264dbb6b83
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="srwlock-class"></a>SRWLock 클래스
슬림 판독기/작성기 잠금을 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
class SRWLock;  
```  
  
## <a name="remarks"></a>설명  
 슬림 판독기/작성기 잠금은는 스레드에서 개체 또는 리소스에 대 한 액세스를 동기화에 사용 됩니다. 자세한 내용은 참조 [동기화 함수](http://msdn.microsoft.com/en-us/9b6359c2-0113-49b6-83d0-316ad95aba1b)합니다.  
  
## <a name="members"></a>멤버  
  
### <a name="public-typedefs"></a>공용 Typedefs  
  
|||  
|-|-|  
|**SyncLockExclusive**|배타 모드에 획득 된 SRWLock 개체에 대 한 동의어입니다.|  
|**SyncLockShared**|공유 모드에서 획득 된 SRWLock 개체에 대 한 동의어입니다.|  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[SRWLock::SRWLock 생성자](../windows/srwlock-srwlock-constructor.md)|SRWLock 클래스의 새 인스턴스를 초기화합니다.|  
|[SRWLock::~SRWLock 소멸자](../windows/srwlock-tilde-srwlock-destructor.md)|SRWLock 클래스의 인스턴스 초기화를 취소합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[SRWLock::LockExclusive 메서드](../windows/srwlock-lockexclusive-method.md)|단독 모드의 SRWLock 개체를 가져옵니다.|  
|[SRWLock::LockShared 메서드](../windows/srwlock-lockshared-method.md)|공유 모드의 SRWLock 개체를 가져옵니다.|  
|[SRWLock::TryLockExclusive 메서드](../windows/srwlock-trylockexclusive-method.md)|현재 또는 지정 된 SRWLock 개체에 대 한 단독 모드의 SRWLock 개체를 얻으려고 합니다.|  
|[SRWLock::TryLockShared 메서드](../windows/srwlock-trylockshared-method.md)|현재 또는 지정된 SRWLock 개체에 대해 공유 모드의 SRWLock 개체를 가져오기 위한 시도입니다.|  
  
### <a name="protected-data-member"></a>보호 된 데이터 멤버  
  
|name|설명|  
|----------|-----------------|  
|[SRWLock::SRWLock_ 데이터 멤버](../windows/srwlock-srwlock-data-member.md)|현재 SRWLock 개체에 대한 기본 잠금 변수를 포함합니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `SRWLock`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## <a name="see-also"></a>참고 항목  
 [Microsoft::WRL::Wrappers 네임스페이스](../windows/microsoft-wrl-wrappers-namespace.md)