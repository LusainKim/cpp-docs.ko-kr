---
title: "컴파일러 오류 C3196 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3196
dev_langs: C++
helpviewer_keywords: C3196
ms.assetid: d9c38a13-191d-472d-aa2b-f61a6459d16c
caps.latest.revision: "6"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 16f03511d1f0fced049c6f9b6cdb63e7d06da835
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3196"></a>컴파일러 오류 C3196
'keyword': 두 번 이상 사용  
  
 키워드를 두 번 이상 사용 했습니다.  
  
 다음 샘플에서는 C3196 오류가 생성 됩니다.  
  
```  
// C3196.cpp  
// compile with: /clr  
ref struct R abstract abstract {};   // C3196  
ref struct S abstract {};   // OK  
```