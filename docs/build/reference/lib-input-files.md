---
title: "LIB 입력 파일 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: Lib
dev_langs: C++
helpviewer_keywords: input files, LIB
ms.assetid: e1236f0d-cd90-446b-b900-f311f456085c
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 5fea7a8700eb2f5a5deee7afd05af8b0de0e4e71
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="lib-input-files"></a>LIB 입력 파일
LIB에서 필요로 하는 입력된 파일은 다음 표에 나와 있는 것 처럼가 사용 되 고 있는 모드에 따라 달라 집니다.  
  
|모드|입력|  
|----------|-----------|  
|기본값 (빌드 또는 라이브러리를 수정 합니다.)|COFF 개체 (.obj) 파일, COFF 라이브러리 (.lib) 32 비트 개체 모델 (OMF) 개체 (.obj) 파일|  
|/EXTRACT와 멤버 추출|COFF 라이브러리 (.lib)|  
|내보내기 파일 및 가져오기 /def 라이브러리|모듈 정의 (.def) 파일, COFF 개체 (.obj) 파일, COFF 라이브러리 (.lib), 32 비트 OMF 개체 (.obj) 파일|  
  
> [!NOTE]
>  16 비트 버전의 LIB에서 만들어진 OMF 라이브러리는 32 비트 버전의 LIB에 입력으로 사용할 수 없습니다.  
  
## <a name="see-also"></a>참고 항목  
 [LIB 개요](../../build/reference/overview-of-lib.md)