---
title: "공급자 디버깅 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- debugging [C++], providers
- OLE DB providers, debugging
- Visual C++ debugger, debugging providers
- Visual C++ debugger
ms.assetid: 90d4e7db-06ea-4de0-a7f4-4f3751d50d93
caps.latest.revision: "7"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 6cfcb90daaf23a5fd8e248d43b920340e38d8057
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="debugging-your-provider"></a>공급자 디버깅
공급자를 디버깅 하는 방법은 두 가지가 있습니다.  
  
-   공급자, 프로세스에서 생성 되므로 일반적으로 OLE DB 소비자 템플릿 및 단계 공급자를 사용 하 여 일부 소비자 코드를 만들 수 있습니다.  
  
-   Visual c + +와 함께 제공 되는 ITEST 유틸리티를 사용할 수 있습니다.  
  
### <a name="to-use-the-itest-utility"></a>ITEST 유틸리티를 사용 하려면  
  
1.  프로젝트를 엽니다.  
  
2.  에 **프로젝트** 메뉴를 클릭 하 여 **설정을**합니다.  
  
3.  에 **속성 페이지** 대화 상자를 클릭는 **디버그** 탭 합니다.  
  
4.  에 **디버그 세션에 사용할 실행 파일** 상자 ITEST 응용 프로그램을 선택 합니다.  
  
5.  중단점을 설정 하 고 디버깅 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [OLE DB 공급자 템플릿을 사용하여 작업](../../data/oledb/working-with-ole-db-provider-templates.md)