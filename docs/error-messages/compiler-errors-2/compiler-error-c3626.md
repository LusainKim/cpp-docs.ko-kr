---
title: "컴파일러 오류 C3626 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3626
dev_langs: C++
helpviewer_keywords: C3626
ms.assetid: 43926e2b-1ba9-4a43-9343-c58449cbb336
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 5267936ed969d5338ceb0febcf66c0dfc714d81d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3626"></a>컴파일러 오류 C3626
'keyword': '__event' 키워드는 COM 인터페이스, 멤버 함수 및 대리자에 대 한 포인터는 데이터 멤버에만 사용할 수 있습니다  
  
 키워드를 잘못 사용 되었습니다.  
  
 다음 샘플에서는 C3626 오류가 생성 됩니다.  
  
```  
// C3626.cpp  
// compile with: /c  
struct A {  
   __event int i;   // C3626  
// try the following line instead  
// __event int i();  
};  
```