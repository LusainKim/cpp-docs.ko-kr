---
title: "컴파일러 오류 C2238 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2238
dev_langs:
- C++
helpviewer_keywords:
- C2238
ms.assetid: 3d53060c-d6b7-4603-b9cf-d7c65eb64cd2
caps.latest.revision: 8
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
ms.openlocfilehash: be7f6b0d7b2d2dbc45363244e6d8b945fab08c9d
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2238"></a>컴파일러 오류 C2238
'token' 앞에 예기치 않은 토큰이 있습니다.  
  
 잘못된 토큰이 있습니다.  
  
 다음 샘플에서는 C2238을 생성합니다.  
  
```  
// C2238.cpp  
// compile with: /c  
class v {  
virtual: int vvv;   // C2238  
};  
```
