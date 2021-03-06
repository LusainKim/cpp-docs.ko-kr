---
title: '&lt;streambuf&gt; | Microsoft Docs'
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: <streambuf>
dev_langs: C++
helpviewer_keywords: streambuf header
ms.assetid: 4365b25c-5831-488b-b9c2-867bfe961b89
caps.latest.revision: "19"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: fa3e46d166ca1807d18caadcca94ec72020a1249
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ltstreambufgt"></a>&lt;streambuf&gt;
iostreams 클래스 작동의 기본 요소인 템플릿 클래스 [basic_streambuf](../standard-library/basic-streambuf-class.md)를 정의하는 iostreams 표준 헤더 \<streambuf>를 포함합니다. 이 헤더는 일반적으로 다른 iostreams 헤더에 의해 포함되며, 직접 포함해야 하는 경우는 거의 없습니다.  
  
## <a name="syntax"></a>구문  
  
```  
#include <streambuf>  
  
```  
  
### <a name="typedefs"></a>형식 정의  
  
|||  
|-|-|  
|[streambuf](../standard-library/streambuf-typedefs.md#streambuf)|`char`를 템플릿 매개 변수로 사용하는 `basic_streambuf`의 특수화입니다.|  
|[wstreambuf](../standard-library/streambuf-typedefs.md#wstreambuf)|`wchar_t`를 템플릿 매개 변수로 사용하는 `basic_streambuf`의 특수화입니다.|  
  
### <a name="classes"></a>클래스  
  
|||  
|-|-|  
|[basic_streambuf 클래스](http://msdn.microsoft.com/en-us/d9c706ba-ce01-43e0-b0b2-a558fc53ea8d)|템플릿 클래스는 스트림의 특정 표현과 요소 간의 전송을 제어하는 스트림 버퍼 파생을 위한 추상 기본 클래스에 대해 설명합니다.|  
  
## <a name="see-also"></a>참고 항목  
 [헤더 파일 참조](../standard-library/cpp-standard-library-header-files.md)   
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [iostream 프로그래밍](../standard-library/iostream-programming.md)   
 [iostreams 규칙](../standard-library/iostreams-conventions.md)



