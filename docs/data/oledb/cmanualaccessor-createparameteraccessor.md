---
title: 'Cmanualaccessor:: Createparameteraccessor | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::CManualAccessor::CreateParameterAccessor
- ATL.CManualAccessor.CreateParameterAccessor
- CManualAccessor.CreateParameterAccessor
- CreateParameterAccessor
- CManualAccessor::CreateParameterAccessor
dev_langs: C++
helpviewer_keywords: CreateParameterAccessor method
ms.assetid: d0a2095b-b37c-4472-accc-45ef365a18c8
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 8ef1fc30c9188395d90171a250b96d116c2913aa
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cmanualaccessorcreateparameteraccessor"></a>CManualAccessor::CreateParameterAccessor
Bind 구조는 매개 변수에 대 한 메모리를 할당 하 고 매개 변수 데이터 멤버를 초기화 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      HRESULT CreateParameterAccessor(   
   int nBindEntries,   
   void* pBuffer,   
   DBLENGTH nBufferSize    
) throw( );  
```  
  
#### <a name="parameters"></a>매개 변수  
 `nBindEntries`  
 [in] 열의 수입니다.  
  
 `pBuffer`  
 [in] 입력된 열에는 저장 되는 버퍼에 대 한 포인터입니다.  
  
 `nBufferSize`  
 [in] 버퍼의 바이트의 크기입니다.  
  
## <a name="return-value"></a>반환 값  
 표준 중 하나 `HRESULT` 값입니다.  
  
## <a name="remarks"></a>설명  
 호출 하기 전에이 함수를 호출 해야 [AddParameterEntry](../../data/oledb/cmanualaccessor-addparameterentry.md)합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [CManualAccessor 클래스](../../data/oledb/cmanualaccessor-class.md)   
 [Cmanualaccessor:: Createaccessor](../../data/oledb/cmanualaccessor-createaccessor.md)   
 [CManualAccessor::AddParameterEntry](../../data/oledb/cmanualaccessor-addparameterentry.md)