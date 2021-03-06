---
title: "문자열 편집기 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: article
f1_keywords: vc.editors.string.F1
dev_langs: C++
helpviewer_keywords:
- String editor
- string tables
- string tables, String editor
- string editing
- string editing, string tables
- resource editors, String editor
- strings [C++], editing
ms.assetid: f71ab8de-3068-4e29-8e28-5a33d18dd416
caps.latest.revision: "15"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: f0d0f368ec82e46a72977b574b1632bf1d9d6d84
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="string-editor"></a>문자열 편집기
문자열 테이블은 응용 프로그램의 모든 문자열에 대한 ID, 값 및 캡션 목록이 포함된 Windows 리소스입니다. 예를 들어 상태 표시줄 프롬프트는 문자열 테이블에 있습니다.  
  
 응용 프로그램을 개발하는 동안 각 언어 또는 조건에 하나씩 여러 문자열 테이블을 만들 수 있습니다. 그러나 실행 가능 모듈에는 문자열 테이블이 하나만 포함됩니다. 테이블을 서로 다른 DLL에 삽입하면 실행 중인 응용 프로그램이 여러 문자열 테이블을 참조할 수 있습니다.  
  
 문자열 테이블을 사용하면 응용 프로그램을 여러 언어로 쉽게 지역화할 수 있습니다. 모든 문자열이 한 문자열 테이블에 있으면 소스 코드를 변경하지 않고 문자열과 기타 리소스를 번역하여 응용 프로그램을 지역화할 수 있습니다. 일반적으로 이 방법이 소스 파일에서 다양한 문자열을 수동으로 찾고 바꾸는 방법보다 더 바람직합니다.  
  
 문자열 편집기를 사용하여 다음을 수행할 수 있습니다.  
  
-   [문자열을 하나 이상 검색합니다](../windows/finding-a-string.md).  
  
-   [새 항목을 문자열 테이블에 빠르게 삽입합니다](../windows/adding-or-deleting-a-string.md) .  
  
-   [리소스 파일 사이에 문자열을 이동합니다.](../windows/moving-a-string-from-one-resource-file-to-another.md)  
  
-   [ID, 값 및 캡션 속성에 대한 바로 편집을 사용](../windows/changing-the-properties-of-a-string.md) 하고 변경 내용을 즉시 확인합니다.  
  
-   [여러 문자열의 Caption 속성을 변경합니다.](../windows/changing-the-caption-property-of-multiple-strings.md)  
  
-   [문자열에 형식 지정 또는 특수 문자를 추가합니다.](../windows/adding-formatting-or-special-characters-to-a-string.md)  
  
    > [!NOTE]
    >  Windows에서는 빈 문자열 테이블을 만들 수 없습니다. 항목 없이 문자열 테이블을 만들면 리소스 파일을 저장할 때 해당 테이블이 자동으로 삭제됩니다.  
  
 관리 되는 프로젝트 (공용 언어 런타임을 대상으로 프로젝트)에 리소스를 추가 하는 방법에 대 한 정보를 참조 하십시오 [데스크톱 응용 프로그램의 리소스](/dotnet/framework/resources/index) 에 *.NET Framework 개발자 가이드입니다.* 를 참조하세요. 관리되는 프로젝트에 리소스 파일 추가, 리소스 액세스, 정적 리소스 표시, 속성에 리소스 문자열 할당 등의 작업을 수동으로 수행하는 방법에 대한 자세한 내용은 [연습: Windows Forms 지역화](http://msdn.microsoft.com/en-us/9a96220d-a19b-4de0-9f48-01e5d82679e5) 및 [Walkthrough: Using Resources for Localization with ASP.NET](http://msdn.microsoft.com/Library/bb4e5b44-e2b0-48ab-bbe9-609fb33900b6).  
  
## <a name="requirements"></a>요구 사항  
 Win32  
  
## <a name="see-also"></a>참고 항목  
 [리소스 편집기](../windows/resource-editors.md)   
 [문자열](http://msdn.microsoft.com/library/windows/desktop/ms646979.aspx)   
 [문자열에 대 한](http://msdn.microsoft.com/library/windows/desktop/ms647465.aspx)

