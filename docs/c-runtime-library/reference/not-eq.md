---
title: not_eq | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
apitype: DLLExport
f1_keywords:
- not_eq
- std::not_eq
- std.not_eq
dev_langs: C++
helpviewer_keywords: not_eq function
ms.assetid: d87ad299-8b50-4393-a57f-06f70e1f23fb
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: b607037fd5281bed80288a5cb45da36684b304fc
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="noteq"></a>not_eq
!= 연산자에 대한 대안입니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
#define not_eq !=  
  
```  
  
## <a name="remarks"></a>설명  
 매크로가 != 연산자를 생성합니다.  
  
## <a name="example"></a>예  
  
```  
// iso646_not_eq.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iso646.h>  
  
int main( )  
{  
   using namespace std;  
   int a = 0, b = 1;  
  
   if (a != b)  
      cout << "a is not equal to b" << endl;  
  
   if (a not_eq b)  
      cout << "a is not equal to b" << endl;  
}  
```  
  
```Output  
a is not equal to b  
a is not equal to b  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<iso646.h>