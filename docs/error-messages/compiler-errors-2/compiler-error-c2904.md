---
title: "컴파일러 오류 C2904 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C2904
dev_langs:
- C++
helpviewer_keywords:
- C2904
ms.assetid: d5802f2e-d3fc-473d-aa04-36957b4eaca5
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
ms.translationtype: Machine Translation
ms.sourcegitcommit: 0d9cbb01d1ad0f2ea65d59334cb88140ef18fce0
ms.openlocfilehash: a16467737d4524ee751b6c75f4f274e46dfe964c
ms.contentlocale: ko-kr
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c2904"></a>컴파일러 오류 C2904
'identifier': 이름이 현재 범위의 템플릿으로 이미 사용되었습니다.  
  
 코드 이름이 중복되지 않았는지 확인합니다.  
  
 다음 샘플에서는 C2904를 생성합니다.  
  
```  
// C2904.cpp  
// compile with: /c  
void X();  // X is declared as a function  
template<class T> class X{};  // C2904  
```
