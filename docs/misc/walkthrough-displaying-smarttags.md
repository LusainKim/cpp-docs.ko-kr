---
title: "연습: 스마트 태그 표시 | Microsoft Docs"
ms.custom: ""
ms.date: "11/17/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "편집기[Visual Studio SDK], 새로 만들기 - 스마트 태그"
ms.assetid: 10bb4f69-b259-41f0-b91a-69b04385d9a5
caps.latest.revision: 31
caps.handback.revision: 31
manager: "douge"
---
# 연습: 스마트 태그 표시
스마트 태그는 전구로 대체되었습니다.[연습: 전구 추천 단어 표시](../Topic/Walkthrough:%20Displaying%20Light%20Bulb%20Suggestions.md)을 참조하세요.  
  
 스마트 태그는 일련의 동작을 표시하도록 확장되는 텍스트 태그입니다. 예를 들어 Visual Basic 또는 Visual C\# 프로젝트에서 변수 이름과 같은 식별자의 이름을 바꾸면 단어 아래에 빨간색 선이 나타납니다. 밑줄 위로 포인터를 이동하면 포인터 근처에 단추가 표시됩니다. 단추를 클릭하면 제안 동작이 표시됩니다\(예: **IsRead의 이름을 IsReady로 바꾸기**\). 동작을 클릭하면 프로젝트에서 **IsRead**에 대한 모든 참조의 이름이 **IsReady**로 바뀝니다.  
  
 스마트 태그는 편집기에서 IntelliSense 구현의 일부이지만 <xref:Microsoft.VisualStudio.Language.Intellisense.SmartTag>를 서브클래싱한 다음 <xref:Microsoft.VisualStudio.Text.Tagging.ITagger%601> 인터페이스 및 <xref:Microsoft.VisualStudio.Text.Tagging.IViewTaggerProvider> 인터페이스를 구현하여 스마트 태그를 구현할 수 있습니다.  
  
> [!NOTE]
>  비슷한 방식으로 다른 종류의 태그를 구현할 수 있습니다.  
  
 다음 연습에서는 현재 단어에 표시되고 두 개의 제안 동작\(**대문자로 변환** 및 **를 소문자로 변환**\)이 있는 스마트 태그를 만드는 방법을 보여 줍니다.  
  
## 사전 요구 사항  
 이 연습을 수행하려면 Visual Studio SDK를 설치해야 합니다. 자세한 내용은 [Visual Studio SDK](../Topic/Visual%20Studio%20SDK.md)을 참조하세요.  
  
## MEF\(Managed Extensibility Framework\) 프로젝트 만들기  
  
#### MEF 프로젝트를 만들려면  
  
1.  편집기 분류자 프로젝트를 만듭니다. 솔루션의 이름을 `SmartTagTest`로 지정합니다.  
  
2.  VSIX 매니페스트 편집기에서 source.extension.vsixmanifest 파일을 엽니다.  
  
3.  **자산** 섹션에 `Microsoft.VisualStudio.MefComponent` 형식이 포함되어 있고, **소스**가 `A project in current solution`으로 설정되었으며, **프로젝트**가 SmartTagTest.dll로 설정되었는지 확인합니다.  
  
4.  source.extension.vsixmanifest를 저장하고 닫습니다.  
  
5.  프로젝트에 대한 다음 참조를 추가하고 **CopyLocal**을 `false`로 설정합니다.  
  
     Microsoft.VisualStudio.Language.Intellisense  
  
6.  기존 클래스 파일을 삭제합니다.  
  
## 스마트 태그에 대한 태거 구현  
  
#### 스마트 태그에 대한 태거를 구현하려면  
  
1.  클래스 파일을 추가하고 이름을 `TestSmartTag`로 지정합니다.  
  
