---
title: "설정 및 해제는 공급자에 대 한 서비스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- OLE DB services [OLE DB], enabling and disabling
- service providers [OLE DB]
ms.assetid: 3deac1bb-f660-407a-92ef-95e139e280c0
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: dc6b3d7cc8e80eaa24c2e2dd9b4e23e79dfb09f9
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="enabling-and-disabling-services-for-a-provider"></a>공급자 서비스 사용 및 사용 안 함
개별 OLE DB 서비스 사용 하도록 설정 하거나 단일 공급자에 액세스 하는 모든 응용 프로그램에 대해 기본적으로 사용 하지 않도록 설정 될 수 있습니다. 추가 하 여 이렇게는 **OLEDB_SERVICES** 공급자 아래에 레지스트리 항목으로 CLSID의 `DWORD` 다음 표에 나와 있는 것 처럼 사용 하거나 사용 하려면 서비스를 지정 하는 값입니다.  
  
|기본 서비스를 사용할 수|키워드 값|  
|------------------------------|-------------------|  
|모든 서비스 (기본값)|0xffffffff|  
|풀링 제외 하 고 모두 및 AutoEnlistment|0xfffffffe|  
|클라이언트 커서 제외한 모든 컴퓨터|0xfffffffb|  
|AutoEnlistment, 및 클라이언트 커서 풀링 차트를 제외한 모든|0xfffffff0|  
|서비스|0x00000000|  
|집합체 없음, 모든 서비스 사용 안 함|\<누락 된 키 >|  
  
## <a name="see-also"></a>참고 항목  
 [OLE DB 서비스 사용 및 사용 안 함](../../data/oledb/enabling-and-disabling-ole-db-services.md)