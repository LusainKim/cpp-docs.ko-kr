---
title: "2.9 지시문 중첩 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
ms.assetid: 6565a43c-fd2d-4366-8322-8d75e1b06600
caps.latest.revision: "4"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: bd3c4f790681b1b044f435c03d185585b565eb62
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="29-directive-nesting"></a>2.9 지시문 중첩
지시문의 동적 중첩 다음 규칙을 따라야 합니다.  
  
-   A **병렬** 안에 다른 동적으로 지시문 **병렬** 논리적으로 설정 하는 새 팀으로 구성 된 현재 스레드의 병렬 처리에 중첩 아니면를 사용할 수 있습니다.  
  
-   **에 대 한**, **섹션**, 및 **단일** 동일에 바인딩하는 지시문 **병렬** 서로 중첩 될 수 없습니다.  
  
-   **중요 한** 지시문 동일한 이름 가진 서로 중첩 될 수 없습니다. 이 제한 사항이 교착 상태를 방지 하는 데 충분 하지 않은 note 합니다.  
  
-   **에 대 한**, **섹션**, 및 **단일** 지시문의 동적 범위에 허용 되지 않는 **중요**, **정렬**, 및 **마스터** 지시문은 동일 하 게 바인딩할 경우 영역 **병렬** 지역으로 합니다.  
  
-   **장벽** 지시문의 동적 범위에 허용 되지 않는 **에 대 한**, **정렬**, **섹션**, **단일**, **마스터**, 및 **중요** 지시문은 동일 하 게 바인딩할 경우 영역 **병렬** 지역으로 합니다.  
  
-   **마스터** 지시문의 동적 범위에 허용 되지 않는 **에 대 한**, **섹션**, 및 **단일** 지시문 경우는 **마스터** 지시문 동일한 바인딩할 **병렬** 작업 공유 지시문으로 합니다.  
  
-   **정렬** 지시문의 동적 범위에 허용 되지 않는 **중요 한** 지시문은 동일 하 게 바인딩할 경우 영역 **병렬** 지역으로 합니다.  
  
-   병렬 영역 내부에서 동적으로 실행 하는 경우 허용 되는 지시문은 병렬 영역 외부에서 실행 하는 경우에 허용 됩니다. 를 실행 하면 동적으로 사용자 지정 병렬 영역 밖에 지시문 마스터 스레드에 이루어진 팀에서 실행 됩니다.