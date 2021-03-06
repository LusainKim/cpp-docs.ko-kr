---
title: _BitScanReverse, _BitScanReverse64 | Microsoft Docs
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords:
- _BitScanReverse64
- _BitScanReverse_cpp
- _BitScanReverse
- _BitScanReverse64_cpp
dev_langs: C++
helpviewer_keywords:
- bsr instruction
- _BitScanReverse intrinsic
- BitScanReverse intrinsic
ms.assetid: 2520a207-af8b-4aad-9ae7-831abeadf376
caps.latest.revision: "12"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 038c0e30078287f968cd744a9bfe53f65a70bb22
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="bitscanreverse-bitscanreverse64"></a>_BitScanReverse, _BitScanReverse64
**Microsoft 전용**  
  
 MSB(최상위 비트)에서 LSB(최하위 비트)로의 마스크 데이터에서 설정 비트(1)를 검색합니다.  
  
## <a name="syntax"></a>구문  
  
```  
unsigned char _BitScanReverse(  
   unsigned long * Index,  
   unsigned long Mask  
);  
unsigned char _BitScanReverse64(  
   unsigned long * Index,  
   unsigned __int64 Mask  
);  
```  
  
#### <a name="parameters"></a>매개 변수  
 [out] `Index`  
 발견된 첫 번째 설정 비트(1)의 비트 위치를 사용하여 로드됩니다.  
  
 [in] `Mask`  
 검색할 32비트 또는 64비트 값입니다.  
  
## <a name="return-value"></a>반환 값  
 `Index`가 설정된 경우에는 0이 아니고 설정 비트가 발견되지 않은 경우에는 0입니다.  
  
## <a name="requirements"></a>요구 사항  
  
|내장 함수|아키텍처|Header|  
|---------------|------------------|------------|  
|`_BitScanReverse`|x86, ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|\<. h >|  
|`_BitScanReverse64`|ARM, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]||  
  
## <a name="example"></a>예  
  
```  
// BitScanReverse.cpp  
// compile with: /EHsc  
#include <iostream>  
#include <intrin.h>  
using namespace std;  
  
#pragma intrinsic(_BitScanReverse)  
  
int main()  
{  
   unsigned long mask = 0x1000;  
   unsigned long index;  
   unsigned char isNonzero;  
  
   cout << "Enter a positive integer as the mask: " << flush;  
   cin >> mask;  
   isNonzero = _BitScanReverse(&index, mask);  
   if (isNonzero)  
   {  
      cout << "Mask: " << mask << " Index: " << index << endl;  
   }  
   else  
   {  
      cout << "No set bits found.  Mask is zero." << endl;  
   }  
}  
```  
  
## <a name="input"></a>입력  
  
```  
12  
```  
  
## <a name="sample-output"></a>샘플 출력  
  
```  
Enter a positive integer as the mask:   
Mask: 12 Index: 3  
```  
  
**Microsoft 전용 종료**  
  
## <a name="see-also"></a>참고 항목  
 [컴파일러 내장 함수](../intrinsics/compiler-intrinsics.md)