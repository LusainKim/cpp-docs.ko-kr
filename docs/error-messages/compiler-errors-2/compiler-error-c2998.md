---
title: "컴파일러 오류 C2998 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C2998
dev_langs: C++
helpviewer_keywords: C2998
ms.assetid: 8193d491-b5d9-4477-acb1-cf166889c070
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 04dbaa32e5fdde406bf5dc4a97febbc9a95d1c56
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c2998"></a>컴파일러 오류 C2998
'identifier': 템플릿 정의일 수 없습니다.  
  
 컴파일러에서 템플릿 정의에 사용되는 구문을 처리할 수 없습니다.  
  
 다음 샘플에서는 C2998을 생성합니다.  
  
```  
// C2998.cpp  
// compile with: /c  
template <class T> int x = 1018; // C2998  
```