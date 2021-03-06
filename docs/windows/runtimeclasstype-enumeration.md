---
title: "RuntimeClassType 열거형 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords: implements/Microsoft::WRL::RuntimeClassType
dev_langs: C++
helpviewer_keywords: RuntimeClassType enumeration
ms.assetid: d380712d-672e-4ea9-b7c5-cf9fa7dbb770
caps.latest.revision: "6"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 26016e8c95807af76484504c491ca1e6e08f8f96
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="runtimeclasstype-enumeration"></a>RuntimeClassType 열거형
유형을 지정 [RuntimeClass](../windows/runtimeclass-class.md) 지원 되는 인스턴스.  
  
## <a name="syntax"></a>구문  
  
```  
enum RuntimeClassType;  
```  
  
## <a name="members"></a>멤버  
  
### <a name="values"></a>값  
  
|이름|설명|  
|----------|-----------------|  
|`ClassicCom`|클래식 COM 런타임 클래스입니다.|  
|`Delegate`|에 해당 **ClassicCom**합니다.|  
|`InhibitFtmBase`|사용 하지 않도록 설정 `FtmBase` 하는 동안 지원 `__WRL_CONFIGURATION_LEGACY__` 정의 되어 있지 않습니다.|  
|`InhibitWeakReference`|약한 참조 지원을 해제합니다.|  
|`WinRt`|Windows 런타임 클래스입니다.|  
|`WinRtClassicComMix`|`WinRt` 및 `ClassicCom`의 조합입니다.|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** implements.h  
  
 **네임스페이스:** Microsoft::WRL  
  
## <a name="see-also"></a>참고 항목  
 [Microsoft::WRL 네임스페이스](../windows/microsoft-wrl-namespace.md)