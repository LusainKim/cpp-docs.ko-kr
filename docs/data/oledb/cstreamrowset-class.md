---
title: "CStreamRowset 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::CStreamRowset<TAccessor>
- ATL::CStreamRowset
- CStreamRowset
- ATL.CStreamRowset<TAccessor>
- ATL.CStreamRowset
dev_langs: C++
helpviewer_keywords: CStreamRowset class
ms.assetid: a106e953-a38a-464e-8ea5-28963d9e4811
caps.latest.revision: "11"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 32c4aa20f805ee141918e7c073709ec33b4d29ca
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cstreamrowset-class"></a>CStreamRowset 클래스
사용 되는 `CCommand` 또는 `CTable` 선언 합니다.  
  
## <a name="syntax"></a>구문  
  
```  
template <class TAccessor = CAccessorBase>  
class CStreamRowset  
```  
  
#### <a name="parameters"></a>매개 변수  
 `TAccessor`  
 접근자 클래스입니다.  
  
## <a name="members"></a>멤버  
  
### <a name="methods"></a>메서드  
  
|||  
|-|-|  
|[CStreamRowset](../../data/oledb/cstreamrowset-cstreamrowset.md)|생성자입니다. 인스턴스화하고 초기화는 `CStreamRowset` 개체입니다.|  
|[닫기](../../data/oledb/cstreamrowset-close.md)|릴리스는 [ISequentialStream](https://msdn.microsoft.com/en-us/library/ms718035.aspx) 클래스에 인터페이스 포인터입니다.|  
  
## <a name="remarks"></a>설명  
 사용 하 여 `CStreamRowset` 에 프로그램 `CCommand` 또는 `CTable` 선언 예제:  
  
 [!code-cpp[NVC_OLEDB_Consumer#11](../../data/oledb/codesnippet/cpp/cstreamrowset-class_1.cpp)]  
  
 또는  
  
 [!code-cpp[NVC_OLEDB_Consumer#12](../../data/oledb/codesnippet/cpp/cstreamrowset-class_2.cpp)]  
  
 `ICommand::Execute`반환 된 `ISequentialStream` 에 저장 된 포인터 `m_spStream`합니다. 사용 하 여는 **읽기** 메서드를 XML 형식 (유니코드 문자열) 데이터를 검색 합니다. 예:  
  
 [!code-cpp[NVC_OLEDB_Consumer#13](../../data/oledb/codesnippet/cpp/cstreamrowset-class_3.cpp)]  
  
 SQL Server 2000 XML 서식에서 수행 하 고 모든 열과 하나의 XML 문자열로 행 집합의 모든 행이 반환 됩니다.  
  
> [!NOTE]
>  이 기능은 SQL Server 2000과만 작동 합니다.  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [OLE DB 소비자 템플릿](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [OLE DB 소비자 템플릿 참조](../../data/oledb/ole-db-consumer-templates-reference.md)