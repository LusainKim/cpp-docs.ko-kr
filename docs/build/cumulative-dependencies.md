---
title: "누적 종속성 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- dependencies, cumulative
- cumulative dependencies in NMAKE
- dependencies
ms.assetid: fa6dd777-80b8-437d-87a7-aec0ed818a49
caps.latest.revision: "11"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 40811087cedd83bcd34745be7f1d5a404f4bb628
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cumulative-dependencies"></a>누적되는 종속 줄
대상이 반복 되는 경우 종속성 설명 블록에 누적 됩니다.  
  
 예를 들어이 규칙 집합에  
  
```Output  
bounce.exe : jump.obj  
bounce.exe : up.obj  
   echo Building bounce.exe...  
```  
  
 이 평가 됩니다.  
  
```Output  
bounce.exe : jump.obj up.obj  
   echo Building bounce.exe...  
```  
  
 별도 설명 블록에 지정 된 각 있지만 마지막 연결선에 있지 않은 대상 명령 블록을 사용 하지 않는 단일 설명 블록에 여러 개의 종속 줄에서 여러 개의 대상은 평가 됩니다. NMAKE 유추 규칙을 사용 하 여 이러한 대상에 대 한 하려고 시도 합니다.  
  
 예를 들어이 규칙 집합에  
  
```Output  
leap.exe bounce.exe : jump.obj  
bounce.exe climb.exe : up.obj  
   echo Building bounce.exe...  
```  
  
 이 평가 됩니다.  
  
```Output  
  
leap.exe : jump.obj  
# invokes an inference rule  
bounce.exe : jump.obj up.obj  
   echo Building bounce.exe...  
climb.exe : up.obj  
   echo Building bounce.exe...  
```  
  
## <a name="see-also"></a>참고 항목  
 [대상](../build/targets.md)