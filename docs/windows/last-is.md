---
title: last_is | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: vc-attr.last_is
dev_langs: C++
helpviewer_keywords: last_is attribute
ms.assetid: 9e045ac0-fa38-4249-af55-67bde5d0a58c
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 7d7a230299a94ba33a142ca44ebc34981f7201ac
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="lastis"></a>last_is
전송할 마지막 배열 요소의 인덱스를 지정 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      [ last_is(  
   "expression"  
) ]  
```  
  
#### <a name="parameters"></a>매개 변수  
 *식*  
 하나 이상의 C 언어 식입니다. 빈 인수 슬롯 허용 됩니다.  
  
## <a name="remarks"></a>설명  
 **last_is** c + + 특성에 동일한 기능을는 [last_is](http://msdn.microsoft.com/library/windows/desktop/aa367066) MIDL 특성입니다.  
  
## <a name="example"></a>예  
 참조 [first_is](../windows/first-is.md) 배열 섹션을 지정 하는 방법의 예입니다.  
  
## <a name="requirements"></a>요구 사항  
  
### <a name="attribute-context"></a>특성 컨텍스트  
  
|||  
|-|-|  
|**적용 대상**|필드에 `struct` 또는 **union**, 매개 변수 인터페이스, 인터페이스 메서드|  
|**반복 가능**|아니요|  
|**필수 특성**|없음|  
|**잘못된 특성**|없음|  
  
 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [IDL 특성](../windows/idl-attributes.md)   
 [Typedef, Enum, Union 및 Struct 특성](../windows/typedef-enum-union-and-struct-attributes.md)   
 [매개 변수 특성](../windows/parameter-attributes.md)   
 [first_is](../windows/first-is.md)   
 [max_is](../windows/max-is.md)   
 [length_is](../windows/length-is.md)   
 [size_is](../windows/size-is.md)   
