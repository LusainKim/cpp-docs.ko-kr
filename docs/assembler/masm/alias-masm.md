---
title: "별칭 (MASM) | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: Alias
dev_langs: C++
helpviewer_keywords: ALIAS directive
ms.assetid: d9725c49-58de-41da-ab01-b06a56cf5cf2
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 59dc4fd5481b22e69153c68e94a81b2887118ebc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="alias-masm"></a>ALIAS (MASM)
**별칭** 지시문 함수에 대해 다른 이름이 만들어집니다.  이 함수에 대 한 이름을 여러 개 만들거나 링커 (LINK.exe) 이전 함수는 새 함수에 매핑할 수 있는 라이브러리를 만들 수 있습니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
ALIAS  <  
alias  
> = <  
actual-name  
>  
  
```  
  
#### <a name="parameters"></a>매개 변수  
 `actual-name`  
 함수 또는 프로시저의 실제 이름입니다.  꺾쇠 괄호는 반드시 있어야 합니다.  
  
 `alias`  
 대체 또는 별칭 이름입니다.  꺾쇠 괄호는 반드시 있어야 합니다.  
  
## <a name="see-also"></a>참고 항목  
 [지시문 참조](../../assembler/masm/directives-reference.md)