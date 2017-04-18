---
title: "컴파일러 오류 C3368 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- devlang-cpp
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- C3368
dev_langs:
- C++
helpviewer_keywords:
- C3368
ms.assetid: 5bfd5be4-dfa9-4b33-9612-010561b40955
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
ms.openlocfilehash: 9ec0cd20ea492ee3e2d3a96042057392d31213ce
ms.lasthandoff: 04/12/2017

---
# <a name="compiler-error-c3368"></a>컴파일러 오류 C3368
'function declaration': IDL에 대한 호출 규칙이 잘못되었습니다.  
  
 만 사용할 수 있습니다는 [__stdcall](../../cpp/stdcall.md) 또는 [__cdecl](../../cpp/cdecl.md) .idl 파일에서 호출 규칙입니다.  
  
 다음 샘플에서는 C3368을 생성합니다.  
  
```  
// C3368.cpp  
// processor: x86  
[idl_module(name="Name", dllname="Some.dll")];  
  
[idl_module(name="Name")]  
int __fastcall f1();   // C3368  
```
