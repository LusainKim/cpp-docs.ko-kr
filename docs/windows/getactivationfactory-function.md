---
title: "GetActivationFactory 함수 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::GetActivationFactory
- client/ABI::Windows::Foundation::GetActivationFactory
- client/Windows::Foundation::GetActivationFactory
dev_langs: C++
helpviewer_keywords: GetActivationFactory function
ms.assetid: 5736d285-6beb-42aa-8788-e261c0010afe
caps.latest.revision: "4"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 6419ef4d48c3f151f8acfb49d40e10853f5d17f7
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="getactivationfactory-function"></a>GetActivationFactory 함수
템플릿 매개 변수로 지정 된 형식에 대 한 한 활성화 팩터리를 검색 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template<  
   typename T  
>  
inline HRESULT GetActivationFactory(  
   _In_ HSTRING activatableClassId,  
   _Out_ Microsoft::WRL::Details::ComPtrRef<T> factory  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 `T`  
 활성화 팩터리 형식을 지정 하는 템플릿 매개 변수입니다.  
  
 `activatableClassId`  
 활성화 팩터리를 생성할 수 있는 클래스의 이름입니다.  
  
 `factory`  
 이 작업이 완료 될 때, 형식에 대 한 활성화 팩터리에 대 한 참조 `T`합니다.  
  
## <a name="return-value"></a>반환 값  
 성공 하면 s_ok이 고 그렇지 않은 경우이 작업이 실패 한 이유를 나타내는 HRESULT 오류가 발생 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** client.h  
  
 **Namespace:** windows:: foundation  
  
## <a name="see-also"></a>참고 항목  
 [Windows::Foundation 네임스페이스](../windows/windows-foundation-namespace.md)