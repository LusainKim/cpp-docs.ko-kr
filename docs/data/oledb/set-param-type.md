---
title: SET_PARAM_TYPE | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: SET_PARAM_TYPE
dev_langs: C++
helpviewer_keywords: SET_PARAM_TYPE macro
ms.assetid: 85979070-2d55-4c67-94b1-9b9058babc59
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 024cf67033cdc35917f37c2e6183e60042c40d45
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="setparamtype"></a>SET_PARAM_TYPE
`COLUMN_ENTRY` 매크로 입력, 출력 또는 입력/출력 다음에 오는 `SET_PARAM_TYPE` 매크로를 지정합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
SET_PARAM_TYPE(  
type  
 )  
  
```  
  
#### <a name="parameters"></a>매개 변수  
 `type`  
 [in] 매개 변수에 대해 설정할 형식입니다.  
  
## <a name="remarks"></a>설명  
 공급자는 기본 데이터 소스에서 지원되는 매개 변수 입력/출력 형식만 지원합니다. 형식은 하나 이상의 **DBPARAMIO** 값 조합입니다( [OLE DB 프로그래머 참조](https://msdn.microsoft.com/en-us/library/ms716845.aspx) 에서 *DBBINDING 구조체*참조).  
  
-   **DBPARAMIO_NOTPARAM** 이 접근자에는 매개 변수가 없습니다. 일반적으로 사용자에게 매개 변수가 무시됨을 알리기 위해 행 접근자에서 **eParamIO** 를 이 값으로 설정합니다.  
  
-   **DBPARAMIO_INPUT** 입력 매개 변수입니다.  
  
-   **DBPARAMIO_OUTPUT** 출력 매개 변수입니다.  
  
-   **DBPARAMIO_INPUT &#124; DBPARAMIO_OUTPUT** 매개 변수는 입력 및 출력 매개 변수입니다.  
  
## <a name="example"></a>예  
```cpp  
class CArtistsProperty
{
public:
   short m_nReturn;
   short m_nAge;
   TCHAR m_szFirstName[21];
   TCHAR m_szLastName[31];

BEGIN_PARAM_MAP(CArtistsProperty)
   SET_PARAM_TYPE(DBPARAMIO_OUTPUT)
   COLUMN_ENTRY(1, m_nReturn)
   SET_PARAM_TYPE(DBPARAMIO_INPUT)
   COLUMN_ENTRY(2, m_nAge)
END_PARAM_MAP()

BEGIN_COLUMN_MAP(CArtistsProperty)
   COLUMN_ENTRY(1, m_szFirstName)
   COLUMN_ENTRY(2, m_szLastName)
END_COLUMN_MAP()

   HRESULT OpenDataSource()
   {
      CDataSource _db;
      _db.Open();
      return m_session.Open(_db);
   }

   void CloseDataSource()
   {
      m_session.Close();
   }

   CSession m_session;

   DEFINE_COMMAND_EX(CArtistsProperty, L" \
      { ? = SELECT Age FROM Artists WHERE Age < ? }")
};
``` 
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [OLE DB 소비자 템플릿에 대한 매크로 및 전역 함수](../../data/oledb/macros-and-global-functions-for-ole-db-consumer-templates.md)