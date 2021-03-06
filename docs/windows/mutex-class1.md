---
title: "뮤텍스 Class1 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: corewrappers/Microsoft::WRL::Wrappers::Mutex
dev_langs: C++
helpviewer_keywords: Mutex class
ms.assetid: 682a0963-721c-46a2-8871-000e9997505b
caps.latest.revision: "4"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: c0e849d1fee7eca67f3b5765d31b54e0660eaa25
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="mutex-class1"></a>뮤텍스 Class1
공유 리소스를 단독으로 제어하는 동기화 개체를 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
class Mutex : public HandleT<HandleTraits::MutexTraits>  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-typedefs"></a>공용 Typedefs  
  
|이름|설명|  
|----------|-----------------|  
|**SyncLock**|동기 잠금을 지원 되는 클래스에 대 한 동의어입니다.|  
  
### <a name="public-constructor"></a>Public 생성자  
  
|name|설명|  
|----------|-----------------|  
|[Mutex::Mutex 생성자](../windows/mutex-mutex-constructor.md)|Mutex 클래스의 새 인스턴스를 초기화합니다.|  
  
### <a name="public-members"></a>공용 멤버  
  
|name|설명|  
|----------|-----------------|  
|[Mutex::Lock 메서드](../windows/mutex-lock-method.md)|현재 개체 또는 지정 된 핸들과 연결 된 뮤텍스 개체 될 때까지 대기는 뮤텍스를 해제 하거나 지정한 시간 제한 간격이 경과 합니다.|  
  
### <a name="public-operator"></a>Public 연산자  
  
|name|설명|  
|----------|-----------------|  
|[Mutex::operator= 연산자](../windows/mutex-operator-assign-operator.md)|현재 Mutex 개체를 할당 합니다 (이동) 지정 된 뮤텍스 개체입니다.|  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 `Mutex`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** corewrappers.h  
  
 **Namespace:** Microsoft::WRL::Wrappers  
  
## <a name="see-also"></a>참고 항목  
 [Microsoft::WRL::Wrappers 네임스페이스](../windows/microsoft-wrl-wrappers-namespace.md)