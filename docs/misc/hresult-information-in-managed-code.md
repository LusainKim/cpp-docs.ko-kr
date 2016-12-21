---
title: "관리 되는 코드에서 HRESULT 정보 | Microsoft Docs"
ms.custom: ""
ms.date: "12/15/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "HRESULT, 관리 되는 VSPackages"
  - "VSPackages, HRESULT 정보"
ms.assetid: 0795ee94-17a8-4327-bf57-27cd5e312a4c
caps.latest.revision: 29
caps.handback.revision: 29
manager: "douge"
---
# 관리 되는 코드에서 HRESULT 정보
HRESULT 반환 값을 발견할 경우 관리 코드와 COM 간의 상호 작용으로 인해 문제가 발생할 수 있습니다.  
  
 COM 인터페이스에서 HRESULT 반환 값은 다음과 같은 역할을 할 수 있습니다.  
  
-   오류 정보\(예: <xref:Microsoft.VisualStudio.VSConstants.E_INVALIDARG>\)를 제공합니다.  
  
-   일반적인 프로그램 동작에 대한 상태 정보를 제공합니다.  
  
 COM이 관리 코드를 호출하는 경우 HRESULT로 인해 다음과 같은 문제가 발생할 수 있습니다.  
  
-   0보다 작은 HRESULT 값\(오류 코드\)을 반환하는 COM 함수가 예외를 생성합니다.  
  
-   둘 이상의 서로 다른 성공 코드를 정기적으로 반환하는 COM 메서드\(예: <xref:Microsoft.VisualStudio.VSConstants.S_OK> 또는 <xref:Microsoft.VisualStudio.VSConstants.S_FALSE>\)를 구분할 수 없습니다.  
  
 대부분의 [!INCLUDE[vsipsdk](../mfc/includes/vsipsdk_md.md)] COM 함수는 0보다 작은 HRESULT 값을 반환하거나 여러 성공 코드를 반환하기 때문에 [!INCLUDE[vsipsdk](../mfc/includes/vsipsdk_md.md)] interop 어셈블리는 메서드 서명이 유지되도록 작성되었습니다. 모든 [!INCLUDE[vsipsdk](../mfc/includes/vsipsdk_md.md)] interop 메서드는 `int` 형식입니다. HRESULT 값은 변경 및 예외 생성 없이 interop 계층을 통해 전달됩니다.  
  
 COM 함수는 호출하는 관리되는 메서드에 HRESULT를 반환하므로 호출하는 메서드가 HRESULT를 확인하고 필요에 따라 예외를 발생시켜야 합니다.  
  
## COM에서 관리 코드로 반환되는 HRESULT 처리  
 관리 코드에서 COM 인터페이스를 호출하는 경우 HRESULT 값을 검사하고 필요에 따라 예외를 발생시킵니다.<xref:Microsoft.VisualStudio.ErrorHandler> 클래스에는 전달된 HRESULT의 값에 따라 COM 예외를 발생시키는 <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure%2A> 메서드가 포함되어 있습니다.  
  
 기본적으로 <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure%2A>는 0보다 작은 값을 가진 HRESULT가 전달될 때마다 예외를 발생시킵니다. 이러한 HRESULT가 허용되는 값이며 예외가 발생하지 않아야 하는 경우 값이 테스트된 후에 추가 HRESULT 값을 <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure%2A>에 전달해야 합니다. 테스트되는 HRESULT가 <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure%2A>에 명시적으로 전달된 HRESULT 값과 일치하는 경우 예외가 발생하지 않습니다.  
  
