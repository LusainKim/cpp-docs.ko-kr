---
title: "&lt;istream&gt; | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- istream/std::<istream>
- <istream>
- std::<istream>
dev_langs: C++
helpviewer_keywords: istream header
ms.assetid: efcf24e4-05d1-4719-ab0b-9e7ebe845d89
caps.latest.revision: "20"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 570a23dff65c6c4838d85083b25507bbf0f68e44
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ltistreamgt"></a>&lt;istream&gt;
iostreams에 대한 추출을 중재하는 템플릿 클래스 basic_istream 및 삽입과 추출을 모두 중재하는 템플릿 클래스 basic_iostream을 정의합니다. 헤더에서 관련 조작자도 정의합니다. 이 헤더 파일은 일반적으로 다른 iostreams 헤더에 의해 포함되며, 직접 포함해야 하는 경우는 거의 없습니다.  
  
## <a name="syntax"></a>구문  
  
```  
#include <istream>  
  
```  
  
### <a name="typedefs"></a>형식 정의  
  
|||  
|-|-|  
|[iostream](../standard-library/istream-typedefs.md#iostream)|`char`에서 특수화된 `basic_iostream` 형식입니다.|  
|[istream](../standard-library/istream-typedefs.md#istream)|`char`에서 특수화된 `basic_istream` 형식입니다.|  
|[wiostream](../standard-library/istream-typedefs.md#wiostream)|**wchar**에서 특수화된 `basic_iostream` 형식입니다.|  
|[wistream](../standard-library/istream-typedefs.md#wistream)|**wchar**에서 특수화된 `basic_istream` 형식입니다.|  
  
### <a name="manipulators"></a>조작자  
  
|||  
|-|-|  
|[ws](../standard-library/istream-functions.md#ws)|스트림의 공백을 건너뜁니다.|  
|[swap](../standard-library/istream-functions.md#istream_swap)|두 스트림 개체를 교환합니다.|  
  
### <a name="operators"></a>연산자  
  
|||  
|-|-|  
|[operator>>](../standard-library/istream-operators.md#op_gt_gt)|스트림에서 문자 및 문자열을 추출합니다.|  
  
### <a name="classes"></a>클래스  
  
|||  
|-|-|  
|[basic_iostream](../standard-library/basic-iostream-class.md)|입력과 출력을 둘 다 수행할 수 있는 스트림 클래스입니다.|  
|[basic_istream](../standard-library/basic-istream-class.md)|이 템플릿 클래스는 문자 특성이 **Tr** 클래스([traits_type](../standard-library/basic-ios-class.md#traits_type)이라고도 함)에 의해 결정되는 **Elem**([char_type](../standard-library/basic-ios-class.md#char_type)이라고도 함) 형식의 요소가 있는 스트림 버퍼에서 요소 및 인코드된 개체의 추출을 제어하는 개체를 설명합니다.|  
  
## <a name="see-also"></a>참고 항목  
 [C++ 표준 라이브러리의 스레드 보안](../standard-library/thread-safety-in-the-cpp-standard-library.md)   
 [iostream 프로그래밍](../standard-library/iostream-programming.md)   
 [iostreams 규칙](../standard-library/iostreams-conventions.md)



