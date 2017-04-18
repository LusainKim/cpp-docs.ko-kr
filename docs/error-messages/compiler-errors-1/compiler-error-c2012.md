---
title: "컴파일러 오류 C2012 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2012
dev_langs:
- C++
helpviewer_keywords:
- C2012
ms.assetid: 9f0d8162-c0b3-4234-a41f-836fdb75c84e
caps.latest.revision: 7
author: corob-msft
ms.author: corob
manager: ghogen
translation.priority.ht:
- de-de
- es-es
- fr-fr
- it-it
- ja-jp
- ko-kr
- ru-ru
- zh-cn
- zh-tw
translation.priority.mt:
- cs-cz
- pl-pl
- pt-br
- tr-tr
translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: abd50581ebfadb732055d54a5ba6c55e40386aa9
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2012"></a>컴파일러 오류 C2012
'<' 다음에 이름이 없습니다.  
  
 `#include` 지시문에 필요한 파일 이름이 없습니다.  
  
 다음 샘플에서는 C2012를 생성합니다.  
  
```  
// C2012.cpp  
#include <   // C2012 include the filename to resolve  
```  
  
 해결 방법:  
  
```  
// C2012b.cpp  
// compile with: /c  
#include <stdio.h>  
```
