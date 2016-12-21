---
title: "방법: 시각화 도우미 사용 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "vs.debug.dataviewer"
  - "vs.debug.stringviewer"
dev_langs: 
  - "FSharp"
  - "VB"
  - "CSharp"
  - "C++"
  - "JScript"
  - "VB"
  - "CSharp"
  - "C++"
helpviewer_keywords: 
  - "디버거, 시각화 도우미"
  - "시각화 도우미, 시각화 도우미 정보"
ms.assetid: d2611385-0134-4387-8c5a-979fe625a462
caps.latest.revision: 37
caps.handback.revision: 37
ms.author: "susanno"
manager: "douge"
---
# 방법: 시각화 도우미 사용
시각화 도우미를 사용하여 변수 또는 개체의 내용을 데이터 형식에 대해 의미 있는 방식으로 표시할 수 있습니다.  **DataTips**, **조사식** 창, **자동** 창 또는 **지역** 창에서 시각화 도우미를 사용할 수 있습니다.  
  
 Compact Framework에서는 시각화 도우미가 지원되지 않습니다.  
  
> [!NOTE]
>  **스토어** 앱에서는 표준 텍스트, HTML, XML 및 JSON 시각화 도우미만 지원됩니다.  사용자가 만든 사용자 지정 시각화 도우미는 지원되지 않습니다.  
  
### 시각화 도우미를 열려면  
  
1.  **DataTips**, **조사식**, **자동**, **지역** 또는 **간단한 조사식** 창에서 변수 이름 옆에 나타나는 돋보기 모양 아이콘을 클릭합니다.  
  
     시각화 도우미의 목록이 나타납니다.  
  
2.  사용할 시각화 도우미를 클릭합니다.  
  
### 원격 디버깅하는 동안 관리 코드에 시각화 도우미를 사용하려면  
  
-   디버깅 세션을 시작하기 전에 시각화 도우미 DLL을 원격 컴퓨터에 복사합니다.  
  
     DLL에 대한 경로는 원격 컴퓨터와 로컬 컴퓨터에서 같아야 합니다.  이 경로는 다음 위치 중 하나일 수 있습니다.  
  
     *Visual Studio 설치 경로*`\Common7\Packages\Debugger\Visualizers`  
  
     또는  
  
     `My Documents\Visual Studio 2010\Visualizers`*Visual Studio 버전*`\Visualizers`  
  
## 참고 항목  
 [시각화 도우미](../Topic/Create%20Custom%20Visualizers%20of%20Data.md)   
 [방법: 시각화 도우미 설치](../Topic/How%20to:%20Install%20a%20Visualizer.md)   
 [방법: 시각화 도우미 작성](../Topic/How%20to:%20Write%20a%20Visualizer.md)   
 [데이터 팁의 데이터 값 보기](../Topic/View%20data%20values%20in%20Data%20Tips%20%20in%20the%20code%20editor.md)