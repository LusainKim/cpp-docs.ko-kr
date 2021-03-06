---
title: "항목 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: vc-attr.entry
dev_langs: C++
helpviewer_keywords: entry attribute
ms.assetid: ba4843e3-d7ad-4b86-9a15-0b4192f0f698
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 9ffd90ccdcce39ab73f1c1b550b466541dacf8a1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="entry"></a>entry
DLL의 진입점을 식별 하 여 모듈에서 내보낸된 함수 또는 상수를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      [ entry(  
   id  
) ]  
```  
  
#### <a name="parameters"></a>매개 변수  
 `id`  
 진입점의 ID입니다.  
  
## <a name="remarks"></a>설명  
 **항목** c + + 특성에 동일한 기능을는 [항목](http://msdn.microsoft.com/library/windows/desktop/aa366815) MIDL 특성입니다.  
  
## <a name="example"></a>예  
 예를 참조 [idl_module](../windows/idl-module.md) 의 사용 예에 대 한 **항목**합니다.  
  
## <a name="requirements"></a>요구 사항  
  
### <a name="attribute-context"></a>특성 컨텍스트  
  
|||  
|-|-|  
|**적용 대상**|`idl_module` 특성|  
|**반복 가능**|아니요|  
|**필수 특성**|없음|  
|**잘못된 특성**|없음|  
  
 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [IDL 특성](../windows/idl-attributes.md)   
