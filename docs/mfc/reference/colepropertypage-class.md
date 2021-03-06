---
title: "클래스에서는 COlePropertyPage | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- COlePropertyPage
- AFXCTL/COlePropertyPage
- AFXCTL/COlePropertyPage::COlePropertyPage
- AFXCTL/COlePropertyPage::GetControlStatus
- AFXCTL/COlePropertyPage::GetObjectArray
- AFXCTL/COlePropertyPage::GetPageSite
- AFXCTL/COlePropertyPage::OVERWRITEApply
- AFXCTL/COlePropertyPage::IsModified
- AFXCTL/COlePropertyPage::OnEditProperty
- AFXCTL/COlePropertyPage::OnHelp
- AFXCTL/COlePropertyPage::OnInitDialog
- AFXCTL/COlePropertyPage::OnObjectsChanged
- AFXCTL/COlePropertyPage::OnSetPageSite
- AFXCTL/COlePropertyPage::SetControlStatus
- AFXCTL/COlePropertyPage::SetDialogResource
- AFXCTL/COlePropertyPage::SetHelpInfo
- AFXCTL/COlePropertyPage::SetModifiedFlag
- AFXCTL/COlePropertyPage::SetPageName
dev_langs: C++
helpviewer_keywords:
- COlePropertyPage [MFC], COlePropertyPage
- COlePropertyPage [MFC], GetControlStatus
- COlePropertyPage [MFC], GetObjectArray
- COlePropertyPage [MFC], GetPageSite
- COlePropertyPage [MFC], IgnoreApply
- COlePropertyPage [MFC], IsModified
- COlePropertyPage [MFC], OnEditProperty
- COlePropertyPage [MFC], OnHelp
- COlePropertyPage [MFC], OnInitDialog
- COlePropertyPage [MFC], OnObjectsChanged
- COlePropertyPage [MFC], OnSetPageSite
- COlePropertyPage [MFC], SetControlStatus
- COlePropertyPage [MFC], SetDialogResource
- COlePropertyPage [MFC], SetHelpInfo
- COlePropertyPage [MFC], SetModifiedFlag
- COlePropertyPage [MFC], SetPageName
ms.assetid: e9972872-8e6b-4550-905e-d36a274d64dc
caps.latest.revision: "23"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: cac788f0e7f691f28a6751d15971f117d753428c
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="colepropertypage-class"></a>에서는 COlePropertyPage 클래스
대화 상자와 유사한 그래픽 인터페이스의 사용자 지정 컨트롤의 속성을 표시하는 데 사용됩니다.  
  
## <a name="syntax"></a>구문  
  
```  
class AFX_NOVTABLE COlePropertyPage : public CDialog  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[COlePropertyPage::COlePropertyPage](#colepropertypage)|`COlePropertyPage` 개체를 생성합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[COlePropertyPage::GetControlStatus](#getcontrolstatus)|컨트롤의 값 수정 되었는지 여부를 나타냅니다.|  
|[COlePropertyPage::GetObjectArray](#getobjectarray)|속성 페이지에서 편집 중인 개체의 배열을 반환 합니다.|  
|[COlePropertyPage::GetPageSite](#getpagesite)|속성 페이지에 대 한 포인터를 반환 `IPropertyPageSite` 인터페이스입니다.|  
|[COlePropertyPage::IgnoreApply](#ignoreapply)|컨트롤 [적용] 단추를 사용 하지 않으면 결정 합니다.|  
|[COlePropertyPage::IsModified](#ismodified)|속성 페이지 수정 되었는지 여부를 나타냅니다.|  
|[COlePropertyPage::OnEditProperty](#oneditproperty)|사용자가 속성을 편집 하는 경우 프레임 워크에서 호출 됩니다.|  
|[COlePropertyPage::OnHelp](#onhelp)|사용자가 도움말을 호출할 때 프레임 워크에서 호출 됩니다.|  
|[COlePropertyPage::OnInitDialog](#oninitdialog)|속성 페이지를 초기화할 때 프레임 워크에서 호출 됩니다.|  
|[COlePropertyPage::OnObjectsChanged](#onobjectschanged)|새 속성을 가진 다른 OLE 컨트롤을 선택할 때 프레임 워크에서 호출 됩니다.|  
|[COlePropertyPage::OnSetPageSite](#onsetpagesite)|속성 프레임이 페이지의 사이트를 제공 하는 경우 프레임 워크에서 호출 됩니다.|  
|[COlePropertyPage::SetControlStatus](#setcontrolstatus)|컨트롤의 값 수정 되었는지 여부를 나타내는 플래그를 설정 합니다.|  
|[COlePropertyPage::SetDialogResource](#setdialogresource)|속성 페이지 대화 상자 리소스를 설정합니다.|  
|[COlePropertyPage::SetHelpInfo](#sethelpinfo)|해당 도움말 파일 및 도움말 컨텍스트 이름, 속성 페이지의 간략 한 도움말 텍스트를 설정합니다.|  
|[COlePropertyPage::SetModifiedFlag](#setmodifiedflag)|속성 페이지 수정 되었는지 여부를 나타내는 플래그를 설정 합니다.|  
|[COlePropertyPage::SetPageName](#setpagename)|속성 페이지의 이름 (캡션)를 설정합니다.|  
  
## <a name="remarks"></a>설명  
 예를 들어, 속성 페이지를 확인 하 고 컨트롤의 caption 속성을 수정할 수 있는 편집 컨트롤을 포함할 수 있습니다.  
  
 각 사용자 지정 또는 주식 컨트롤 속성에는 컨트롤의 사용자는 현재 속성 값을 확인 하 고 필요한 경우 해당 값을 수정할 수 있는 대화 상자 컨트롤이 있을 수 있습니다.  
  
 사용 하 여 대 한 자세한 내용은 `COlePropertyPage`, 문서를 참조 [ActiveX 컨트롤: 속성 페이지](../../mfc/mfc-activex-controls-property-pages.md)합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CDialog](../../mfc/reference/cdialog-class.md)  
  
 `COlePropertyPage`  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxctl.h  
  
##  <a name="colepropertypage"></a>COlePropertyPage::COlePropertyPage  
 `COlePropertyPage` 개체를 생성합니다.  
  
```  
COlePropertyPage(
    UINT idDlg,  
    UINT idCaption);
