---
title: lcid | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: language-reference
f1_keywords: vc-attr.lcid
dev_langs: C++
helpviewer_keywords: LCID attribute
ms.assetid: 7f248c69-ee1c-42c3-9411-39cf27c9f43d
caps.latest.revision: "10"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: 36ccb085c2f6128012d446f6be15dff94c718e35
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="lcid"></a>lcid
로캘 식별자는 함수에 전달할 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
[lcid]  
  
```  
  
## <a name="remarks"></a>설명  
 **lcid** 의 기능을 구현 하는 c + + 특성은 [lcid](http://msdn.microsoft.com/library/windows/desktop/aa367067) MIDL 특성입니다. 사용 하 여 라이브러리 블록에 대 한 로캘을 구현 하려는 경우는 **lcid =** `lcid` 매개 변수를는 [모듈](../windows/module-cpp.md) 특성입니다.  
  
## <a name="example"></a>예  
  
```  
// cpp_attr_ref_lcid.cpp  
// compile with: /LD  
#include <unknwn.h>  
[module(name="MyLibrary")];  
typedef long HRESULT;  
  
[dual, uuid("2F5F63F1-16DA-11d2-9E7B-00C04FB926DA")]  
__interface IStatic {  
   HRESULT MyFunc([in, lcid] long LocaleID, [out, retval] BSTR * ReturnVal);  
};  
```  
  
## <a name="requirements"></a>요구 사항  
  
### <a name="attribute-context"></a>특성 컨텍스트  
  
|||  
|-|-|  
|**적용 대상**|인터페이스 매개 변수|  
|**반복 가능**|아니요|  
|**필수 특성**|없음|  
|**잘못된 특성**|없음|  
  
 자세한 내용은 [특성 컨텍스트](../windows/attribute-contexts.md)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [IDL 특성](../windows/idl-attributes.md)   
 [매개 변수 특성](../windows/parameter-attributes.md)   