2.  다음 가져오기를 추가합니다.  
  
     [!code-cs[VSSDKSmartTagTest#1](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_1.cs)]
     [!code-vb[VSSDKSmartTagTest#1](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_1.vb)]  
  
3.  <xref:Microsoft.VisualStudio.Language.Intellisense.SmartTag>에서 상속하는 `TestSmartTag`라는 클래스를 추가합니다.  
  
     [!code-cs[VSSDKSmartTagTest#2](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_2.cs)]
     [!code-vb[VSSDKSmartTagTest#2](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_2.vb)]  
  
4.  단어의 첫 문자 아래에 파란색 선을 표시하는 <xref:Microsoft.VisualStudio.Language.Intellisense.SmartTagType>를 <xref:Microsoft.VisualStudio.Language.Intellisense.SmartTagType>으로 사용하여 기본 생성자를 호출하는 이 클래스에 대한 생성자를 추가합니다.<xref:Microsoft.VisualStudio.Language.Intellisense.SmartTagType>을 사용하는 경우 단어의 마지막 문자 아래에 빨간색 선이 표시됩니다.  
  
     [!code-cs[VSSDKSmartTagTest#3](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_3.cs)]
     [!code-vb[VSSDKSmartTagTest#3](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_3.vb)]  
  
5.  `TestSmartTag` 형식의 <xref:Microsoft.VisualStudio.Text.Tagging.ITagger%601>에서 상속하고 <xref:System.IDisposable>을 구현하는 `TestSmartTagger`라는 클래스를 추가합니다.  
  
     [!code-cs[VSSDKSmartTagTest#4](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_4.cs)]
     [!code-vb[VSSDKSmartTagTest#4](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_4.vb)]  
  
6.  태거 클래스에 다음과 같은 전용 필드를 추가합니다.  
  
     [!code-cs[VSSDKSmartTagTest#5](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_5.cs)]
     [!code-vb[VSSDKSmartTagTest#5](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_5.vb)]  
  
7.  전용 필드를 설정하고 <xref:Microsoft.VisualStudio.Text.Editor.ITextView.LayoutChanged> 이벤트를 구독하는 생성자를 추가합니다.  
  
     [!code-cs[VSSDKSmartTagTest#6](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_6.cs)]
     [!code-vb[VSSDKSmartTagTest#6](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_6.vb)]  
  
8.  현재 단어에 대한 태그가 만들어지도록 <xref:Microsoft.VisualStudio.Text.Tagging.ITagger%601.GetTags%2A>를 구현합니다. 이 메서드는 나중에 설명하는 private 메서드 `GetSmartTagActions`도 호출합니다.  
  
     [!code-cs[VSSDKSmartTagTest#7](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_7.cs)]
     [!code-vb[VSSDKSmartTagTest#7](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_7.vb)]  
  
9. `GetSmartTagActions` 메서드를 추가하여 스마트 태그 동작을 설정합니다. 동작 자체는 이후 단계에서 구현됩니다.  
  
     [!code-cs[VSSDKSmartTagTest#8](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_8.cs)]
     [!code-vb[VSSDKSmartTagTest#8](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_8.vb)]  
  
10. `SmartTagsChanged` 이벤트를 선언합니다.  
  
     [!code-cs[VSSDKSmartTagTest#9](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_9.cs)]
     [!code-vb[VSSDKSmartTagTest#9](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_9.vb)]  
  
11. <xref:Microsoft.VisualStudio.Text.Tagging.ITagger%601.GetTags%2A>가 호출되도록 하는 `TagsChanged` 이벤트를 발생시키는 `OnLayoutChanged` 이벤트 처리기를 구현합니다.  
  
     [!code-cs[VSSDKSmartTagTest#10](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_10.cs)]
     [!code-vb[VSSDKSmartTagTest#10](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_10.vb)]  
  
12. <xref:Microsoft.VisualStudio.Text.Editor.ITextView.LayoutChanged> 이벤트를 구독 취소하도록 <xref:System.IDisposable.Dispose%2A> 메서드를 구현합니다.  
  
     [!code-cs[VSSDKSmartTagTest#11](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_11.cs)]
     [!code-vb[VSSDKSmartTagTest#11](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_11.vb)]  
  
## 스마트 태그 태거 공급자 구현  
  
#### 스마트 태그 태거 공급자를 구현하려면  
  
1.  <xref:Microsoft.VisualStudio.Text.Tagging.IViewTaggerProvider>에서 상속하는 `TestSmartTagTaggerProvider`라는 클래스를 추가합니다.<xref:Microsoft.VisualStudio.Utilities.ContentTypeAttribute>로 "text"를 사용하고, <xref:Microsoft.VisualStudio.Utilities.OrderAttribute>로 Before\="default"를 사용하고, <xref:Microsoft.VisualStudio.Text.Tagging.TagTypeAttribute>로 <xref:Microsoft.VisualStudio.Language.Intellisense.SmartTag>를 사용하여 내보냅니다.  
  
     [!code-cs[VSSDKSmartTagTest#12](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_12.cs)]
     [!code-vb[VSSDKSmartTagTest#12](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_12.vb)]  
  
2.  <xref:Microsoft.VisualStudio.Text.Operations.ITextStructureNavigatorSelectorService>를 속성으로 가져옵니다.  
  
     [!code-cs[VSSDKSmartTagTest#13](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_13.cs)]
     [!code-vb[VSSDKSmartTagTest#13](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_13.vb)]  
  
3.  <xref:Microsoft.VisualStudio.Text.Tagging.IViewTaggerProvider.CreateTagger%2A> 메서드를 구현합니다.  
  
     [!code-cs[VSSDKSmartTagTest#14](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_14.cs)]
     [!code-vb[VSSDKSmartTagTest#14](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_14.vb)]  
  
## 스마트 태그 동작 구현  
  
#### 스마트 태그 동작을 구현하려면  
  
1.  두 개의 클래스를 만듭니다. 첫 번째 클래스의 이름은 `UpperCaseSmartTagAction`이고 두 번째 클래스의 이름은 `LowerCaseSmartTagAction`입니다. 두 클래스 모두 <xref:Microsoft.VisualStudio.Language.Intellisense.ISmartTagAction>를 구현합니다.  
  
     [!code-cs[VSSDKSmartTagTest#15](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_15.cs)]
     [!code-vb[VSSDKSmartTagTest#15](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_15.vb)]  
  
     [!code-cs[VSSDKSmartTagTest#16](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_16.cs)]
     [!code-vb[VSSDKSmartTagTest#16](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_16.vb)]  
  
 한 클래스는 <xref:System.String.ToUpper%2A>를 호출하고 다른 클래스는 <xref:System.String.ToLower%2A>를 호출한다는 점을 제외하고 두 클래스는 유사합니다. 다음 단계에서는 대문자 동작 클래스만 설명하지만 두 클래스를 모두 구현해야 합니다. 대문자 동작 구현 단계를 소문자 동작 구현 패턴으로 사용합니다.  
  
1.  전용 필드 집합을 선언합니다.  
  
     [!code-cs[VSSDKSmartTagTest#17](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_17.cs)]
     [!code-vb[VSSDKSmartTagTest#17](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_17.vb)]  
  
2.  필드를 설정하는 생성자를 추가합니다.  
  
     [!code-cs[VSSDKSmartTagTest#18](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_18.cs)]
     [!code-vb[VSSDKSmartTagTest#18](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_18.vb)]  
  
3.  속성을 다음과 같이 구현합니다.  
  
     [!code-cs[VSSDKSmartTagTest#19](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_19.cs)]
     [!code-vb[VSSDKSmartTagTest#19](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_19.vb)]  
  
4.  범위에 있는 텍스트를 해당 대문자로 바꾸어 <xref:Microsoft.VisualStudio.Language.Intellisense.ISmartTagAction.Invoke%2A> 메서드를 구현합니다.  
  
     [!code-cs[VSSDKSmartTagTest#20](../misc/codesnippet/CSharp/walkthrough-displaying-smarttags_20.cs)]
     [!code-vb[VSSDKSmartTagTest#20](../misc/codesnippet/VisualBasic/walkthrough-displaying-smarttags_20.vb)]  
  
## 코드 빌드 및 테스트  
 이 코드를 테스트하려면 SmartTagTest 솔루션을 빌드하고 실험적 인스턴스에서 실행합니다.  
  
#### SmartTagTest 솔루션을 빌드하고 테스트하려면  
  
1.  솔루션을 빌드합니다.  
  
2.  디버거에서 이 프로젝트를 실행하면 Visual Studio의 두 번째 인스턴스가 인스턴스화됩니다.  
  
3.  텍스트 파일을 만들고 일부 텍스트를 입력합니다.  
  
     텍스트에서 첫 번째 단어의 첫 문자 아래에 파란색 선이 표시됩니다.  
  
4.  파란색 선 위로 포인터를 이동합니다.  
  
     포인터 근처에 단추가 표시됩니다.  
  
5.  단추를 클릭하면 두 가지 제안 동작\(**대문자로 변환** 및 **소문자로 변환**\)이 표시됩니다. 첫 번째 동작을 클릭하면 현재 단어의 모든 텍스트가 대문자로 변환됩니다. 두 번째 동작을 클릭하면 모든 텍스트가 소문자로 변환됩니다.  
  
## 참고 항목  
 [연습: 파일 이름 확장명에 콘텐츠 형식 연결](../Topic/Walkthrough:%20Linking%20a%20Content%20Type%20to%20a%20File%20Name%20Extension.md)