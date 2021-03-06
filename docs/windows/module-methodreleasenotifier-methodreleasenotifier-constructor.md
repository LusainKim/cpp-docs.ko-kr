---
title: "Module::MethodReleaseNotifier::MethodReleaseNotifier 생성자 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: module/Microsoft::WRL::Module::MethodReleaseNotifier::MethodReleaseNotifier
dev_langs: C++
helpviewer_keywords: MethodReleaseNotifier, constructor
ms.assetid: 762e2ca4-0a92-49de-9ff5-d3efa0f067c0
caps.latest.revision: "3"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 045dd8dd0dbee58c0feea33bc7ce4f6cea30e591
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="modulemethodreleasenotifiermethodreleasenotifier-constructor"></a>Module::MethodReleaseNotifier::MethodReleaseNotifier 생성자
Module:: methodreleasenotifier 클래스의 새 인스턴스를 초기화합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
MethodReleaseNotifier(  
   _In_ T* object,   
   _In_ void (T::* method)(),   
   bool release) throw() :  
            ReleaseNotifier(release), object_(object),   
            method_(method);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `object`  
 개체 멤버 함수가 이벤트 처리기입니다.  
  
 `method`  
 멤버 함수 매개 변수의 `object` 이벤트 처리기입니다.  
  
 `release`  
 지정 `true` 내부 호출을 사용 하도록 설정 하려면 [모듈:: ReleaseNotifier::Release()](../windows/module-releasenotifier-release.md) 메서드도 있습니다; 그렇지 않으면 지정 `false`합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** module.h  
  
 **네임스페이스:** Microsoft::WRL  
  
## <a name="see-also"></a>참고 항목  
 [Module::MethodReleaseNotifier 클래스](../windows/module-methodreleasenotifier-class.md)