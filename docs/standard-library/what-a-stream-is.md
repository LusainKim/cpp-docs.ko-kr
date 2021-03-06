---
title: "스트림이란 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-standard-libraries
ms.tgt_pltfrm: 
ms.topic: article
dev_langs: C++
helpviewer_keywords:
- reading data [C++], iostream programming
- data [C++], reading
- streams [C++], in iostream classes
- streams [C++]
ms.assetid: a7e661e9-6cd1-4543-a9a4-c58ee9fd32f3
caps.latest.revision: "8"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 7084a0fb74d963532e01623e8e9047768c67f801
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="what-a-stream-is"></a>What a Stream Is
C++에도 C와 마찬가지로 기본 제공 입력/출력 기능은 없습니다. 하지만, 모든 C++ 컴파일러는 iostream class라고 알려진 체계적이고 객체지향화된 I/O 패키지를 번들로(기본으로) 제공합니다. 스트림은 iostream 클래스의 중요 컨셉입니다. 스트림 객체는 Byte 데이터에 대한 원본과 대상의 역할을 하는 스마트 파일로 간주하면 됩니다. 스크림의 형질(특성)은 클래스 자체와 삽입(Insertion)과 추출(Extraction) 연산자에 의해 커스터마이징됨으로서 결정됩니다.  
  
 디스크 운영 시스템은 장치 드라이버를 통해, 키보드, 스크린, 프린터 그리고 통신 포트를 마치 확장된 파일인 것 처럼 처리합니다. Iostream 클래스는 이 다수의 확장된 파일과 상호 작용합니다. 내장 클래스들은 Disk I/O와 동일한 Syntax를 이용하여 메모리로부터 읽기와 쓰기를 지원하므로, 스트림 클래스들을 파생하기가 한결 쉬워집니다.  
  
## <a name="in-this-section"></a>섹션 내용  
 [입력/출력 대체](../standard-library/input-output-alternatives.md)  
  
## <a name="see-also"></a>참고 항목  
 [iostream 프로그래밍](../standard-library/iostream-programming.md)

