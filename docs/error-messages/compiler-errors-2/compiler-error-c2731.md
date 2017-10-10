---
title: "컴파일러 오류 C2731 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology:
- cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords:
- C2731
dev_langs:
- C++
helpviewer_keywords:
- C2731
ms.assetid: 9b563999-febd-4582-9147-f355083c091e
caps.latest.revision: 8
author: corob-msft
ms.author: corob
manager: ghogen
ms.translationtype: MT
ms.sourcegitcommit: 35b46e23aeb5f4dbfd2a0dd44b906389dd5bfc88
ms.openlocfilehash: 82a110e7d222a2fe183d0323472a0266e9779771
ms.contentlocale: ko-kr
ms.lasthandoff: 10/10/2017

---
# <a name="compiler-error-c2731"></a>컴파일러 오류 C2731
'identifier': 함수를 오버 로드할 수 없습니다  
  
 함수 `main`, `WinMain`, `DllMain`, 및 `LibMain` 오버 로드할 수 없습니다.  
  
 다음 샘플에서는 C2731 오류가 생성 됩니다.  
  
```  
// C2731.cpp  
extern "C" void WinMain(int, char *, char *);  
void WinMain(int, short, char *, char*);   // C2731  
```
