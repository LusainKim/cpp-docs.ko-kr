---
title: 'Crowset:: Movelast | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- ATL::CRowset<TAccessor>::MoveLast
- CRowset<TAccessor>::MoveLast
- ATL.CRowset.MoveLast
- ATL::CRowset::MoveLast
- CRowset<TAccessor>.MoveLast
- MoveLast
- CRowset::MoveLast
- ATL.CRowset<TAccessor>.MoveLast
- CRowset.MoveLast
dev_langs: C++
helpviewer_keywords: MoveLast method
ms.assetid: 81063578-ae9d-467b-8c88-81d8fc66e020
caps.latest.revision: "9"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: d57885232fb10f302aeb36c6c074e7a88f0fb67b
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="crowsetmovelast"></a>CRowset::MoveLast
커서가 마지막 행으로 이동합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
HRESULT MoveLast( ) throw( );  
  
```  
  
## <a name="return-value"></a>반환 값  
 표준 `HRESULT`입니다.  
  
## <a name="remarks"></a>설명  
 호출 [irowset:: Restartposition](https://msdn.microsoft.com/en-us/library/ms712877.aspx) 위치 다음 인출 위치를 마지막으로 변경 하려면 위치를 지정 하 고 마지막 행을 검색 합니다.  
  
 이 방법을 사용 하 여 설정한 하려면 **DBPROP_CANSCROLLBACKWARDS** 를 `VARIANT_TRUE` 호출 하기 전에 **열려** 테이블이 나 행 집합을 포함 하는 명령입니다. (성능 향상을 위해 설정할 수 있습니다 **DBPROP_QUICKRESTART** 를 `VARIANT_TRUE`.)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** atldbcli.h  
  
## <a name="see-also"></a>참고 항목  
 [CRowset 클래스](../../data/oledb/crowset-class.md)   
 [Crowset:: Movenext](../../data/oledb/crowset-movenext.md)   
 [Irowset:: Restartposition](https://msdn.microsoft.com/en-us/library/ms712877.aspx)   
 [CRowset::MovePrev](../../data/oledb/crowset-moveprev.md)