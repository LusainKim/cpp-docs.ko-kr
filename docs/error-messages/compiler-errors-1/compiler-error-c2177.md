---
title: "컴파일러 오류 C2177 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2177
dev_langs:
- C++
helpviewer_keywords:
- C2177
ms.assetid: 2a39a880-cddb-4d3e-a572-645a14c4c478
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: ee58568c2878d9a3a83b95aee2d9cab5f87eac56
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2177"></a>컴파일러 오류 C2177
상수가 너무 큽니다.  
  
 상수 값이 할당된 변수 형식에 대해 너무 큽니다.  
  
 다음 샘플에서는 C2177을 생성합니다.  
  
```  
// C2177.cpp  
int main() {  
   int a=18446744073709551616;   // C2177  
   int b=18446744073709551615;   // OK  
}  
```
