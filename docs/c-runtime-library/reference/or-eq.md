---
title: or_eq | Microsoft Docs
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
- std::or_eq
- or_eq
- std.or_eq
dev_langs: C++
helpviewer_keywords: or_eq function
ms.assetid: 1eb92464-ed58-40d8-a30e-f0a6aa2f4318
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7d6d8b7761cbf7f3802b185a10291c408cc0ff33
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="oreq"></a>or_eq
&#124;= 연산자에 대한 대안입니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
#define or_eq |=  
  
```  
  
## <a name="remarks"></a>설명  
 매크로가 &#124;= 연산자를 생성합니다.  
  
## <a name="example"></a>예  
  
```  
// iso646_oreq.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iso646.h>  
  
int main( )  
{  
   using namespace std;  
   int a = 3, b = 2, result;  
  
   result= a |= b;  
   cout << result << endl;  
  
   result= a or_eq b;  
   cout << result << endl;  
}  
```  
  
```Output  
3  
3  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<iso646.h>