---
title: "문자 할당 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- characters [C++], assignments
- MBCS [C++], character assignments
ms.assetid: dcc329cd-92df-4e20-817d-364be62ff28f
caps.latest.revision: "9"
author: ghogen
ms.author: ghogen
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 266d3284716647fa073f76ef6ef871a3abd179bb
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="character-assignment"></a>문자 할당
다음 예제는 `while` 루프 다른 문자열에 'X'를 제외한 모든 문자를 복사 하는 문자열을 검색 합니다.  
  
```  
while( *sz2 )  
{  
    if( *sz2 != 'X' )  
        *sz1++ = *sz2++;  
    else  
        sz2++;  
}  
```  
  
 코드에 바이트를 복사 `sz2` 가 가리키는 위치에 `sz1`를 증가 시킵니다 `sz1` 다음 바이트를 수신 하도록 합니다. 그러나의 다음 문자가 `sz2` 더블 바이트 문자에 대 한 할당 `sz1` 만 첫 번째 바이트를 복사 합니다. 다음 코드에서는 문자를 안전 하 게 복사 하는 이식 가능한 함수 및 증가 시키는 다른 `sz1` 및 `sz2` 올바르게:  
  
```  
while( *sz2 )  
{  
    if( *sz2 != 'X' )  
    {  
        _mbscpy_s( sz1, 1, sz2 );  
        sz1 = _mbsinc( sz1 );  
        sz2 = _mbsinc( sz2 );  
    }  
    else  
        sz2 = _mbsinc( sz2 );  
}  
```  
  
## <a name="see-also"></a>참고 항목  
 [MBCS 프로그래밍 팁](../text/mbcs-programming-tips.md)   
 [문자 비교](../text/character-comparison.md)