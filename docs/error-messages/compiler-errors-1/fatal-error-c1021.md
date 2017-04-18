---
title: "심각한 오류 C1021 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C1021
dev_langs:
- C++
helpviewer_keywords:
- C1021
ms.assetid: e23171f4-ca6b-40c0-a913-a2edc6fa3766
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
ms.openlocfilehash: b1ea205d21b0d73f269ff475f9224ab2c10ee562
ms.lasthandoff: 04/12/2017

---
# <a name="fatal-error-c1021"></a>심각한 오류 C1021
'string' 전처리기 명령이 잘못되었습니다.  
  
 `string`유효 하지 않거나 [전처리기 지시문](../../preprocessor/preprocessor-directives.md)합니다. 오류를 해결하려면 `string`에 대해 올바른 전처리기 이름을 사용합니다.  
  
 다음 샘플에서는 C1021을 생성합니다.  
  
```  
// C1021.cpp  
#BadPreProcName    // C1021 delete line  
```
