---
title: "공급자에서 열을 동적으로 바인딩 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- columns [C++], dynamic column binding
- dynamic column binding
- providers [C++], dynamic column binding
ms.assetid: 45e811e3-f5a7-4627-98cc-bf817c4e556e
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: f95dde27d6958bd9f1ad40bc411c7c434634879b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="dynamically-binding-columns-in-your-provider"></a>공급자에서 열을 동적으로 바인딩
동적 열 바인딩 게이트웨이가 필요한 지 확인 합니다. 때문에 필요할 수 있습니다.  
  
-   행 집합 열 컴파일 타임에 정의 되지 않습니다.  
  
-   열을 추가 하는 책갈피와 같은 요소를 지원 합니다.  
  
### <a name="to-implement-dynamic-column-binding"></a>동적 열 바인딩 구현 하려면  
  
1.  제거 **PROVIDER_COLUMN_MAP**사용자 코드에서 s입니다.  
  
2.  사용자 레코드 (구조)에 다음 선언을 추가 합니다.  
  
    ```  
    static ATLCOLUMNINFO* GetColumnInfo(void* pThis, ULONG* pcCols);  
    ```  
  
3.  구현 된 `GetColumnInfo` 함수입니다. 이 함수를 통해 정보가 저장 되는 방법을 레이아웃 합니다. 속성 또는이 함수에 대 한 기타 정보를 가져와야 할 수 있습니다. 에 매크로 만들 수도 있습니다는 [COLUMN_ENTRY](../../data/oledb/column-entry.md) 매크로 고유한 정보를 추가 합니다.  
  
     다음 예제에서는 한 `GetColumnInfo` 함수입니다.  
  
    ```  
    // Check the property flag for bookmarks, if it is set, set the zero  
    // ordinal entry in the column map with the bookmark information.  
    CAgentRowset* pRowset = (CAgentRowset*) pThis;  
    CComQIPtr<IRowsetInfo, &IID_IRowsetInfo> spRowsetProps = pRowset;  
  
    CDBPropIDSet set(DBPROPSET_ROWSET);  
    set.AddPropertyID(DBPROP_BOOKMARKS);  
    DBPROPSET* pPropSet = NULL;  
    ULONG ulPropSet = 0;  
    HRESULT hr;  
  
    if (spRowsetProps)  
       hr = spRowsetProps->GetProperties(1, &set, &ulPropSet, &pPropSet);  
  
    if (pPropSet)  
    {  
       CComVariant var = pPropSet->rgProperties[0].vValue;  
       CoTaskMemFree(pPropSet->rgProperties);  
       CoTaskMemFree(pPropSet);  
  
       if (SUCCEEDED(hr) && (var.boolVal == VARIANT_TRUE))  
       {  
          ADD_COLUMN_ENTRY_EX(ulCols, OLESTR("Bookmark"), 0, sizeof(DWORD), DBTYPE_BYTES,   
             0, 0, GUID_NULL, CAgentMan, dwBookmark, DBCOLUMNFLAGS_ISBOOKMARK)  
          ulCols++;  
       }  
    }  
  
    // Next, set up the other columns.  
    ADD_COLUMN_ENTRY(ulCols, OLESTR("Command"), 1, 256, DBTYPE_STR, 0xFF, 0xFF,   
       GUID_NULL, CAgentMan, szCommand)  
    ulCols++;  
    ADD_COLUMN_ENTRY(ulCols, OLESTR("Text"), 2, 256, DBTYPE_STR, 0xFF, 0xFF,   
       GUID_NULL, CAgentMan, szText)  
    ulCols++;  
  
    ADD_COLUMN_ENTRY(ulCols, OLESTR("Command2"), 3, 256, DBTYPE_STR, 0xFF, 0xFF,   
       GUID_NULL, CAgentMan, szCommand2)  
    ulCols++;  
    ADD_COLUMN_ENTRY(ulCols, OLESTR("Text2"), 4, 256, DBTYPE_STR, 0xFF, 0xFF,   
       GUID_NULL, CAgentMan, szText2)  
    ulCols++;  
  
    if (pcCols != NULL)  
       *pcCols = ulCols;  
  
    return _rgColumns;  
    }  
    ```  
  
## <a name="see-also"></a>참고 항목  
 [OLE DB 공급자 템플릿을 사용하여 작업](../../data/oledb/working-with-ole-db-provider-templates.md)