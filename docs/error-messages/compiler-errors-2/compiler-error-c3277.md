---
title: "컴파일러 오류 C3277 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: C3277
dev_langs: C++
helpviewer_keywords: C3277
ms.assetid: 8ac5f476-e30c-4879-92c6-f03cdbd74045
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 68ff09360a5ea247aae4ca9ad47242b80c194451
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3277"></a>컴파일러 오류 C3277
관리 되지 않는 열거형 'enum' 관리 되는 'type' 내부에 정의할 수 없습니다.  
  
 관리 되는 형식 내 열거형 잘못 정의 되었습니다.  
  
 다음 샘플에서는 C3277 오류가 생성 됩니다.  
  
```  
// C3277a.cpp  
// compile with: /clr  
ref class A  
{  
   enum E {e1,e2};   // C3277  
   // try the following line instead  
   // enum class E {e1,e2};  
};  
  
int main()  
{  
}  
```  
