---
title: "compl | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
apiname: compl
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
- std::compl
- std.compl
- compl
dev_langs: C++
helpviewer_keywords: compl function
ms.assetid: e03f6fb5-cb8b-4afa-99c0-905f4105fb34
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 15ca138d271c1cf9e6a86cef8330b327c011b9b1
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="compl"></a>compl
~ 연산자에 대한 대안입니다.  
  
## <a name="syntax"></a>구문  
  
```  
  
#define compl ~  
  
```  
  
## <a name="remarks"></a>설명  
 매크로가 ~ 연산자를 생성합니다.  
  
## <a name="example"></a>예  
  
```  
// iso646_compl.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <iso646.h>  
  
int main( )  
{  
   using namespace std;  
   int a = 1, result;  
  
   result = ~a;  
   cout << result << endl;  
  
   result= compl(a);  
   cout << result << endl;  
}  
```  
  
```Output  
-2  
-2  
```  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** \<iso646.h>