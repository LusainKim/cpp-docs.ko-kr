---
title: CColumns, CColumnsInfo | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- m_szDomainSchema
- CColumns
- m_guidType
- COLLATION_CATALOG
- m_szTableSchema
- COLUMN_DEFAULT
- IS_NULLABLE
- m_nColumnPropID
- ORDINAL_POSITION
- m_szColumnDefault
- m_szCollationCatalog
- m_nDateTimePrecision
- m_szDomainCatalog
- m_nOrdinalPosition
- m_szDomainName
- COLUMN_GUID
- CHARACTER_SET_NAME
- m_nColumnFlags
- DOMAIN_NAME
- m_szCollationName
- m_szColumnName
- CHARACTER_SET_SCHEMA
- COLUMN_FLAGS
- m_szCharSetName
- NUMERIC_PRECISION
- DOMAIN_SCHEMA
- DOMAIN_CATALOG
- m_nDataType
- m_szTableCatalog
- CHARACTER_SET_CATALOG
- m_szCharSetSchema
- CHARACTER_OCTET_LENGTH
- NUMERIC_SCALE
- m_nNumericScale
- COLUMN_PROPID
- m_guidColumn
- m_szCharSetCatalog
- m_nMaxLength
- CHARACTER_MAXIMUM_LENGTH
- COLLATION_NAME
- COLLATION_SCHEMA
- m_bColumnHasDefault
- m_szTableName
- m_nNumericPrecision
- DATA_TYPE
- m_nOctetLength
- CColumnsInfo
- m_szCollationSchema
- m_bIsNullable
- COLUMN_HASDEFAULT
- DATETIME_PRECISION
dev_langs: C++
helpviewer_keywords:
- NUMERIC_PRECISION
- COLUMN_PROPID
- DATA_TYPE
- ORDINAL_POSITION
- m_nMaxLength
- DESCRIPTION class data member
- m_nDateTimePrecision
- m_bColumnHasDefault
- m_szCollationName
- m_guidType
- CColumnsInfo parameter class
- COLLATION_SCHEMA
- m_szDomainSchema
- COLUMN_HASDEFAULT
- CHARACTER_OCTET_LENGTH
- m_szDomainName
- DOMAIN_NAME
- DOMAIN_SCHEMA
- m_szTableSchema
- TABLE_CATALOG
- m_szCharSetCatalog
- m_szColumnDefault
- TABLE_NAME
- COLUMN_FLAGS
- m_szDomainCatalog
- m_nOrdinalPosition
- m_nColumnPropID
- NUMERIC_SCALE
- COLLATION_CATALOG
- DATETIME_PRECISION
- TABLE_SCHEMA
- m_nNumericPrecision
- m_szColumnName
- COLUMN_NAME
- m_nOctetLength
- IS_NULLABLE
- m_bIsNullable
- m_szTableCatalog
- COLLATION_NAME
- m_szDescription
- m_szTableName
- CColumns typedef class
- m_nDataType
- m_nNumericScale
- m_szCollationCatalog
- m_szCollationSchema
- CHARACTER_SET_NAME
- m_nColumnFlags
- COLUMN_GUID
- CHARACTER_MAXIMUM_LENGTH
- m_szCharSetName
- m_guidColumn
- CHARACTER_SET_SCHEMA
- CHARACTER_SET_CATALOG
- DOMAIN_CATALOG
- m_szCharSetSchema
- COLUMN_DEFAULT
ms.assetid: 7a4ca8e8-e041-4def-8c1a-00c211f7da0b
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 90ec0d78dc9a95f80dec04141184f5376d0e6556
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ccolumns-ccolumnsinfo"></a>CColumns, CColumnsInfo
Typedef 클래스 호출 **CColumns** 해당 매개 변수 클래스를 구현 하려면 **CColumnsInfo**합니다.  
  
## <a name="remarks"></a>설명  
 참조 [스키마 행 집합 클래스 및 Typedef 클래스](../../data/oledb/schema-rowset-classes-and-typedef-classes.md) typedef 클래스 사용에 대 한 자세한 내용은 합니다.  
  
 이 클래스는 지정된 된 사용자에 액세스할 수 있는 카탈로그에 정의 된 테이블의 열을 식별 합니다.  
  
 다음 표에는 클래스 데이터 멤버 및 해당 OLE DB 열이 나열됩니다. 참조 [COLUMNS 행 집합](https://msdn.microsoft.com/en-us/library/ms723052.aspx) 에 *OLE DB Programmer's Reference* 스키마 및 열에 대 한 자세한 내용은 합니다.  
  
|데이터 멤버|OLE DB 열|  
|------------------|--------------------|  
|m_szTableCatalog|TABLE_CATALOG|  
|m_szTableSchema|TABLE_SCHEMA|  
|m_szTableName|TABLE_NAME|  
|m_szColumnName|COLUMN_NAME|  
|m_guidColumn|COLUMN_GUID|  
|m_nColumnPropID|COLUMN_PROPID|  
|m_nOrdinalPosition|ORDINAL_POSITION|  
|m_bColumnHasDefault|COLUMN_HASDEFAULT|  
|m_szColumnDefault|COLUMN_DEFAULT|  
|m_nColumnFlags|COLUMN_FLAGS|  
|m_bIsNullable|IS_NULLABLE|  
|m_nDataType|DATA_TYPE|  
|m_guidType|TYPE_GUID|  
|m_nMaxLength|CHARACTER_MAXIMUM_LENGTH|  
|m_nOctetLength|CHARACTER_OCTET_LENGTH|  
|m_nNumericPrecision|NUMERIC_PRECISION|  
|m_nNumericScale|NUMERIC_SCALE|  
|m_nDateTimePrecision|DATETIME_PRECISION|  
|m_szCharSetCatalog|CHARACTER_SET_CATALOG|  
|m_szCharSetSchema|CHARACTER_SET_SCHEMA|  
|m_szCharSetName|CHARACTER_SET_NAME|  
|m_szCollationCatalog|COLLATION_CATALOG|  
|m_szCollationSchema|COLLATION_SCHEMA|  
|m_szCollationName|COLLATION_NAME|  
|m_szDomainCatalog|DOMAIN_CATALOG|  
|m_szDomainSchema|DOMAIN_SCHEMA|  
|m_szDomainName|DOMAIN_NAME|  
|m_szDescription|설명|  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbsch.h  
  
## <a name="see-also"></a>참고 항목  
 [CatDB](../../visual-cpp-samples.md)   
 [CRestrictions 클래스](../../data/oledb/crestrictions-class.md)