> [!NOTE]
>  <xref:Microsoft.VisualStudio.VSConstants> 클래스에는 일반적인 HRESULT\(예: <xref:Microsoft.VisualStudio.VSConstants.S_OK> 및 <xref:Microsoft.VisualStudio.VSConstants.E_NOTIMPL>\) 및 [!INCLUDE[vsprvs](../assembler/masm/includes/vsprvs_md.md)] HRESULT\(예: <xref:Microsoft.VisualStudio.VSConstants.VS_E_INCOMPATIBLEDOCDATA> 및 <xref:Microsoft.VisualStudio.VSConstants.VS_E_UNSUPPORTEDFORMAT>\)에 대한 상수가 포함되어 있습니다. 또한 <xref:Microsoft.VisualStudio.VSConstants>는 COM의 SUCCEEDED 및 FAILED 매크로에 해당하는 <xref:Microsoft.VisualStudio.ErrorHandler.Succeeded%2A> 및 <xref:Microsoft.VisualStudio.ErrorHandler.Failed%2A> 메서드를 제공합니다.  
  
 예를 들어 <xref:Microsoft.VisualStudio.VSConstants.E_NOTIMPL>은 허용되는 반환 값이지만 0보다 작은 다른 HRESULT는 오류를 나타내는 다음 함수 호출을 고려해 보세요.  
  
 [!code-vb[VSSDKHRESULTInformation#1](../misc/codesnippet/VisualBasic/hresult-information-in-managed-code_1.vb)]
 [!code-cs[VSSDKHRESULTInformation#1](../misc/codesnippet/CSharp/hresult-information-in-managed-code_1.cs)]  
  
 허용되는 반환 값이 둘 이상 있는 경우 <xref:Microsoft.VisualStudio.ErrorHandler.ThrowOnFailure%2A> 호출의 목록에 다른 HRESULT 값을 추가하면 됩니다.  
  
 [!code-vb[VSSDKHRESULTInformation#2](../misc/codesnippet/VisualBasic/hresult-information-in-managed-code_2.vb)]
 [!code-cs[VSSDKHRESULTInformation#2](../misc/codesnippet/CSharp/hresult-information-in-managed-code_2.cs)]  
  
## 관리 코드에서 COM으로 HRESULT 반환  
 예외가 발생하지 않는 경우 관리 코드가 호출한 COM 함수에 <xref:Microsoft.VisualStudio.VSConstants.S_OK>를 반환합니다. COM interop는 관리 코드에서 강력한 형식의 일반적인 예외를 지원합니다. 예를 들어 허용되지 않는 `null` 인수를 받은 메서드는 <xref:System.ArgumentNullException>을 발생시킵니다.  
  
 어떤 예외를 발생시켜야 하는지 모르지만 COM에 반환하려는 HRESULT를 알고 있는 경우 <xref:System.Runtime.InteropServices.Marshal.ThrowExceptionForHR%2A> 메서드를 사용하여 적절한 예외를 발생시킬 수 있습니다. 이는 비표준 오류\(예: <xref:Microsoft.VisualStudio.VSConstants.VS_E_INCOMPATIBLEDOCDATA>\)에도 적용됩니다.<xref:System.Runtime.InteropServices.Marshal.ThrowExceptionForHR%2A>이 전달된 HRESULT를 강력한 형식의 예외에 매핑하려고 합니다. 매핑할 수 없는 경우 대신 일반 COM 예외를 발생시킵니다. 최종 결과로, 관리 코드에서 <xref:System.Runtime.InteropServices.Marshal.ThrowExceptionForHR%2A>에 전달하는 HRESULT가 호출한 COM 함수에 반환됩니다.  
  
> [!NOTE]
>  예외가 발생하면 성능이 저하되며 비정상적인 프로그램 상태를 나타냅니다. 자주 발생하는 상태는 예외를 발생시키는 대신 인라인으로 처리해야 합니다.  
  
## 참고 항목  
 [관리되는 VSPackage](../misc/managed-vspackages.md)   
 [비관리 코드와의 상호 운용](../Topic/Interoperating%20with%20Unmanaged%20Code.md)   
 [방법: HRESULT 및 예외 매핑](../Topic/How%20to:%20Map%20HRESULTs%20and%20Exceptions.md)   
 [상호 운용을 위한 COM 구성 요소 빌드](http://msdn.microsoft.com/ko-kr/7a2c657a-cfef-40f0-bed3-7c2c0ac4abdf)   
 [관리되는 VSPackage](../misc/managed-vspackages.md)