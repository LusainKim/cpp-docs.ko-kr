---
title: "프로젝트 빌드 오류 PRJ0008 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-tools
ms.tgt_pltfrm: 
ms.topic: error-reference
f1_keywords: PRJ0008
dev_langs: C++
helpviewer_keywords: PRJ0008
ms.assetid: 6bf7f17a-d2a8-4826-99c7-d600d846952f
caps.latest.revision: "7"
author: corob-msft
ms.author: corob
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 1740b0cf1edfc90258de4fe26478298ddf2875c6
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="project-build-error-prj0008"></a>프로젝트 빌드 오류 PRJ0008
'File' 파일을 삭제 하지 못했습니다.  
  
 **파일이 다른 프로세스에서 열려 있지 않으면 및 쓰기 금지 되어 있는지 확인 합니다.**  
  
 다시 작성 중 정리, Visual c + + 빌드에 대해 알려진된 중간 파일과 출력 파일을 모두 뿐 아니라 삭제 와일드 카드 지정에 충족 하는 모든 파일은 **정리할 때 삭제할 확장명** 속성에는 [일반 구성 설정 속성 페이지](../../ide/general-property-page-project.md)합니다.  
  
 Visual c + + 파일을 삭제할 수 없는 경우이 오류가 나타납니다. 이 오류를 해결 하려면 파일 및 디렉터리 쓰기 가능한 빌드를 수행 하는 사용자에 대 한 이어야 합니다.