---
title: 'Cmanualaccessor:: Addparameterentry | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- CManualAccessor::AddParameterEntry
- ATL.CManualAccessor.AddParameterEntry
- CManualAccessor.AddParameterEntry
- AddParameterEntry
- ATL::CManualAccessor::AddParameterEntry
dev_langs: C++
helpviewer_keywords: AddParameterEntry method
ms.assetid: 9048b164-052b-41b1-a861-227fc529e0b5
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 66c88bf072cbae6c86949d52ded121dd694c0e97
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cmanualaccessoraddparameterentry"></a>CManualAccessor::AddParameterEntry
매개 변수 항목 구조를 매개 변수 항목을 추가합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      void AddParameterEntry(  
   DBORDINAL nOrdinal,  
   DBTYPE wType,  
   DBLENGTH nColumnSize,  
   void* pData,  
   void* pLength = NULL,  
   void* pStatus = NULL,  
   DBPARAMIO eParamIO = DBPARAMIO_INPUT   
) throw ( );  
```  
  
#### <a name="parameters"></a>매개 변수  
 참조 [DBBINDING](https://msdn.microsoft.com/en-us/library/ms716845.aspx) 에 *OLE DB Programmer's Reference*합니다.  
  
 `nOrdinal`  
 [in] 매개 변수 수입니다.  
  
 `wType`  
 [in] 데이터 형식입니다.  
  
 `nColumnSize`  
 [in] 열 크기 (바이트)에서입니다.  
  
 `pData`  
 [in] 버퍼에 저장 된 열 데이터에 대 한 포인터입니다.  
  
 `pLength`  
 [in] 필요한 경우 필드 길이에 대 한 포인터입니다.  
  
 `pStatus`  
 [in] 필요한 경우 열 상태에 바인딩할 수를 변수에 대 한 포인터입니다.  
  
 *eParamIO*  
 [in] 바인딩에 연결 된 매개 변수는 입력, 입/출력 또는 출력 매개 변수 인지 여부를 지정 합니다.  
  
## <a name="remarks"></a>설명  
 이 함수를 사용 하려면 호출 먼저 해야 [CreateParameterAccessor](../../data/oledb/cmanualaccessor-createparameteraccessor.md)합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [CManualAccessor 클래스](../../data/oledb/cmanualaccessor-class.md)   
 [Cmanualaccessor:: Addbindentry](../../data/oledb/cmanualaccessor-addbindentry.md)   
 [DBViewer 샘플](../../visual-cpp-samples.md)