```  
  
### <a name="parameters"></a>매개 변수  
 *idDlg*  
 대화 상자 템플릿의 리소스 ID입니다.  
  
 *idCaption*  
 속성 페이지의 캡션의 리소스 ID입니다.  
  
### <a name="remarks"></a>설명  
 서브 클래스를 구현 하는 경우 `COlePropertyPage`, 하위 클래스의 생성자를 사용 해야는 `COlePropertyPage` 에 대화 상자 템플릿 리소스를 식별 하는 생성자의 속성 페이지를 바탕으로 하는 및의 캡션을 포함 하는 문자열 리소스입니다.  
  
##  <a name="getcontrolstatus"></a>COlePropertyPage::GetControlStatus  
 속성 페이지 컨트롤에 지정 된 리소스 id의 값이 수정 되었는지 여부를 결정 합니다.  
  
```  
BOOL GetControlStatus(UINT nID);
```  
  
### <a name="parameters"></a>매개 변수  
 `nID`  
 속성 페이지 컨트롤의 리소스 ID입니다.  
  
### <a name="return-value"></a>반환 값  
 **True 이면** 컨트롤 값이 고, 그렇지 않으면 수정 된 경우 **FALSE**합니다.  
  
##  <a name="getobjectarray"></a>COlePropertyPage::GetObjectArray  
 속성 페이지에서 편집 중인 개체의 배열을 반환 합니다.  
  
```  
LPDISPATCH* GetObjectArray(ULONG* pnObjects);
```  
  
### <a name="parameters"></a>매개 변수  
 `pnObjects`  
 페이지에서 편집 중인 개체의 수를 수신할 부호 없는 long 정수에 대 한 포인터입니다.  
  
### <a name="return-value"></a>반환 값  
 배열에 대 한 포인터 `IDispatch` 속성 페이지에 있는 각 컨트롤의 속성에 액세스 하는 데 사용 되는 포인터입니다. 호출자에 게 이러한 인터페이스 포인터를 해제 해야 합니다.  
  
### <a name="remarks"></a>설명  
 각 속성 페이지 개체를 유지 관리에 대 한 포인터의 배열에서 `IDispatch` 페이지에서 편집 중인 개체의 인터페이스입니다. 이 함수는 설정의 `pnObjects` 인수 해당 배열에 있는 요소의 수를 배열의 첫 번째 요소에 대 한 포인터를 반환 합니다.  
  
##  <a name="getpagesite"></a>COlePropertyPage::GetPageSite  
 속성 페이지에 대 한 포인터를 가져옵니다 `IPropertyPageSite` 인터페이스입니다.  
  
```  
LPPROPERTYPAGESITE GetPageSite();
```  
  
### <a name="return-value"></a>반환 값  
 속성 페이지에 대 한 포인터 `IPropertyPageSite` 인터페이스입니다.  
  
### <a name="remarks"></a>설명  
 컨트롤 및 컨테이너에는 사용자가 찾아 컨트롤 속성을 편집할 수 있도록 협력 합니다. 컨트롤 속성 페이지, 사용자를 관련된 집합 속성을 편집할 수 있는 OLE 개체는 각각 제공 합니다. 컨테이너 속성 페이지를 표시 하는 속성 프레임을 제공 합니다. 각 페이지에 대 한 속성 프레임 제공 수 있도록 지 원하는 페이지 사이트는 `IPropertyPageSite` 인터페이스입니다.  
  
##  <a name="ignoreapply"></a>COlePropertyPage::IgnoreApply  
 컨트롤 [적용] 단추를 사용 하지 않으면 결정 합니다.  
  
```  
void IgnoreApply(UINT nID);
```  
  
### <a name="parameters"></a>매개 변수  
 `nID`  
 무시 되는 컨트롤의 ID입니다.  
  
### <a name="remarks"></a>설명  
 속성 페이지의 적용 단추 페이지 컨트롤 속성의 값이 변경 되었으면 하는 경우에 활성화 됩니다. 적용 단추를 해당 값을 변경 하는 경우 사용할 발생 하지 않는 컨트롤을 지정 하려면이 함수를 사용 합니다.  
  
##  <a name="ismodified"></a>COlePropertyPage::IsModified  
 사용자 속성 페이지에 있는 모든 값을 변경 되었는지 여부를 결정 합니다.  
  
```  
BOOL IsModified();
```  
  
### <a name="return-value"></a>반환 값  
 **True 이면** 속성 페이지를 수정 합니다.  
  
##  <a name="oneditproperty"></a>COlePropertyPage::OnEditProperty  
 프레임 워크는 특정 속성은 편집 하는 경우이 함수를 호출 합니다.  
  
```  
virtual BOOL OnEditProperty(DISPID dispid);
```  
  
### <a name="parameters"></a>매개 변수  
 `dispid`  
 편집 중인 속성의 디스패치 ID입니다.  
  
### <a name="return-value"></a>반환 값  
 기본 구현은 반환 **FALSE**합니다. 이 함수의 재정의 반환할지 **TRUE**합니다.  
  
### <a name="remarks"></a>설명  
 페이지에서 해당 컨트롤에 포커스를 설정 하 여 재정의할 수 있습니다. 기본 구현은 아무 작업도 수행 하 고 반환 **FALSE**합니다.  
  
##  <a name="onhelp"></a>COlePropertyPage::OnHelp  
 프레임 워크 사용자 온라인 도움말을 요청 하는 경우이 함수를 호출 합니다.  
  
```  
virtual BOOL OnHelp(LPCTSTR lpszHelpDir);
```  
  
### <a name="parameters"></a>매개 변수  
 *lpszHelpDir*  
 속성 페이지의 도움말 파일을 포함 하는 디렉터리입니다.  
  
### <a name="return-value"></a>반환 값  
 기본 구현은 반환 **FALSE**합니다.  
  
### <a name="remarks"></a>설명  
 사용자가 도움말에 액세스 하는 경우 속성 페이지 위한 특별 한 조치를 수행 해야 하는 경우 재정의 합니다. 기본 구현은 아무 작업도 수행 하 고 반환 **FALSE**, WinHelp를 호출 하기 위해 프레임 워크 게 지시 합니다.  
  
##  <a name="oninitdialog"></a>COlePropertyPage::OnInitDialog  
 속성 페이지 대화 상자 초기화 될 때 프레임 워크에서이 함수를 호출 합니다.  
  
```  
virtual BOOL OnInitDialog();
```  
  
### <a name="return-value"></a>반환 값  
 기본 구현은 반환 **FALSE**합니다.  
  
### <a name="remarks"></a>설명  
 대화 상자 초기화 될 때 특별 한 조치가 필요한 경우 재정의 합니다. 기본 구현 호출 `CDialog::OnInitDialog` 반환 **FALSE**합니다.  
  
##  <a name="onobjectschanged"></a>COlePropertyPage::OnObjectsChanged  
 새 속성을 가진 다른 OLE 컨트롤을 선택할 때 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnObjectsChanged();
```  
  
