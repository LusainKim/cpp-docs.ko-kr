---
title: COLUMN_ENTRY_PS | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: COLUMN_ENTRY_PS
dev_langs: C++
helpviewer_keywords: COLUMN_ENTRY_PS macro
ms.assetid: 563c12b0-3376-49d5-a14f-aa68d1e63a7a
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 594c9301d914279cafa76aa573b6b1434cf9d88a
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="columnentryps"></a>COLUMN_ENTRY_PS
행 집합의 특정 열에는 행 집합의 바인딩을 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
COLUMN_ENTRY_PS(  
nOrdinal  
,   
nPrecision  
,   
nScale  
,   
data  
 )  
  
```  
  
#### <a name="parameters"></a>매개 변수  
 참조 [DBBINDING](https://msdn.microsoft.com/en-us/library/ms716845.aspx) 에 *OLE DB Programmer's Reference*합니다.  
  
 `nOrdinal`  
 [in] 열 번호입니다.  
  
 `nPrecision`  
 [in] 바인딩하려는 열의 최대 정밀도입니다.  
  
 `nScale`  
 [in] 바인딩할 열의 배율입니다.  
  
 `data`  
 [in] 사용자 레코드에서 해당 데이터 멤버입니다.  
  
## <a name="remarks"></a>설명  
 바인딩할 열의 정밀도 및 배율을 지정할 수 있습니다. 다음과 같은 위치에 사용됩니다.  
  
-   사이 [BEGIN_COLUMN_MAP](../../data/oledb/begin-column-map.md) 및 [END_COLUMN_MAP](../../data/oledb/end-column-map.md) 매크로입니다.  
  
-   사이 [BEGIN_ACCESSOR](../../data/oledb/begin-accessor.md) 및 [END_ACCESSOR](../../data/oledb/end-accessor.md) 매크로입니다.  
  
-   사이 [BEGIN_PARAM_MAP](../../data/oledb/begin-param-map.md) 및 [END_PARAM_MAP](../../data/oledb/end-param-map.md) 매크로입니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [매크로 및 전역 함수에 대 한 OLE DB 소비자 템플릿](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)   
 [BEGIN_ACCESSOR](../../data/oledb/begin-accessor.md)   
 [BEGIN_ACCESSOR_MAP](../../data/oledb/begin-accessor-map.md)   
 [BEGIN_COLUMN_MAP](../../data/oledb/begin-column-map.md)   
 [COLUMN_ENTRY](../../data/oledb/column-entry.md)   
 [COLUMN_ENTRY_EX](../../data/oledb/column-entry-ex.md)   
 [COLUMN_ENTRY_LENGTH](../../data/oledb/column-entry-length.md)   
 [COLUMN_ENTRY_PS_LENGTH](../../data/oledb/column-entry-ps-length.md)   
 [COLUMN_ENTRY_LENGTH_STATUS](../../data/oledb/column-entry-length-status.md)   
 [COLUMN_ENTRY_PS_LENGTH_STATUS](../../data/oledb/column-entry-ps-length-status.md)   
 [COLUMN_ENTRY_STATUS](../../data/oledb/column-entry-status.md)   
 [COLUMN_ENTRY_PS_STATUS](../../data/oledb/column-entry-ps-status.md)   
 [END_ACCESSOR](../../data/oledb/end-accessor.md)   
 [END_ACCESSOR_MAP](../../data/oledb/end-accessor-map.md)   
 [END_COLUMN_MAP](../../data/oledb/end-column-map.md)