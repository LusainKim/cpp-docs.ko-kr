---
title: 'Cdynamicparameteraccessor:: Getparamstatus | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CDynamicParameterAccessor::GetParamStatus
- CDynamicParameterAccessor.GetParamStatus
- ATL.CDynamicParameterAccessor.GetParamStatus
- ATL::CDynamicParameterAccessor::GetParamStatus
- GetParamStatus
dev_langs: C++
helpviewer_keywords: GetParamStatus method
ms.assetid: 9300225a-616c-4a7d-82d0-8c2ecd4d8185
caps.latest.revision: "8"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: ecee1f92e1b8e5e185e1c193ae52161ab9032df8
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cdynamicparameteraccessorgetparamstatus"></a>CDynamicParameterAccessor::GetParamStatus
버퍼에 저장된 지정된 매개 변수의 상태를 검색합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      bool GetParamStatus(  
   DBORDINAL nParam,  
   DBSTATUS* pStatus  
);  
DBSTATUS* GetParamStatus(   
   DBORDINAL nParam    
) const throw( );  
```  
  
#### <a name="parameters"></a>매개 변수  
 `nParam`  
 [in] 매개 변수 번호입니다(1에서 오프셋). 매개 변수 0은 반환 값으로 예약됩니다. 매개 변수 번호는 SQL 또는 저장 프로시저 호출에서 해당 순서를 기준으로 하는 매개 변수의 인덱스입니다. 참조 [SetParam](../../data/oledb/cdynamicparameteraccessor-setparam.md) 예에 대 한 합니다.  
  
 `pStatus`  
 [out] 포함 하는 변수가에 대 한 포인터는 `DBSTATUS` 지정된 된 매개 변수의 상태입니다. 에 대 한 내용은 `DBSTATUS` 값, 참조 [상태](https://msdn.microsoft.com/en-us/library/ms722617.aspx) 에 *OLE DB Programmer's Reference*, 검색 또는 `DBSTATUS` oledb.h에서 합니다.  
  
## <a name="remarks"></a>설명  
 첫 번째 재정의 반환 **true** 성공 또는 **false** 실패 합니다. 두 번째 재정의 지정된 된 매개 변수의 상태를 포함 하는 메모리를 가리킵니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [CDynamicParameterAccessor 클래스](../../data/oledb/cdynamicparameteraccessor-class.md)