### <a name="remarks"></a>설명  
 개발자 환경에서 OLE 컨트롤의 속성을 볼 때 해당 속성 페이지를 표시 하는 모덜리스 대화 상자가 사용 됩니다. 다른 컨트롤을 선택 하면 속성의 새 집합에 대 한 다양 한 속성 페이지에 표시 되어야 합니다. 프레임 워크 변경의 속성 페이지에 알리기 위해이 함수를 호출 합니다.  
  
 이 작업에 대 한 알림을 수신 하 고 특별 한 조치를 수행 하려면이 함수를 재정의 합니다.  
  
##  <a name="onsetpagesite"></a>COlePropertyPage::OnSetPageSite  
 프레임 워크 속성 프레임이 페이지 사이트 속성 페이지를 제공 하는 경우이 함수를 호출 합니다.  
  
```  
virtual void OnSetPageSite();
```  
  
### <a name="remarks"></a>설명  
 기본 구현은 페이지의 캡션을 로드 하 고 대화 상자 리소스에서 페이지의 크기를 결정 하려고 합니다. 이후 작업; 속성 페이지에서 필요로 하는 경우이 함수를 재정의 합니다. 재정의 기본 클래스 구현을 호출 해야 합니다.  
  
##  <a name="setcontrolstatus"></a>COlePropertyPage::SetControlStatus  
 속성 페이지 컨트롤의 상태를 변경합니다.  
  
