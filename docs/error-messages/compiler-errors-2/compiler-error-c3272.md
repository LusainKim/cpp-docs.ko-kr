---
title: "컴파일러 오류 C3272 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: C3272
dev_langs: C++
helpviewer_keywords: C3272
ms.assetid: 7cdf254d-f207-4116-a1bf-7386f3b82a6f
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 70c08b38abf3df5820ab2b37064d1f47d358e44e
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compiler-error-c3272"></a>컴파일러 오류 C3272
'symbol': 기호는 StructLayout(LayoutKind::Explicit)으로 정의된 typename 형식의 멤버이므로 FieldOffset이 필요합니다.  
  
때 `StructLayout(LayoutKind::Explicit)` 필드 표시 되어야 합니다가 적용 된 경우 `FieldOffset`합니다.  
  
다음 샘플에서는 C3272를 생성합니다.  
  
```  
// C3272_2.cpp  
// compile with: /clr /c  
using namespace System;  
using namespace System::Runtime::InteropServices;  
  
[StructLayout(LayoutKind::Explicit)]  
ref struct X  
{  
   int data_;   // C3272  
   // try the following line instead  
   // [FieldOffset(0)] int data_;  
};  
```  
