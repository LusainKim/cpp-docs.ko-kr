---
title: 'Cxmlaccessor:: Getxmlrowdata | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::CXMLAccessor::GetXMLRowData
- ATL.CXMLAccessor.GetXMLRowData
- CXMLAccessor::GetXMLRowData
- CXMLAccessor.GetXMLRowData
- GetXMLRowData
dev_langs: C++
helpviewer_keywords: GetXMLRowData method
ms.assetid: 156b66e3-42fd-491c-8943-38cf5e36f687
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 1cfd67065b267f01704bb0658b89d9bab2186100
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cxmlaccessorgetxmlrowdata"></a>CXMLAccessor::GetXMLRowData
행으로 테이블의 전체 내용을 XML 형식의 문자열 데이터를 검색합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
      HRESULT GetXMLRowData(   
   CSimpleStringW& strOutput,   
   bool bAppend = false    
) throw( );  
```  
  
#### <a name="parameters"></a>매개 변수  
 `strOutput`  
 [out] 테이블 데이터를 검색할 수를 포함 하는 버퍼에 대 한 참조입니다. XML 태그 이름이 데이터 저장소의 열 이름과 일치 하는 문자열 데이터는 데이터 형식.  
  
 *bAppend*  
 [in] 문자열을 출력 데이터의 끝에 추가할 것인지를 지정 하는 부울 값입니다.  
  
## <a name="return-value"></a>반환 값  
 표준 중 하나 `HRESULT` 값입니다.  
  
## <a name="remarks"></a>설명  
 다음 XML에서 행 데이터 형식 지정 방법을 보여 줍니다. `DATA`아래 행 데이터를 표시 합니다. 사용 하 여 원하는 행으로 이동 하는 메서드를 이동 합니다.  
  
 `<row>`  
  
 `<column name>DATA</column name>`  
  
 `</row>`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [CXMLAccessor 클래스](../../data/oledb/cxmlaccessor-class.md)