```  
BOOL SetControlStatus(
    UINT nID,  
    BOOL bDirty);
```  
  
### <a name="parameters"></a>매개 변수  
 `nID`  
 속성 페이지 컨트롤의 ID를 포함 합니다.  
  
 `bDirty`  
 수정 된 속성 페이지의 필드를 지정 합니다. 로 설정 **TRUE** 필드 수정 된 경우 **FALSE** 수정 되지 않은 경우.  
  
### <a name="return-value"></a>반환 값  
 **True 이면**지정된 된 컨트롤 했으면 설정, **FALSE**합니다.  
  
### <a name="remarks"></a>설명  
 적용 단추를 선택 하거나 속성 페이지를 닫을 때 속성 페이지 컨트롤의 상태가 변경 되었으면 컨트롤의 속성을 적절 한 값으로 업데이트 됩니다.  
  
##  <a name="setdialogresource"></a>COlePropertyPage::SetDialogResource  
 속성 페이지 대화 상자 리소스를 설정합니다.  
  
```  
void SetDialogResource(HGLOBAL hDialog);
```  
  
### <a name="parameters"></a>매개 변수  
 *hDialog*  
 속성 페이지 대화 상자 리소스에 대 한 핸들입니다.  
  
##  <a name="sethelpinfo"></a>COlePropertyPage::SetHelpInfo  
 도구 설명 정보, 도움말 파일 이름 및 속성 페이지에 대 한 도움말 컨텍스트를 지정합니다.  
  
```  
void SetHelpInfo(
    LPCTSTR lpszDocString,  
    LPCTSTR lpszHelpFile = NULL,  
    DWORD dwHelpContext = 0);
```  
  
### <a name="parameters"></a>매개 변수  
 *lpszDocString*  
 상태 표시줄 또는 다른 위치에 표시 하기 위한 간단한 도움말 정보를 포함 하는 문자열입니다.  
  
 `lpszHelpFile`  
 속성 페이지의 도움말 파일의 이름입니다.  
  
 *dwHelpContext*  
 속성 페이지에 대 한 도움말 컨텍스트입니다.  
  
##  <a name="setmodifiedflag"></a>COlePropertyPage::SetModifiedFlag  
 속성 페이지 수정 되었는지 여부를 나타냅니다.  
  
```  
void SetModifiedFlag(BOOL bModified = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 `bModified`  
 속성 페이지의 수정 된 플래그에 대 한 새 값을 지정합니다.  
  
##  <a name="setpagename"></a>COlePropertyPage::SetPageName  
 일반적으로 속성 프레임이 페이지의 탭에 표시 하는 속성 페이지의 이름을 설정 합니다.  
  
```  
void SetPageName(LPCTSTR lpszPageName);
```  
  
### <a name="parameters"></a>매개 변수  
 *lpszPageName*  
 속성 페이지의 이름을 포함 하는 문자열에 대 한 포인터입니다.  
  
## <a name="see-also"></a>참고 항목  
 [MFC 샘플 CIRC3](../../visual-cpp-samples.md)   
 [MFC 샘플 TESTHELP](../../visual-cpp-samples.md)   
 [CDialog 클래스](../../mfc/reference/cdialog-class.md)   
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [CDialog 클래스](../../mfc/reference/cdialog-class.md)
