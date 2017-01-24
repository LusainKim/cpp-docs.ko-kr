---
title: "방법: Windows Forms를 사용하는 도구 상자 컨트롤 만들기 | Microsoft Docs"
ms.custom: ""
ms.date: "11/16/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "도구 상자 컨트롤"
  - "winforms"
  - "도구 상자"
ms.assetid: abbd3c3c-3a6e-4539-bd6c-a5891dead234
caps.latest.revision: 12
caps.handback.revision: 12
manager: "douge"
---
# 방법: Windows Forms를 사용하는 도구 상자 컨트롤 만들기
확장이 설치될 때 [!INCLUDE[vssdk_dev11_long](../misc/includes/vssdk_dev11_long_md.md)]에 들어 있는 Windows Forms 도구 상자 컨트롤 템플릿을 통해 자동으로 **도구 상자**에 추가된 Windows Forms 컨트롤을 만들 수 있습니다. 이 항목에서는 템플릿을 사용하여 다른 사용자에게 배포할 수 있는 **도구 상자** 컨트롤을 만드는 방법을 보여 줍니다.  
  
> [!NOTE]
>  Visual Studio SDK를 다운로드하는 방법을 알아보려면 MSDN 웹 사이트의 [Visual Studio 확장성 개발자 센터](http://go.microsoft.com/fwlink/?linkid=121964)를 참조하세요.  
  
## 도구 상자 컨트롤 만들기  
 Windows Forms 도구 상자 컨트롤 템플릿을 사용하여 프로젝트를 만든 다음 디자이너에서 UI\(사용자 인터페이스\)를 빌드합니다.  
  
#### Windows Forms 도구 상자 컨트롤 프로젝트를 만들려면  
  
1.  **파일** 메뉴에서 **새로 만들기**를 클릭한 다음 **프로젝트**를 클릭합니다.  
  
2.  **새 프로젝트** 대화 상자의 **설치된 템플릿**에서 원하는 프로그래밍 언어에 대한 노드를 클릭한 다음 **확장성**을 클릭합니다. 프로젝트 형식 목록에서 **Windows Forms 도구 상자 컨트롤**을 선택합니다.  
  
3.  **이름** 상자에 원하는 프로젝트 이름을 입력합니다.**확인**을 클릭합니다.  
  
     Visual Studio는 배포할 VSIX 매니페스트 및 **도구 상자**에 컨트롤을 넣기 위한 특성, 사용자 지정 컨트롤이 포함된 솔루션을 만듭니다.  
  
#### 컨트롤 UI를 빌드하려면  
  
1.  **솔루션 탐색기**에서 ToolboxControl.cs를 두 번 클릭하여 디자이너에서 이 파일을 엽니다.  
  
2.  **도구 상자**에서 원하는 컨트롤을 디자인 화면에 끌어와 디자인에 따라 정렬합니다.  
  
3.  **속성** 창에서 사용자 지정 컨트롤 및 자식 컨트롤에 대해 public 속성을 설정합니다.  
  
## 컨트롤 코딩  
 기본적으로 컨트롤은 솔루션과 이름이 같은 **도구 상자** 항목 그룹에서 **ToolboxControl1**로 **도구 상자**에 표시됩니다. 이러한 이름은 ToolboxControl.cs 파일에서 변경할 수 있습니다.  
  
#### 컨트롤을 코딩하려면  
  
1.  **솔루션 탐색기**에서 ToolboxControl.cs를 마우스 오른쪽 단추로 클릭한 다음 **코드 보기**를 클릭하여 코드 보기에서 파일을 엽니다.  
  
2.  컨트롤을 구현하는 partial 클래스 정의에서 클래스 이름을 마우스 오른쪽 단추로 클릭하고 **리팩터링**, **이름 바꾸기**를 차례로 클릭합니다. 클래스 이름을 컨트롤이 설치될 때 **도구 상자**에 표시될 이름으로 변경합니다.  
  
3.  클래스 정의 바로 위의 `ProvideToolboxControl` 특성 선언에서 첫 번째 매개 변수 값을 **도구 상자**의 컨트롤을 호스트하는 항목 그룹의 이름으로 변경합니다.  
  
     다음 예제에서는 `General` 항목 그룹에서 `Counter`라는 컨트롤의 `ProvideToolboxControl` 특성 및 조정된 클래스 정의를 보여 줍니다.  
  
     [!code-cs[ToolboxControlWinForms#07](../misc/codesnippet/CSharp/how-to-create-a-toolbox-control-that-uses-windows-forms_1.cs)]  
  
4.  컨트롤의 속성, 메서드 및 이벤트를 구현합니다.  
  
## 빌드, 테스트 및 배포  
 F5 키를 누르면 .vsix 배포 파일이 있는 프로젝트가 빌드되고 **도구 상자**에 컨트롤을 설치한 Visual Studio의 두 번째 인스턴스를 엽니다.  
  
#### 컨트롤을 빌드하고 테스트하려면  
  
1.  F5 키를 누릅니다.  
  
2.  Visual Studio의 새 인스턴스에서 Windows Forms 응용 프로그램 프로젝트를 만듭니다.  
  
3.  **도구 상자**에서 컨트롤을 찾아 디자인 화면으로 끕니다.  
  
4.  **속성** 창에서 속성이 예상대로 나타나는지 확인합니다.  
  
5.  메서드 및 이벤트를 테스트하는 데 필요한 코드 또는 추가 컨트롤을 추가합니다.  
  
6.  F5 키를 눌러 Windows Forms 응용 프로그램을 엽니다.  
  
7.  컨트롤의 속성, 메서드 및 이벤트가 예상대로 동작하는지 확인합니다.  
  
#### 컨트롤을 배포하려면  
  
1.  테스트된 프로젝트를 빌드한 후 파일 탐색기에서 프로젝트의 \\bin\\debug\\ 폴더를 열고 .vsix 파일을 찾습니다.  
  
2.  네트워크 또는 웹 사이트에 .vsix 파일을 업로드합니다.  
  
     파일을 [Visual Studio 갤러리](http://go.microsoft.com/fwlink/?LinkID=123847) 웹 사이트에 업로드하면 다른 사용자가 Visual Studio의 **확장 관리자**를 사용하여 컨트롤을 찾아 설치할 수 있습니다.  
  
## 참고 항목  
 [WPF 도구 상자 컨트롤 만들기](../Topic/Creating%20a%20WPF%20Toolbox%20Control.md)