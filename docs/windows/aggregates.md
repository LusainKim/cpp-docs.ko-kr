---
title: "집계 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: vc-attr.aggregates
dev_langs: C++
helpviewer_keywords:
- aggregates attribute
- aggregation [C++]
- aggregate objects [C++], aggregates attribute
- aggregates [C++]
ms.assetid: 67a084c9-941f-474b-a029-9c93b38ebe9a
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f3fc74f10e0b5900030d48b37d1918de8807d152
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="aggregates"></a>집계
개체가 CLSID에 의해 지정된 개체를 집계함을 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      [ aggregates(  
   clsid,  
   variable_name  
) ]  
```  
  
#### <a name="parameters"></a>매개 변수  
 `clsid`  
 집계할 수 있는 개체의 CLSID를 지정합니다.  
  
 `variable_name`  
 삽입될 변수의 이름입니다. 이 변수는 집계 중인 개체의 **IUnknown** 을 포함합니다.  
  
## <a name="remarks"></a>설명  
 개체에 적용하는 경우는 **aggregates** C++ 특성은 집계 중인 개체에 대해 외부 래퍼를 구현합니다( `clsid`에 의해 지정됨).  
  
 이 특성을 사용하려면 [coclass](../windows/coclass.md), [progid](../windows/progid.md)또는 [vi_progid](../windows/vi-progid.md) 특성(또는 이 중 하나를 암시하는 다른 특성)을 동일한 요소에 적용해야 합니다. 단일 특성을 사용하는 경우 다른 두 특성도 자동으로 적용됩니다. 예를 들어 **progid** 를 적용하면 **vi_progid** 및 **coclass** 도 적용됩니다.  
  
 **ATL 프로젝트**  
  
 ATL을 사용하는 프로젝트 내에서 이 특성을 사용하는 경우 특성의 동작이 변경됩니다. 먼저 다음 항목이 대상 개체의 COM 맵에 추가됩니다.  
  
```  
COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND(_m_spAttrXXX, clsid)  
```  
  
 두 번째로 [DECLARE_GET_CONTROLLING_UNKNOWN](../atl/reference/aggregation-and-class-factory-macros.md#declare_get_controlling_unknown) 매크로도 추가됩니다.  
  
## <a name="example"></a>예  
  
```  
// cpp_attr_ref_aggregates.cpp  
// compile with: /LD  
#define _ATL_ATTRIBUTES  
#include "atlbase.h"  
#include "atlcom.h"  
  
// requires 'aggregatable.dll'  
// see aggregatable attribute to create 'aggregatable.dll'  
class DECLSPEC_UUID("1a8369cc-1c91-42c4-befa-5a5d8c9d2529") CMyClass;  
  
[module (name="MYObject")];  
[object, uuid("ab006d85-e754-47c5-9ef4-2744ff32a20c")]  
__interface IObject  
{  
};  
  
[ coclass, aggregates(__uuidof(CMyClass)),   
  uuid("91cb2c06-8931-432a-baac-206e55c4edfb")]  
struct CObject : IObject  
{  
   int i;  
};  
```  
  
## <a name="requirements"></a>요구 사항  
  
### <a name="attribute-context"></a>특성 컨텍스트  
  
|||  
|-|-|  
|**적용 대상**|**class**, `struct`|  
|**반복 가능**|예|  
|**필수 특성**|다음 중 하나 이상: **coclass**, **progid**또는 **vi_progid**.|  
|**잘못된 특성**|없음|  
  
 특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [COM 특성](../windows/com-attributes.md)   
 [클래스 특성](../windows/class-attributes.md)   
 [Typedef, Enum, Union 및 Struct 특성](../windows/typedef-enum-union-and-struct-attributes.md)   
 [집계](http://msdn.microsoft.com/library/windows/desktop/ms686558)   
 [집계할 수](http://msdn.microsoft.com/library/windows/desktop/aa366721)   
 [COM_INTERFACE_ENTRY_AUTOAGGREGATE_BLIND](../atl/reference/com-interface-entry-macros.md#com_interface_entry_autoaggregate_blind)   
 