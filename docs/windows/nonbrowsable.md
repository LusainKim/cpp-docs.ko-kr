---
title: nonbrowsable | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: vc-attr.nonbrowsable
dev_langs: C++
helpviewer_keywords: nonbrowsable attribute
ms.assetid: e71a98e7-4b65-454a-9829-342b9f2a84be
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 279d6e80fe100fbbd41e54c4a13640e3046cf73c
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="nonbrowsable"></a>nonbrowsable
인터페이스 멤버를 속성 브라우저에 표시 되지 해야 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
[nonbrowsable]  
  
```  
  
## <a name="remarks"></a>설명  
 **nonbrowsable** c + + 특성에 동일한 기능을는 [nonbrowsable](http://msdn.microsoft.com/library/windows/desktop/aa367117) MIDL 특성입니다.  
  
## <a name="example"></a>예  
  
```  
// cpp_attr_ref_nonbrowsable.cpp  
// compile with: /LD  
#include <unknwn.h>  
[module(name="MyLib")];  
  
[object, helpstring("help string"), helpstringcontext(1),   
uuid="11111111-1111-1111-1111-111111111111"]   
__interface IMyI  
{  
   [nonbrowsable] HRESULT xx();  
};  
```  
  
## <a name="requirements"></a>요구 사항  
  
### <a name="attribute-context"></a>특성 컨텍스트  
  
|||  
|-|-|  
|**적용 대상**|인터페이스 메서드|  
|**반복 가능**|아니요|  
|**필수 특성**|없음|  
|**잘못된 특성**|없음|  
  
 특성 컨텍스트에 대한 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [IDL 특성](../windows/idl-attributes.md)   
 [메서드 특성](../windows/method-attributes.md)   
