---
title: "&lt;istream&gt; 함수 | Microsoft 문서"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- istream/std::swap
- istream/std::ws
ms.assetid: 0301ea0d-4ded-4841-83dd-4253b55b3188
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 30bf6fb6bba318d2ab4d150fb242a28e4148083d
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="ltistreamgt-functions"></a>&lt;istream&gt; 함수
|||  
|-|-|  
|[swap](#istream_swap)|[ws](#ws)|  
  
##  <a name="istream_swap"></a>  swap  
 두 stream 개체의 요소를 교환합니다.  
  
```  
template <class Elem, class Tr>  
void swap(
    basic_istream<Elem, Tr>& left,  
    basic_istream<Elem, Tr>& right);

template <class Elem, class Tr>  
void swap(
    basic_iostream<Elem, Tr>& left,  
    basic_iostream<Elem, Tr>& right);
```  
  
### <a name="parameters"></a>매개 변수  
 `left`  
 스트림입니다.  
  
 `right`  
 스트림입니다.  
  
##  <a name="ws"></a>  ws  
 스트림의 공백을 건너뜁니다.  
  
```  
template class<Elem, Tr> basic_istream<Elem, Tr>& ws(basic_istream<Elem, Tr>& _Istr);
```  
  
### <a name="parameters"></a>매개 변수  
 `_Istr`  
 스트림입니다.  
  
### <a name="return-value"></a>반환 값  
 스트림입니다.  
  
### <a name="remarks"></a>설명  
 이 조작자는 모든 `ch` 요소(이 요소의 경우 [use_facet](../standard-library/basic-filebuf-class.md#open)< **ctype**\< **Elem**> >( [getloc](../standard-library/ios-base-class.md#getloc)). **is**( **ctype**\< **Elem**>:: **space**, **ch**)가 true임)를 추출하고 삭제합니다.  
  
 함수는 요소를 추출하는 동안 파일 끝에 도달하면 [setstate](../standard-library/basic-ios-class.md#setstate)( **eofbit**)를 호출합니다. `_Istr`를 반환합니다.  
  
### <a name="example"></a>예  
  `ws` 사용 예제는 [operator>>](../standard-library/istream-operators.md#op_gt_gt)를 참조하세요.  
  
## <a name="see-also"></a>참고 항목  
 [\<istream>](../standard-library/istream.md)

