---
title: EXTERN (MASM) | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: extern
dev_langs: C++
helpviewer_keywords: EXTERN directive
ms.assetid: 667d703d-3aaf-4139-a586-29bc5dab1aff
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 814922100d34534d51abed4cb682cc4181685066
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="extern-masm"></a>EXTERN (MASM)
하나 이상의 외부 변수, 레이블 또는 이라는 기호 정의 *이름* 형식이 변수인 `type`합니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
   EXTERN [[langtype]] name [[(altid)]] :  
type [[, [[langtype]] name [[(altid)]] :type]]...  
```  
  
## <a name="remarks"></a>설명  
 `type` 수 [ABS](../../assembler/masm/operator-abs.md)를 가져오는 *이름* 상수입니다. 와 동일 [EXTRN](../../assembler/masm/extrn.md)합니다.  
  
## <a name="see-also"></a>참고 항목  
 [지시문 참조](../../assembler/masm/directives-reference.md)