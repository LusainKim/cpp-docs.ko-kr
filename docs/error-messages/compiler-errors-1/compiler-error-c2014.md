---
title: "컴파일러 오류 C2014 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C2014
dev_langs: C++
helpviewer_keywords: C2014
ms.assetid: 231d8e9c-48c0-4027-99a3-245d186275ec
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: b5f718aee1cb7ede548719a8275ea6788b70d1c2
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2014"></a>컴파일러 오류 C2014
전처리기 명령은 공백 아닌 문자로 시작 해야 합니다.  
  
 `#` 기호는 전처리기 지시문의 공백 없는 줄에 첫 번째 문자 여야 합니다.  
  
 다음 샘플에서는 C2014 오류가 생성 됩니다.  
  
```  
// C2014.cpp  
int k; #include <stdio.h>   // C2014  
```  
  
 해결 방법:  
  
```  
// C2014b.cpp  
// compile with: /c  
int k;   
#include <stdio.h>  
```