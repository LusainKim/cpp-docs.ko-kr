---
title: "CPane 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CPane
- AFXPANE/CPane
- AFXPANE/CPane::AdjustSizeImmediate
- AFXPANE/CPane::AllocElements
- AFXPANE/CPane::AllowShowOnPaneMenu
- AFXPANE/CPane::CalcAvailableSize
- AFXPANE/CPane::CalcInsideRect
- AFXPANE/CPane::CalcRecentDockedRect
- AFXPANE/CPane::CalcSize
- AFXPANE/CPane::CanBeDocked
- AFXPANE/CPane::CanBeTabbedDocument
- AFXPANE/CPane::ConvertToTabbedDocument
- AFXPANE/CPane::CopyState
- AFXPANE/CPane::Create
- AFXPANE/CPane::CreateDefaultMiniframe
- AFXPANE/CPane::CreateEx
- AFXPANE/CPane::DockByMouse
- AFXPANE/CPane::DockPane
- AFXPANE/CPane::DockPaneStandard
- AFXPANE/CPane::DockToFrameWindow
- AFXPANE/CPane::DoesAllowSiblingBars
- AFXPANE/CPane::FloatPane
- AFXPANE/CPane::GetAvailableExpandSize
- AFXPANE/CPane::GetAvailableStretchSize
- AFXPANE/CPane::GetBorders
- AFXPANE/CPane::GetClientHotSpot
- AFXPANE/CPane::GetDockSiteRow
- AFXPANE/CPane::GetExclusiveRowMode
- AFXPANE/CPane::GetHotSpot
- AFXPANE/CPane::GetMinSize
- AFXPANE/CPane::GetPaneName
- AFXPANE/CPane::GetVirtualRect
- AFXPANE/CPane::IsChangeState
- AFXPANE/CPane::IsDragMode
- AFXPANE/CPane::IsInFloatingMultiPaneFrameWnd
- AFXPANE/CPane::IsLeftOf
- AFXPANE/CPane::IsResizable
- AFXPANE/CPane::IsTabbed
- AFXPANE/CPane::LoadState
- AFXPANE/CPane::MoveByAlignment
- AFXPANE/CPane::MovePane
- AFXPANE/CPane::OnAfterChangeParent
- AFXPANE/CPane::OnBeforeChangeParent
- AFXPANE/CPane::OnPressCloseButton
- AFXPANE/CPane::OnShowControlBarMenu
- AFXPANE/CPane::RecalcLayout
- AFXPANE/CPane::SaveState
- AFXPANE/CPane::SetActiveInGroup
- AFXPANE/CPane::SetBorders
- AFXPANE/CPane::SetClientHotSpot
- AFXPANE/CPane::SetDockState
- AFXPANE/CPane::SetExclusiveRowMode
- AFXPANE/CPane::SetMiniFrameRTC
- AFXPANE/CPane::SetMinSize
- AFXPANE/CPane::SetVirtualRect
- AFXPANE/CPane::StretchPaneDeferWndPos
- AFXPANE/CPane::ToggleAutoHide
- AFXPANE/CPane::UndockPane
- AFXPANE/CPane::UpdateVirtualRect
- AFXPANE/CPane::OnAfterDock
- AFXPANE/CPane::OnAfterFloat
- AFXPANE/CPane::OnBeforeDock
- AFXPANE/CPane::OnBeforeFloat
- AFXPANE/CPane::m_bHandleMinSize
- AFXPANE/CPane::m_recentDockInfo
dev_langs: C++
helpviewer_keywords:
- CPane [MFC], AdjustSizeImmediate
- CPane [MFC], AllocElements
- CPane [MFC], AllowShowOnPaneMenu
- CPane [MFC], CalcAvailableSize
- CPane [MFC], CalcInsideRect
- CPane [MFC], CalcRecentDockedRect
- CPane [MFC], CalcSize
- CPane [MFC], CanBeDocked
- CPane [MFC], CanBeTabbedDocument
- CPane [MFC], ConvertToTabbedDocument
- CPane [MFC], CopyState
- CPane [MFC], Create
- CPane [MFC], CreateDefaultMiniframe
- CPane [MFC], CreateEx
- CPane [MFC], DockByMouse
- CPane [MFC], DockPane
- CPane [MFC], DockPaneStandard
- CPane [MFC], DockToFrameWindow
- CPane [MFC], DoesAllowSiblingBars
- CPane [MFC], FloatPane
- CPane [MFC], GetAvailableExpandSize
- CPane [MFC], GetAvailableStretchSize
- CPane [MFC], GetBorders
- CPane [MFC], GetClientHotSpot
- CPane [MFC], GetDockSiteRow
- CPane [MFC], GetExclusiveRowMode
- CPane [MFC], GetHotSpot
- CPane [MFC], GetMinSize
- CPane [MFC], GetPaneName
- CPane [MFC], GetVirtualRect
- CPane [MFC], IsChangeState
- CPane [MFC], IsDragMode
- CPane [MFC], IsInFloatingMultiPaneFrameWnd
- CPane [MFC], IsLeftOf
- CPane [MFC], IsResizable
- CPane [MFC], IsTabbed
- CPane [MFC], LoadState
- CPane [MFC], MoveByAlignment
- CPane [MFC], MovePane
- CPane [MFC], OnAfterChangeParent
- CPane [MFC], OnBeforeChangeParent
- CPane [MFC], OnPressCloseButton
- CPane [MFC], OnShowControlBarMenu
- CPane [MFC], OnShowControlBarMenu
- CPane [MFC], RecalcLayout
- CPane [MFC], SaveState
- CPane [MFC], SetActiveInGroup
- CPane [MFC], SetBorders
- CPane [MFC], SetClientHotSpot
- CPane [MFC], SetDockState
- CPane [MFC], SetExclusiveRowMode
- CPane [MFC], SetMiniFrameRTC
- CPane [MFC], SetMinSize
- CPane [MFC], SetVirtualRect
- CPane [MFC], StretchPaneDeferWndPos
- CPane [MFC], ToggleAutoHide
- CPane [MFC], UndockPane
- CPane [MFC], UpdateVirtualRect
- CPane [MFC], OnAfterDock
- CPane [MFC], OnAfterFloat
- CPane [MFC], OnBeforeDock
- CPane [MFC], OnBeforeFloat
- CPane [MFC], m_bHandleMinSize
- CPane [MFC], m_recentDockInfo
ms.assetid: 5c651a64-3c79-4d94-9676-45f6402a6bc5
caps.latest.revision: "30"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 56d3d30907a5001b95cdd55bd17fc86eaf5c078f
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cpane-class"></a>CPane Class
`CPane` 는의 향상 된 클래스는 [CControlBar 클래스](../../mfc/reference/ccontrolbar-class.md)합니다. 기존 MFC 프로젝트를 업그레이드 하는 경우 모든 항목을 바꿉니다 `CControlBar` 와 `CPane`합니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CPane : public CBasePane  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|`CPane::~CPane`|소멸자|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CPane::AdjustSizeImmediate](#adjustsizeimmediate)|즉시는 창 레이아웃을 다시 계산 됩니다.|  
|[CPane::AllocElements](#allocelements)|내부 사용에 대 한 저장소를 할당 합니다.|  
|[CPane::AllowShowOnPaneMenu](#allowshowonpanemenu)|창에서 응용 프로그램 창의 런타임에 생성 된 목록에 나열 되는지 지정 합니다.|  
|[CPane::CalcAvailableSize](#calcavailablesize)|지정된 된 사각형 및 현재 창 사각형 크기 차이 계산 합니다.|  
|[CPane::CalcInsideRect](#calcinsiderect)|내부 계산 사각형의 테두리 및 위치 조정 막대를 고려 하는 창입니다.|  
|[CPane::CalcRecentDockedRect](#calcrecentdockedrect)|최근에 도킹 된 사각형을 계산합니다.|  
|[CPane::CalcSize](#calcsize)|창의 크기를 계산합니다.|  
|[CPane::CanBeDocked](#canbedocked)|창에서 지정 된 기본 창에서 도킹 될 수 있는지 여부를 결정 합니다.|  
|[CPane::CanBeTabbedDocument](#canbetabbeddocument)|창에서 탭 된 문서로 변환할 수 있는지 여부를 결정 합니다.|  
|[CPane::ConvertToTabbedDocument](#converttotabbeddocument)|도킹 가능한 창을 탭 된 문서로 변환합니다.|  
|[CPane::CopyState](#copystate)|창의 상태를 복사합니다. (재정의 [CBasePane::CopyState](../../mfc/reference/cbasepane-class.md#copystate).)|  
|[Cpane:: Create](#create)|컨트롤 막대를 만들고 연결 하는 `CPane` 개체입니다.|  
|[Cpane:: Createdefaultminiframe](#createdefaultminiframe)|부동 창에 대 한 미니 프레임 창을 만듭니다.|  
|[Cpane:: Createex](#createex)|컨트롤 막대를 만들고 연결 하는 `CPane` 개체입니다.|  
|`CPane::CreateObject`|프레임워크에서 이 클래스 형식의 동적 인스턴스를 만드는 데 사용합니다.|  
|[CPane::DockByMouse](#dockbymouse)|메서드를 도킹 마우스를 사용 하 여 창을 도킹 합니다.|  
|[CPane::DockPane](#dockpane)|부동 창의 기본 창으로 도킹합니다.|  
|[CPane::DockPaneStandard](#dockpanestandard)|개요 (표준) 도킹을 사용 하 여 창을 도킹 합니다.|  
|[CPane::DockToFrameWindow](#docktoframewindow)|도킹 가능한 창 프레임에 창을 도킹합니다. (`CBasePane::DockToFrameWindow`를 재정의합니다.)|  
|[CPane::DoesAllowSiblingBars](#doesallowsiblingbars)|현재 창 도킹 됨 같은 행에 다른 창에 도킹할 수 있는지 여부를 나타냅니다.|  
|[CPane::FloatPane](#floatpane)|창을 부동 합니다.|  
|[CPane::GetAvailableExpandSize](#getavailableexpandsize)|창에서 확장할 수 있는 픽셀 단위로 크기를 반환 합니다.|  
|[CPane::GetAvailableStretchSize](#getavailablestretchsize)|창 축소할 수를 픽셀 단위로 시도 하는 양을 반환 합니다.|  
|[CPane::GetBorders](#getborders)|창의 테두리의 두께 반환 합니다.|  
|[CPane::GetClientHotSpot](#getclienthotspot)|반환 된 *핫 스폿* 는 창에 대 한 합니다.|  
|[CPane::GetDockSiteRow](#getdocksiterow)|창 도킹 도킹 행을 반환 합니다.|  
|[CPane::GetExclusiveRowMode](#getexclusiverowmode)|창 배타 행 모드 인지 여부를 결정 합니다.|  
|[CPane::GetHotSpot](#gethotspot)|내부에 저장 된 핫 스폿 반환 `CMFCDragFrameImpl` 개체입니다.|  
|[CPane::GetMinSize](#getminsize)|창 크기에 허용 되는 최소값을 검색 합니다.|  
|[CPane::GetPaneName](#getpanename)|창에 대 한 title을 검색합니다.|  
|`CPane::GetResizeStep`|내부적으로 사용 합니다.|  
|`CPane::GetThisClass`|에 대 한 포인터를 가져오는 데 프레임 워크에서는 [CRuntimeClass](../../mfc/reference/cruntimeclass-structure.md) 이 클래스 형식과 연결 된 개체입니다.|  
|[CPane::GetVirtualRect](#getvirtualrect)|검색 된 *가상 사각형* 창.|  
|[CPane::IsChangeState](#ischangestate)|이 메서드 다른 창, 도킹 행 및 미니 프레임 창을 기준으로 창 위치를 분석 하 고 적절 한 창에서 이동 하는 대로 `AFX_CS_STATUS` 값입니다.|  
|[CPane::IsDragMode](#isdragmode)|창에서 끌어온 있는지 여부를 지정 합니다.|  
|[CPane::IsInFloatingMultiPaneFrameWnd](#isinfloatingmultipaneframewnd)|다중 창 프레임 창에는 창이 되는지 여부를 지정 합니다. (`CBasePane::IsInFloatingMultiPaneFrameWnd`를 재정의합니다.)|  
|[CPane::IsLeftOf](#isleftof)|창 왼쪽의 (또는 위에)를 결정 합니다. 지정된 된 사각형입니다.|  
|[CPane::IsResizable](#isresizable)|창 크기를 조정할 수 있는지 여부를 결정 합니다. (재정의 [cbasepane:: Isresizable](../../mfc/reference/cbasepane-class.md#isresizable).)|  
|[CPane::IsTabbed](#istabbed)|창에서 탭 컨트롤의 탭된 창에 삽입 된 있는지 여부를 결정 합니다. (재정의 [CBasePane::IsTabbed](../../mfc/reference/cbasepane-class.md#istabbed).)|  
|[CPane::LoadState](#loadstate)|레지스트리에서 창의 상태를 로드 합니다. (재정의 [CBasePane::LoadState](../../mfc/reference/cbasepane-class.md#loadstate).)|  
|[CPane::MoveByAlignment](#movebyalignment)|지정 된 크기는 창과 가상 사각형을 이동합니다.|  
|[CPane::MovePane](#movepane)|창이 지정된 된 사각형으로 이동 합니다.|  
|[CPane::OnAfterChangeParent](#onafterchangeparent)|부모 창의 변경 될 때 프레임 워크에서 호출 됩니다.|  
|[CPane::OnBeforeChangeParent](#onbeforechangeparent)|부모 창의 변경 되려고 할 때 프레임 워크에서 호출 됩니다.|  
|[CPane::OnPressCloseButton](#onpressclosebutton)|창에 대 한 캡션에서 닫기 단추를 선택 하면 프레임 워크에서 호출 됩니다.|  
|`CPane::OnProcessDblClk`|내부적으로 사용 합니다.|  
|[Cpane:: Onshowcontrolbarmenu](#onshowcontrolbarmenu)|특수 창 메뉴를 표시하려고 할 때 프레임워크에서 호출됩니다.|  
|[Cpane:: Onshowcontrolbarmenu](#onshowcontrolbarmenu)|특수 창 메뉴를 표시하려고 할 때 프레임워크에서 호출됩니다.|  
|`CPane::PrepareToDock`|내부적으로 사용 합니다.|  
|[Cpane:: Recalclayout](#recalclayout)|창에 대 한 레이아웃 정보를 다시 계산합니다. (재정의 [CBasePane::RecalcLayout](../../mfc/reference/cbasepane-class.md#recalclayout).)|  
|[CPane::SaveState](#savestate)|레지스트리에 창의 상태를 저장합니다. (재정의 [CBasePane::SaveState](../../mfc/reference/cbasepane-class.md#savestate).)|  
|[Cpane:: Setactiveingroup](#setactiveingroup)|창에 활성으로 플래그 지정합니다.|  
|[CPane::SetBorders](#setborders)|창의 테두리 값을 설정합니다.|  
|[CPane::SetClientHotSpot](#setclienthotspot)|창에 대 한 핫 스폿 설정합니다.|  
|[CPane::SetDockState](#setdockstate)|도킹 된 창에 대 한 상태 정보를 복원 합니다.|  
|[CPane::SetExclusiveRowMode](#setexclusiverowmode)|배타 행 모드를 해제 하거나 사용 합니다.|  
|[CPane::SetMiniFrameRTC](#setminiframertc)|기본 미니 프레임 창에 대 한 런타임 클래스 정보를 설정합니다.|  
|[CPane::SetMinSize](#setminsize)|창 크기에 허용 되는 최소값을 설정 합니다.|  
|[CPane::SetVirtualRect](#setvirtualrect)|설정의 *가상 사각형* 창.|  
|[CPane::StretchPaneDeferWndPos](#stretchpanedeferwndpos)|가로 또는 세로로 도킹 스타일에 따라 창을 늘어납니다.|  
|[CPane::ToggleAutoHide](#toggleautohide)|자동 숨기기 모드를 설정/해제 합니다.|  
|[CPane::UndockPane](#undockpane)|도킹 사이트, 기본 슬라이더 또는 현재 도킹 되는 미니 프레임 창에서 창에서를 제거 합니다. (재정의 [CBasePane::UndockPane](../../mfc/reference/cbasepane-class.md#undockpane).)|  
|[CPane::UpdateVirtualRect](#updatevirtualrect)|가상 사각형을 업데이트합니다.|  
  
### <a name="protected-methods"></a>보호된 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CPane::OnAfterDock](#onafterdock)|창을 도킹 된 프레임 워크에서 호출 됩니다.|  
|[CPane::OnAfterFloat](#onafterfloat)|창을 부동화 된 프레임 워크에서 호출 됩니다.|  
|[CPane::OnBeforeDock](#onbeforedock)|창에서 도킹 될 되려고 할 때 프레임 워크에서 호출 됩니다.|  
|[CPane::OnBeforeFloat](#onbeforefloat)|창을 놓을지 되려고 할 때 프레임 워크에서 호출 됩니다.|  
  
### <a name="data-members"></a>데이터 멤버  
  
|name|설명|  
|----------|-----------------|  
|[CPane::m_bHandleMinSize](#m_bhandleminsize)|창에 대 한 최소 크기의 일관 된 처리할 수 있습니다.|  
|[M_recentdockinfo](#m_recentdockinfo)|최근 도킹 정보가 포함 되어 있습니다.|  
  
## <a name="remarks"></a>설명  
 일반적으로 `CPane` 개체는 직접 인스턴스화되지 않습니다. 개체를 파생 된 도킹 기능이 있는 창, 필요한 경우 [CDockablePane](../../mfc/reference/cdockablepane-class.md)합니다. 도구 모음 기능이 필요한 경우에서 개체를 파생 [CMFCToolBar](../../mfc/reference/cmfctoolbar-class.md)합니다.  
  
 클래스를 파생 시키는 경우 `CPane`에서 도킹 될 수는 [CDockSite](../../mfc/reference/cdocksite-class.md) 에 이동식 될 수 있습니다 및는 [CPaneFrameWnd](../../mfc/reference/cpaneframewnd-class.md)합니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CBasePane](../../mfc/reference/cbasepane-class.md)  
  
 [CPane](../../mfc/reference/cpane-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxPane.h  
  
##  <a name="adjustsizeimmediate"></a>CPane::AdjustSizeImmediate  
 즉시는 창 레이아웃을 다시 계산 됩니다.  
  
```  
virtual void AdjustSizeImmediate(BOOL bRecalcLayout = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bRecalcLayout`  
 `TRUE`자동으로; 창 레이아웃을 다시 계산 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 창 레이아웃을 동적으로 변경 하는 경우이 메서드를 호출 합니다. 예를 들어 다음 숨기 거 나 도구 모음 단추를 표시 하는 경우이 메서드를 호출 하는 것이 좋습니다.  
  
##  <a name="allocelements"></a>CPane::AllocElements  
 내부 사용에 대 한 저장소를 할당 합니다.  
  
```  
BOOL AllocElements(
    int nElements,  
    int cbElement);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nElements`  
 저장소를 할당 하는 요소 수입니다.  
  
 [in] `cbElement`  
 요소를 바이트 단위로 크기입니다.  
  
### <a name="return-value"></a>반환 값  
 `FALSE`메모리 할당에 실패 하면 그렇지 않으면 `TRUE`합니다.  
  
##  <a name="allowshowonpanemenu"></a>CPane::AllowShowOnPaneMenu  
 창에서 응용 프로그램 창의 런타임에 생성 된 목록에 나열 되는지 지정 합니다.  
  
```  
virtual BOOL AllowShowOnPaneMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`목록에는 창이 표시 되어 그렇지 않으면 `FALSE`합니다. 기본 구현에서는 항상 반환 `TRUE`합니다.  
  
### <a name="remarks"></a>설명  
 응용 프로그램 마법사에서 생성 된 응용 프로그램에 포함 된 창에 나열 된 메뉴 옵션을 포함 합니다. 이 메서드는 창 목록에 표시 되는지 여부를 결정 합니다.  
  
##  <a name="calcavailablesize"></a>CPane::CalcAvailableSize  
 지정된 된 사각형 및 현재 창 사각형 크기 차이 계산 합니다.  
  
```  
virtual CSize CalcAvailableSize(CRect rectRequired);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rectRequired`  
 필요한 사각형입니다.  
  
### <a name="return-value"></a>반환 값  
 너비와 높이 간 차이 `rectRequired` 및 현재 창 사각형입니다.  
  
##  <a name="calcinsiderect"></a>CPane::CalcInsideRect  
 내부 계산 사각형의 테두리 및 위치 조정 막대를 포함 하는 창입니다.  
  
```  
void CalcInsideRect(
    CRect& rect,  
    BOOL bHorz) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [out] `rect`  
 크기와 창의 클라이언트 영역 오프셋을 포함합니다.  
  
 [in] `bHorz`  
 `TRUE`창이 않으면 방향이 가로로; 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 창에 대 한 레이아웃을 다시 계산 해야 할 때 프레임 워크에서 호출 됩니다. `rect` 매개 변수 크기와 창의 클라이언트 영역의 오프셋으로 채워집니다. 테두리 및 위치 조정 막대 포함 합니다.  
  
##  <a name="calcrecentdockedrect"></a>CPane::CalcRecentDockedRect  
 최근에 도킹 된 사각형을 계산합니다.  
  
```  
void CalcRecentDockedRect();
```  
  
### <a name="remarks"></a>설명  
 이 메서드는 업데이트 [M_recentdockinfo](#m_recentdockinfo)합니다.  
  
##  <a name="calcsize"></a>CPane::CalcSize  
 창의 크기를 계산합니다.  
  
```  
virtual CSize CalcSize(BOOL bVertDock);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bVertDock`  
 `TRUE`창에서 세로로 도킹 되는 경우 `FALSE` 그렇지 않은 경우.  
  
### <a name="return-value"></a>반환 값  
 크기를 반환 하는이 메서드의 기본 구현 (0, 0).  
  
### <a name="remarks"></a>설명  
 파생된 클래스는이 메서드를 재정의 해야 합니다.  
  
##  <a name="canbedocked"></a>CPane::CanBeDocked  
 창에서 지정 된 기본 창에 도킹할 수 있는 경우를 결정 합니다.  
  
```  
virtual BOOL CanBeDocked(CBasePane* pDockBar) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDockBar`  
 이 창의 도킹 창을 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`지정 된 도킹 창을;에서이 창을 도킹할 수 있는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 일반적으로 창 지정된 도킹 창에 도킹 될 수 있는지 여부를 결정 하는 프레임 워크에서 호출 됩니다. 인지 여부를 확인 창에서 도킹 될 수 있습니다, 메서드는 창의 현재 도킹 맞춤을 사용할 수 있습니다.  
  
 호출 하 여 프레임 창의 다양 한 측면에 도킹 사용 하도록 설정 하면 [CBasePane::EnableDocking](../../mfc/reference/cbasepane-class.md#enabledocking)합니다.  
  
##  <a name="canbetabbeddocument"></a>CPane::CanBeTabbedDocument  
 창에서 탭 된 문서로 변환할 수 있는지 확인 합니다.  
  
```  
virtual BOOL CanBeTabbedDocument() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창에서 탭 된 문서로; 변환할 수 있는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 파생된 클래스에서이 메서드를 재정의 하 고 반환 `FALSE` 창을 탭 된 문서로 변환 되 고 하지 못하도록 하려는 경우. 탭된 문서 창 위치 메뉴에 표시 되지 않습니다.  
  
##  <a name="converttotabbeddocument"></a>CPane::ConvertToTabbedDocument  
 도킹 가능한 창을 탭 된 문서로 변환합니다.  
  
```  
virtual void ConvertToTabbedDocument(BOOL bActiveTabOnly = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bActiveTabOnly`  
 사용 되지 않습니다 `CPane::ConvertToTabbedDocument`합니다.  
  
### <a name="remarks"></a>설명  
 탭된 문서로 도킹 가능한 창만 변환할 수 있습니다. 자세한 내용은 참조 [CDockablePane::ConvertToTabbedDocument](../../mfc/reference/cdockablepane-class.md#converttotabbeddocument)합니다.  
  
##  <a name="copystate"></a>CPane::CopyState  
 창의 상태를 복사합니다.  
  
```  
virtual void CopyState(CPane* pOrgBar);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pOrgBar`  
 창에 대 한 포인터입니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 상태를 복사 `pOrgBar` 현재 창에 있습니다.  
  
##  <a name="create"></a>Cpane:: Create  
 컨트롤 막대를 만들고 연결 하는 [CPane](../../mfc/reference/cpane-class.md) 개체입니다.  
  
```  
virtual BOOL Create(
    LPCTSTR lpszClassName,  
    DWORD dwStyle,  
    const RECT& rect,  
    CWnd* pParentWnd,  
    UINT nID,  
    DWORD dwControlBarStyle = AFX_DEFAULT_PANE_STYLE,  
    CCreateContext* pContext = NULL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszClassName`  
 Windows 클래스의 이름을 지정합니다.  
  
 [in] `dwStyle`  
 창 스타일 특성을 지정합니다. 자세한 내용은 참조 [창 스타일](../../mfc/reference/styles-used-by-mfc.md#window-styles)합니다.  
  
 [in] `rect`  
 초기 크기와 위치를 지정 된 `pParentWnd` 창의 클라이언트 좌표에서.  
  
 [in] [out]`pParentWnd`  
 이 창의 부모 창을 지정합니다.  
  
 [in] `nID`  
 창 ID를 지정합니다.  
  
 [in] `dwControlBarStyle`  
 창 스타일을 지정합니다. 자세한 내용은 참조 [cbasepane:: Createex](../../mfc/reference/cbasepane-class.md#createex)합니다.  
  
 [in] [out]`pContext`  
 창 만들기 컨텍스트를 지정합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창에서 성공적으로 만들어진 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 Windows 창을 만들고에 연결 된 `CPane` 개체입니다.  
  
 명시적으로 초기화 되지 경우 [M_recentdockinfo](#m_recentdockinfo) 호출 하기 전에 `Create`, 매개 변수 `rect` 부동 또는 도킹 된 창 때 사각형으로 사용 됩니다.  
  
##  <a name="createdefaultminiframe"></a>Cpane:: Createdefaultminiframe  
 부동 창에 대 한 미니 프레임 창을 만듭니다.  
  
```  
virtual CPaneFrameWnd* CreateDefaultMiniframe(CRect rectInitial);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rectInitial`  
 초기 크기와 화면 좌표에 미니 프레임 창 만들기의 위치를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 새로 만든된 미니 프레임 창입니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 창을 움직이는 경우 미니 프레임 창을 만들기 위해 프레임 워크에서 호출 됩니다. 미니 프레임 창을 유형일 수 [CPaneFrameWnd](../../mfc/reference/cpaneframewnd-class.md) 또는 형식의 [CMultiPaneFrameWnd](../../mfc/reference/cmultipaneframewnd-class.md)합니다. 창에 다중 미니 프레임 창을 만들는 `AFX_CBRS_FLOAT_MULTI` 스타일입니다.  
  
 미니 프레임 창에 대 한 런타임 클래스 정보에 저장 됩니다는 `CPane::m_pMiniFrameRTC` 멤버입니다. 사용자 지정 된 미니 프레임 창 만들기로 결정 하는 경우이 멤버를 설정 하는 파생된 클래스를 사용할 수 있습니다.  
  
##  <a name="createex"></a>Cpane:: Createex  
 컨트롤 막대를 만들고 연결 하는 [CPane](../../mfc/reference/cpane-class.md) 개체입니다.  
  
```  
virtual BOOL CreateEx(
    DWORD dwStyleEx,  
    LPCTSTR lpszClassName,  
    DWORD dwStyle,  
    const RECT& rect,  
    CWnd* pParentWnd,  
    UINT nID,  
    DWORD dwControlBarStyle = AFX_DEFAULT_PANE_STYLE,  
    CCreateContext* pContext = NULL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `dwStyleEx`  
 확장된 창 스타일 특성을 지정합니다. 자세한 내용은 참조 [확장 창 스타일](../../mfc/reference/styles-used-by-mfc.md#extended-window-styles)합니다.  
  
 [in] `lpszClassName`  
 Windows 클래스의 이름을 지정합니다.  
  
 [in] `dwStyle`  
 창 스타일 특성을 지정합니다. 자세한 내용은 참조 [창 스타일](../../mfc/reference/styles-used-by-mfc.md#window-styles)합니다.  
  
 [in] `rect`  
 초기 크기와 위치를 지정 된 `pParentWnd` 창의 클라이언트 좌표에서.  
  
 [in] [out]`pParentWnd`  
 이 창의 부모 창을 지정합니다.  
  
 [in] `nID`  
 창 ID를 지정합니다.  
  
 [in] `dwControlBarStyle`  
 창 스타일을 지정합니다. 자세한 내용은 참조 [cbasepane:: Createex](../../mfc/reference/cbasepane-class.md#createex)합니다.  
  
 [in] [out]`pContext`  
 창에 대 한 create 컨텍스트를 지정합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창에서 성공적으로 만들어진 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 Windows 창을 만들고에 연결 된 `CPane` 개체입니다.  
  
 명시적으로 초기화 되지 경우 [M_recentdockinfo](#m_recentdockinfo) 호출 하기 전에 `CreateEx`, 매개 변수 `rect` 부동 또는 도킹 된 창 때 사각형으로 사용 됩니다.  
  
##  <a name="dockbymouse"></a>CPane::DockByMouse  
 마우스를 사용 하 여 창을 도킹 합니다.  
  
```  
virtual BOOL DockByMouse(CBasePane* pDockBar);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDockBar`  
 기본 창이이 창의 도킹을 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창에서 성공적으로; 도킹 된 경우 그렇지 않으면 `FALSE`합니다.  
  
##  <a name="dockpane"></a>CPane::DockPane  
 부동 창의 기본 창으로 도킹합니다.  
  
```  
virtual BOOL DockPane(
    CBasePane* pDockBar,  
    LPCRECT lpRect,  
    AFX_DOCK_METHOD dockMethod);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] [out]`pDockBar`  
 기본 창에이 창을 도킹 하려면를 지정 합니다.  
  
 [in] `lpRect`  
 이 창을 도킹할 수 인 기본 창에 사각형을 지정 합니다.  
  
 [in] `dockMethod`  
 도킹 사용할 메서드를 지정 합니다. 사용 가능한 옵션은 다음과 같습니다.  
  
|옵션|설명|  
|------------|-----------------|  
|`DM_UNKNOWN`|프레임 워크 도킹 메서드를 알 수 없는 경우이 옵션을 사용 합니다. 창 부동 가장 최근 위치를 저장 하지 않습니다. 또한 프로그래밍 방식으로 최근 부동 위치를 저장 하지 않은 경우는 창을 도킹 하려면이 옵션을 사용할 수 있습니다.|  
|`DM_MOUSE`|내부적으로 사용 합니다.|  
|`DM_DBL_CLICK`|위치 조정 막대를 두 번 클릭할 때이 옵션은 사용 됩니다. 가장 최근의 도킹 위치에는 창 위치가 변경 합니다. 창에서이 두 번 클릭 하 여 도킹 되지 않았는지, 창에서 가장 최근의 부동 위치에 위치가 변경 합니다.|  
|`DM_SHOW`|프로그래밍 방식으로 창을 도킹 하려면이 옵션을 사용할 수 있습니다. 창에서 가장 최근 부동 위치를 저장합니다.|  
|`DM_RECT`|창이 도킹 되어 있는 지정 된 지역에 `lpRect`합니다.|  
|`DM_STANDARD`|이 옵션을 사용 하면 이동 하는 동안 창 프레임 워크에 개요 프레임으로 그립니다.|  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창에서 성공적으로; 도킹 된 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드를 지정 된 기본 창 창을 도킹 된 `pDockBar` 매개 변수입니다. 호출 하 여 도킹를 먼저 활성화 해야 [CBasePane::EnableDocking](../../mfc/reference/cbasepane-class.md#enabledocking)합니다.  
  
##  <a name="dockpanestandard"></a>CPane::DockPaneStandard  
 개요 (표준) 도킹을 사용 하 여 창을 도킹 합니다.  
  
```  
virtual CPane* DockPaneStandard(BOOL& bWasDocked);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bWasDocked`  
 `TRUE`창이 도킹 있는 경우가 성공적으로; 그렇지 않으면 `FALSE`합니다.  
  
### <a name="return-value"></a>반환 값  
 이 메서드는 항상 반환 된 `this` 포인터입니다.  
  
### <a name="remarks"></a>설명  
 파생 된 창에 대해서만이 메서드는는 [CDockablePane 클래스](../../mfc/reference/cdockablepane-class.md)합니다. 자세한 내용은 참조 [CDockablePane::DockPaneStandard](../../mfc/reference/cdockablepane-class.md#dockpanestandard)합니다.  
  
##  <a name="docktoframewindow"></a>CPane::DockToFrameWindow  
 도킹 가능한 창 프레임에 창을 도킹합니다.  
  
```  
virtual BOOL DockToFrameWindow(
    DWORD dwAlignment,  
    LPCRECT lpRect = NULL,  
    DWORD dwDockFlags = DT_DOCK_LAST,  
    CBasePane* pRelativeBar = NULL,  
    int nRelativeIndex = -1,  
    BOOL bOuterEdge = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `dwAlignment`  
 부모 프레임에 창을 도킹 하려면 원하는 부분입니다.  
  
 [in] `lpRect`  
 지정 된 크기입니다.  
  
 [in] `dwDockFlags`  
 무시됩니다.  
  
 [in] `pRelativeBar`  
 무시됩니다.  
  
 [in] `nRelativeIndex`  
 무시됩니다.  
  
 [in] `bOuterEdge`  
 경우 `TRUE` 로 지정 되는 쪽에서 다른 도킹 가능한 창 고 `dwAlignment`, 창이 도킹 되어 있는 다른 창 외부 부모 프레임 가장자리에 더 가깝기 때문입니다. 경우 `FALSE`는 창은 클라이언트 영역의 가운데에 곧 제공 될 도킹 됩니다.  
  
### <a name="return-value"></a>반환 값  
 `FALSE`경우 창 구분선 ( [CPaneDivider 클래스](../../mfc/reference/cpanedivider-class.md)) 그렇지 않으면 안 `TRUE`합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="doesallowsiblingbars"></a>CPane::DoesAllowSiblingBars  
 현재 창 도킹 됨 같은 행에 다른 창에 도킹할 수 있는지 여부를 나타냅니다.  
  
```  
virtual BOOL DoesAllowSiblingBars() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`이 창 자체;과 같은 행에 다른 창으로 도킹 한 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 호출 하 여이 동작을 해제 하거나 설정할 수 있습니다 [CPane::SetExclusiveRowMode](#setexclusiverowmode)합니다.  
  
 기본적으로 도구 모음 사용 하지 않도록 설정 하는 배타 행 모드 있고 메뉴 모음에 배타 행 모드를 사용 합니다.  
  
##  <a name="floatpane"></a>CPane::FloatPane  
 창을 부동 합니다.  
  
```  
virtual BOOL FloatPane(
    CRect rectFloat,  
    AFX_DOCK_METHOD dockMethod = DM_UNKNOWN,  
    bool bShow = true);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rectFloat`  
 부동 하는 경우의 창 위치를 화면 좌표로 위치를 지정 합니다.  
  
 [in] `dockMethod`  
 창 움직이는 때 사용할 도킹 방법을 지정 합니다. 가능한 값 목록은 참조 [CPane::DockPane](#dockpane)합니다.  
  
 [in] `bShow`  
 `TRUE`움직이는; 때 창을 표시 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창이 성공적으로 움직이는 또는 때문에 창을 부동 수 없는 경우 [CBasePane::CanFloat](../../mfc/reference/cbasepane-class.md#canfloat) 반환 `FALSE`, 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 창에 지정 된 위치에 배치 하려면이 메서드를 호출 하는 `rectFloat` 매개 변수입니다. 이 메서드는 창에 대 한 부모 미니 프레임 창을 자동으로 만듭니다.  
  
##  <a name="getavailableexpandsize"></a>CPane::GetAvailableExpandSize  
 창에서 확장할 수 있는 픽셀 단위로 크기를 반환 합니다.  
  
```  
virtual int GetAvailableExpandSize() const;  
```  
  
### <a name="return-value"></a>반환 값  
 반환 값은 사용 가능한 너비; 창에서 가로로 도킹 되어, 하는 경우 그렇지 않으면 반환 값은 사용 가능한 높이입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getavailablestretchsize"></a>CPane::GetAvailableStretchSize  
 창 축소할 수를 픽셀 단위로 시도 하는 양을 반환 합니다.  
  
```  
virtual int GetAvailableStretchSize() const;  
```  
  
### <a name="return-value"></a>반환 값  
 픽셀의 창 축소할 수 있는 양입니다. 창이 도킹 되어 있는 가로 방향으로,이 수는 사용 가능한 너비입니다. 그렇지 않으면 사용할 수 있는 높이입니다.  
  
### <a name="remarks"></a>설명  
 스트레치 사용 가능한 크기는 최소 크기는 창에 대 한 허용을 빼서 계산 ( [CPane::GetMinSize](#getminsize))에서 현재 크기 ( [CWnd::GetWindowRect](../../mfc/reference/cwnd-class.md#getwindowrect)).  
  
##  <a name="getborders"></a>CPane::GetBorders  
 창의 테두리의 두께 반환 합니다.  
  
```  
CRect GetBorders() const;  
```  
  
### <a name="return-value"></a>반환 값  
 A [CRect](../../atl-mfc-shared/reference/crect-class.md) 픽셀, 창의 각 면의에서 현재 너비를 포함 하는 개체입니다. 예를 들어 값은 `left` 의 멤버는 `CRect` 개체 왼쪽된 테두리의 너비입니다.  
  
### <a name="remarks"></a>설명  
 테두리의 크기를 설정 하려면 호출 [CPane::SetBorders](#setborders)합니다.  
  
##  <a name="getclienthotspot"></a>CPane::GetClientHotSpot  
 반환 된 *핫 스폿* 는 창에 대 한 합니다.  
  
```  
CPoint GetClientHotSpot() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
 *핫 스폿* 는 사용자가 선택한 창을 이동 하려면 보유 하는 창에서 점으로 합니다. 핫 스폿은 창이 도킹된 위치에서 이동할 때 부드러운 애니메이션에 사용 됩니다.  
  
##  <a name="getdocksiterow"></a>CPane::GetDockSiteRow  
 도킹 행을 반환 ( [CDockingPanesRow 클래스](../../mfc/reference/cdockingpanesrow-class.md))에 창이 도킹 되어 있습니다.  
  
```  
CDockingPanesRow* GetDockSiteRow() const;  
```  
  
### <a name="return-value"></a>반환 값  
 A `CDockingPanesRow`* 창에서 도킹 된 도킹 행을 가리키는 또는 `NULL` 창에서이 도킹 되지 않은 경우.  
  
##  <a name="getexclusiverowmode"></a>CPane::GetExclusiveRowMode  
 창 배타 행 모드에서 인지 여부를 확인 합니다.  
  
```  
virtual BOOL GetExclusiveRowMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`배타 행 모드에 표시 되는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 배타 행 모드에 대 한 자세한 내용은 참조 [CPane::SetExclusiveRowMode](#setexclusiverowmode)합니다.  
  
##  <a name="gethotspot"></a>CPane::GetHotSpot  
 내부에 저장 된 핫 스폿 반환 `CMFCDragFrameImpl` 개체입니다.  
  
```  
CPoint GetHotSpot() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
 `CPane` 클래스를 포함 한 `CMFCDragFrameImpl` 개체 `m_dragFrameImpl`, 즉 표준 도킹 모드의 창을 이동할 때 나타나는 사각형 그리기를 담당 합니다. 핫 스폿 사용자 창에서 이동할 때 현재 마우스 위치에 상대적인 사각형을 그리는 데 사용 됩니다.  
  
##  <a name="getminsize"></a>CPane::GetMinSize  
 창 크기에 허용 되는 최소값을 검색 합니다.  
  
```  
virtual void GetMinSize(CSize& size) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [out] `size`  
 A `CSize` 크기가 허용 되는 최소값으로 채워진 개체입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getpanename"></a>CPane::GetPaneName  
 창에 대 한 title을 검색합니다.  
  
```  
virtual void GetPaneName(CString& strName) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [out] `strName`  
 A `CString` 캡션 이름으로 채워지는 개체입니다.  
  
### <a name="remarks"></a>설명  
 창 제목 도킹 또는 부동 창이 되 면 캡션 영역에 표시 됩니다. 창에서 탭된 그룹의 일부 이면 제목 탭 영역에 표시 됩니다. 창 자동 숨기기 모드 이면 제목에 표시 됩니다는 `CMFCAutoHideButton`합니다.  
  
##  <a name="getvirtualrect"></a>CPane::GetVirtualRect  
 검색 된 *가상 사각형* 창.  
  
```  
void GetVirtualRect(CRect& rectVirtual) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [out] `rectVirtual`  
 A `CRect` 가상 사각형으로 채워진 개체입니다.  
  
### <a name="remarks"></a>설명  
 창을 이동 될 때 프레임 워크 가상 사각형에는 창의 원래 위치를 저장 합니다. 프레임 워크 창의 원래 위치로 복원 하려면 가상 사각형을 사용할 수 있습니다.  
  
 창을 프로그래밍 방식으로 이동 하려는 경우가 아니면 가상 사각형에 관련 된 메서드를 호출 하지 마십시오.  
  
##  <a name="ischangestate"></a>CPane::IsChangeState  
 이 메서드 다른 창, 도킹 행 및 미니 프레임 창을 기준으로 한 위치를 분석 하 고 적절 한 창에서 이동 하는 대로 `AFX_CS_STATUS` 값입니다.  
  
```  
virtual AFX_CS_STATUS IsChangeState(
    int nOffset,  
    CBasePane** ppTargetBar) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nOffset`  
 도킹 민감도 지정합니다. 내에서 이동 하는 창 예를 들어 `nOffset` 도킹 행에서 픽셀이 도킹 합니다.  
  
 [in] `ppTargetBar`  
 메서드가 반환 될 때 `ppTargetBar` 를 현재 창에서 도킹 함을, 개체에 대 한 포인터 또는 `NULL` 없는 도킹 발생 해야 할지 여부.  
  
### <a name="return-value"></a>반환 값  
 다음 중 하나 `AFX_CS_STATUS` 값:  
  
|값|설명|  
|-----------|-----------------|  
|`CS_NOTHING`|창에서 도킹 사이트 근처 않습니다. 프레임 워크 창을 도킹 하지 않습니다.|  
|`CS_DOCK_IMMEDIATELY`|도킹 사이트를 통해 표시 되 고 `DT_IMMEDIATE` 스타일을 사용 하도록 설정 합니다. 프레임 워크는 즉시 창을 도킹 합니다.|  
|`CS_DELAY_DOCK`|창은 주 프레임의 가장자리 또는 다른 도킹 창으로 도킹 사이트를 통해입니다. 프레임 워크는 사용자를 이동 하는 놓을 때 창을 도킹 합니다.|  
|`CS_DELAY_DOCK_TO_TAB`|창에서 탭된 창에서 도킹 창 도킹 사이트 끝났습니다. 다른 도킹 창의 캡션 또는 탭된 창 탭 영역 위로 창이 되 면 발생 합니다. 프레임 워크는 사용자를 이동 하는 놓을 때 창을 도킹 합니다.|  
  
##  <a name="isdragmode"></a>CPane::IsDragMode  
 창에서 이동 되 고 있는지 여부를 지정 합니다.  
  
```  
virtual BOOL IsDragMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창; 이동 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="isinfloatingmultipaneframewnd"></a>CPane::IsInFloatingMultiPaneFrameWnd  
 다중 창 프레임 창에는 창 인지를 지정 ( [CMultiPaneFrameWnd 클래스](../../mfc/reference/cmultipaneframewnd-class.md)).  
  
```  
virtual BOOL IsInFloatingMultiPaneFrameWnd() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`다중 창 프레임 창의 창이 되 면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 도킹 가능한 창만 다중 창 프레임 창에 배치할 수 있습니다. 따라서 `CPane::IsInFloatingMultiPaneFrameWnd` 항상 반환 `FALSE`합니다.  
  
##  <a name="isleftof"></a>CPane::IsLeftOf  
 창 왼쪽의 (또는 위에)를 결정 합니다. 지정된 된 사각형입니다.  
  
```  
bool IsLeftOf(
    CRect rect,  
    bool bWindowRect = true) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rect`  
 A `CRect` 비교에 사용 되는 개체입니다.  
  
 [in] `bWindowRect`  
 경우 `TRUE`, `rect` 경우; 화면 좌표를 포함 하도록 가정 `FALSE`, `rect` 클라이언트 좌표를 포함 하도록 간주 됩니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
 이 메서드는 왼쪽의 해당 위치 하는지 여부를 확인 하는 창이 가로로 도킹 되어, 경우 `rect`합니다. 그렇지 않으면이 메서드는 위치 위에 인지를 확인 `rect`합니다.  
  
##  <a name="isresizable"></a>CPane::IsResizable  
 창 크기를 조정할 수 있는지 여부를 지정 합니다.  
  
```  
virtual BOOL IsResizable() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`이 크기를 조정할 수 있습니다. 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 자료 `CPane` 개체 크기를 조정할 수 없기 때문입니다.  
  
 도킹 관리자 크기 조정 가능한 플래그를 사용 하 여 창 레이아웃을 결정 합니다. 부모 프레임의 외부 가장자리에 항상 비 크기 조정이 불가능 창이 나와 있습니다.  
  
 비-크기 조정 가능한 창 도킹 컨테이너에 있을 수 없습니다.  
  
##  <a name="istabbed"></a>CPane::IsTabbed  
 창에서 탭 컨트롤의 탭된 창에 삽입 되었음을 있는지 여부를 결정 합니다.  
  
```  
virtual BOOL IsTabbed() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창; 탭으로 연결 되어 있는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 탭된 상태 부동에서 별도로 처리 됩니다, 도킹 및 자동 숨김 상태입니다.  
  
##  <a name="loadstate"></a>CPane::LoadState  
 레지스트리에서 창의 상태를 로드 합니다.  
  
```  
virtual BOOL LoadState(
    LPCTSTR lpszProfileName = NULL,  
    int nIndex = -1,  
    UINT uiID = (UINT) -1);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszProfileName`  
 프로필 이름입니다.  
  
 [in] `nIndex`  
 프로필 인덱스입니다.  
  
 [in] `uiID`  
 창 id입니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창 상태를 성공적으로 로드 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 프레임 워크는 레지스트리에서 창의 상태를 로드 하려면이 메서드를 호출 합니다. 추가 정보를 로드 하 여 저장 되는 파생된 클래스에서 재정의 [CPane::SaveState](#savestate)합니다.  
  
 이 메서드를 재정의 하는 경우 또한 기본 메서드를 호출 하 고 반환 `FALSE` 기본 메서드를 반환 하는 경우 `FALSE`합니다.  
  
##  <a name="m_bhandleminsize"></a>CPane::m_bHandleMinSize  
 최소 창 크기의 일관 된 처리할 수 있습니다.  
  
```  
AFX_IMPORT_DATA static BOOL m_bHandleMinSize;  
```  
  
### <a name="remarks"></a>설명  
 응용 프로그램에서 하나 이상의 도킹 창을 재정의 `GetMinSize`, 응용 프로그램에서 호출 하는 경우 또는 `SetMinSize`,이 정적 멤버를 설정 하려면 `TRUE` 일관 되 게 창 크기는 어떻게를 처리 하기 위해 프레임 워크를 사용 하도록 설정 하려면.  
  
 이 값은로 설정 하는 경우 `TRUE`, 늘어나지은 필요에 따라 크기가 최소 크기 아래로 줄여야 하는 모든 창 잘립니다. 프레임 워크 창 영역 창 크기 조정 목적을 사용 하므로이 값은로 설정 하는 경우 창이 도킹 창 영역 크기를 변경 하지 마십시오 `TRUE`합니다.  
  
##  <a name="m_recentdockinfo"></a>M_recentdockinfo  
 최근 도킹 정보가 포함 되어 있습니다.  
  
```  
CRecentDockSiteInfo m_recentDockInfo;  
```  
  
### <a name="remarks"></a>설명  
 이 멤버에는 창에 대 한 최신 도킹 상태 정보를 저장 하는 프레임 워크입니다.  
  
##  <a name="movebyalignment"></a>CPane::MoveByAlignment  
 지정 된 크기는 창과 가상 사각형을 이동합니다.  
  
```  
BOOL MoveByAlignment(
    DWORD dwAlignment,  
    int nOffset);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `dwAlignment`  
 창 맞춤을 지정 합니다.  
  
 [in] `nOffset`  
 창과 가상 사각형 이동 하는 기준인 픽셀 양입니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
 `dwAlignment`다음 값 중 하나일 수 있습니다.  
  
|값|설명|  
|-----------|-----------------|  
|`CBRS_ALIGN_TOP`|창을 프레임 창의 클라이언트 영역의 위쪽에 도킹 될 수 있습니다.|  
|`CBRS_ALIGN_BOTTOM`|창을 프레임 창의 클라이언트 영역 아래쪽에 도킹 될 수 있습니다.|  
|`CBRS_ALIGN_LEFT`|창을 프레임 창의 클라이언트 영역의 왼쪽에 도킹 될 수 있습니다.|  
|`CBRS_ALIGN_RIGHT`|창을 프레임 창의 클라이언트 영역 오른쪽에 도킹 될 수 있습니다.|  
|`CBRS_ALIGN_ANY`|창을 프레임 창의 클라이언트 영역의 모든 면에 도킹 될 수 있습니다.|  
  
 경우 `dwAlignment` 포함는 `CBRS_ALIGN_LEFT` 또는 `CBRS_ALIGN_RIGHT` 플래그, 창 및 가상 사각형 이동 하 고, 그러지 않으면 가로로 `dwAlignment` 포함는 `CBRS_ALIGN_TOP` 또는 `CBRS_ALIGN_BOTTOM` 플래그, 창 및 가상 사각형 이동 세로로 합니다.  
  
##  <a name="movepane"></a>CPane::MovePane  
 창이 지정된 된 사각형으로 이동 합니다.  
  
```  
virtual CSize MovePane(
    CRect rectNew,  
    BOOL bForceMove,  
    HDWP& hdwp);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rectNew`  
 창에 새 사각형을 지정합니다.  
  
 [in] `bForceMove`  
 경우 `TRUE`,이 메서드는 허용 된 최소 창 크기를 무시 ( [CPane::GetMinSize](#getminsize)) 고, 그렇지 않으면, 창 인지 확인 최소한의 최소 크기를 허용 하기 위해 필요한 경우 조정 됩니다.  
  
 [in] `hdwp`  
 사용되지 않습니다.  
  
### <a name="return-value"></a>반환 값  
 A `CSize` 신규 버전과 기존 사각형의 너비 및 높이의 차이 포함 하는 개체 (오래 된 사각형- `rectNew`).  
  
### <a name="remarks"></a>설명  
 이 메서드는 도킹 가능한 창에 대해서만 사용 됩니다.  
  
##  <a name="onafterchangeparent"></a>CPane::OnAfterChangeParent  
 부모 창의 변경 될 때 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnAfterChangeParent(CWnd* pWndOldParent);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] [out]`pWndOldParent`  
 창의 이전 부모 창입니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 부모 창의 도킹 또는 부동 형식 작업으로 인해 변경 될 때 프레임 워크에서 호출 됩니다.  
  
##  <a name="onafterdock"></a>CPane::OnAfterDock  
 창을 도킹 된 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnAfterDock(
    CBasePane* pBar,  
    LPCRECT lpRect,  
    AFX_DOCK_METHOD dockMethod);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pBar`  
 이 매개 변수는 사용되지 않습니다.  
  
 [in] `lpRect`  
 이 매개 변수는 사용되지 않습니다.  
  
 [in] `dockMethod`  
 이 매개 변수는 사용되지 않습니다.  
  
##  <a name="onafterfloat"></a>CPane::OnAfterFloat  
 창을 부동 후 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnAfterFloat();
```  
  
### <a name="remarks"></a>설명  
 창을 부동 하는 후 처리를 수행 하려는 경우이 메서드는 파생된 클래스에서 재정의할 수 있습니다.  
  
##  <a name="onbeforechangeparent"></a>CPane::OnBeforeChangeParent  
 부모 창의 변경 되려고 할 때 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnBeforeChangeParent(
    CWnd* pWndNewParent,  
    BOOL bDelay = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] [out]`pWndNewParent`  
 새 부모 창을 지정합니다.  
  
 [in] `bDelay`  
 `TRUE`전역 도킹 레이아웃 조정; 지연 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 프레임 워크에서 창의 부모 창에서 되 고 있어서 변경 되려고 할 때 도킹 하거나 부동 합니다.  
  
 기본적으로 창에서 등록 되어 있지 않은 도킹 창으로 호출 하 여 `CDockSite::RemovePane`합니다.  
  
##  <a name="onbeforedock"></a>CPane::OnBeforeDock  
 창 도킹 되려고 할 때 프레임 워크에서 호출 됩니다.  
  
```  
virtual BOOL OnBeforeDock(
    CBasePane** ppDockBar,  
    LPCRECT lpRect,  
    AFX_DOCK_METHOD dockMethod);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] [out]`ppDockBar`  
 이 창에 도킹 되는 창을 지정 합니다.  
  
 [in] `lpRect`  
 도킹 사각형을 지정합니다.  
  
 [in] `dockMethod`  
 도킹 방법을 지정합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창에 도킹할 수 있는 경우. 함수가 반환 하는 경우 `FALSE`, 도킹 작업이 중단 됩니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 창이 도킹 될 되려고 할 때 프레임 워크에서 호출 됩니다. 창을 도킹 마지막 전에 처리를 수행 하려는 경우이 메서드는 파생된 클래스에서 재정의할 수 있습니다.  
  
##  <a name="onbeforefloat"></a>CPane::OnBeforeFloat  
 Float에 대 한이 되 면 프레임 워크에서 호출 됩니다.  
  
```  
virtual BOOL OnBeforeFloat(
    CRect& rectFloat,  
    AFX_DOCK_METHOD dockMethod);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rectFloat`  
 부동 상태에 있을 때 창의 크기와 위치를 지정 합니다.  
  
 [in] `dockMethod`  
 창 도킹 방법을 지정합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`창 수 놓을지; 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 float로에 대 한이 되 면 프레임 워크에서 호출 됩니다. 창에서 마지막으로 표시 되기 전에 처리를 수행 하려는 경우이 메서드는 파생된 클래스에서 재정의할 수 있습니다.  
  
##  <a name="onpressclosebutton"></a>CPane::OnPressCloseButton  
 사용자는 창에 대 한 캡션을 닫기 단추를 누를 때 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnPressCloseButton();
```  
  
### <a name="remarks"></a>설명  
 이 메서드는 프레임 워크에서 사용자가 누를 때는 **닫기** 창의 캡션 단추입니다. 에 대 한 알림을 받을 수는 **닫기** 이벤트의 경우 파생된 클래스에서이 메서드를 재정의할 수 있습니다.  
  
##  <a name="onshowcontrolbarmenu"></a>Cpane:: Onshowcontrolbarmenu  
 특수 창 메뉴를 표시하려고 할 때 프레임워크에서 호출됩니다.  
  
```  
virtual BOOL OnShowControlBarMenu(CPoint point);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `point`  
 메뉴 위치를 지정합니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`이면 메뉴를 표시할 수 있습니다. 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 즉 창의 동작을 지정할 수 있도록 하는 여러 항목을 포함 하는 메뉴: **부동**, **도킹**, **AutoHide**, 및 **숨기기**. 호출 하 여 모든 창에 대 한이 메뉴를 사용 하도록 설정할 수 [CDockingManager::EnableDockSiteMenu](../../mfc/reference/cdockingmanager-class.md#enabledocksitemenu)합니다.  
  
##  <a name="recalclayout"></a>Cpane:: Recalclayout  
 창에 대 한 레이아웃 정보를 다시 계산합니다.  
  
```  
virtual void RecalcLayout();
```  
  
### <a name="remarks"></a>설명  
 창이 도킹 되어 있는,이 메서드는 창에 대 한 가상 사각형 크기로 창의 현재 크기를 설정 하 여 업데이트 합니다.  
  
 창 부동 창인 경우이 메서드는 미니 프레임의 크기에 창 크기를 조정 하려면 부모 미니 프레임을 알립니다. 프레임 워크를 사용 하면 미니 프레임 창의 크기를 허용 되는 최소값 이상 인지 ( [CPane::GetMinSize](#getminsize)) 필요한 경우 미니 프레임 크기를 조정 합니다.  
  
##  <a name="savestate"></a>CPane::SaveState  
 레지스트리에 창의 상태를 저장합니다.  
  
```  
virtual BOOL SaveState(
    LPCTSTR lpszProfileName = NULL,  
    int nIndex = -1,  
    UINT uiID = (UINT) -1);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszProfileName`  
 프로필 이름입니다.  
  
 [in] `nIndex`  
 프로필 인덱스입니다.  
  
 [in] `uiID`  
 창 id입니다.  
  
### <a name="return-value"></a>반환 값  
 `TRUE`상태가 성공적으로; 저장 하는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 레지스트리에 창의 상태를 저장 하는 경우이 메서드를 호출 하는 프레임 워크입니다. 재정의 `SaveState` 는 추가 정보를 저장 합니다.  
  
 이 메서드를 재정의 하는 경우 또한 기본 메서드를 호출 하 고 반환 `FALSE` 기본 메서드를 반환 하는 경우 `FALSE`합니다.  
  
##  <a name="setactiveingroup"></a>Cpane:: Setactiveingroup  
 창에 활성으로 플래그 지정합니다.  
  
```  
virtual void SetActiveInGroup(BOOL bActive);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bActive`  
 A `BOOL` 창에서 활성화 된 것으로 플래그가 있는지 여부를 지정 하는 합니다.  
  
### <a name="remarks"></a>설명  
 자동 숨기기 단추를 선택 또는 도킹 가능한 창을 표시 되며, 해당 자동 숨기기 창 활성화 된 것으로 표시 됩니다.  
  
 연결 된 창 자동 숨기기 단추의 모양은 두 가지 요소를 기반으로 합니다. 창이 활성화 되 면 및 `static BOOL CMFCAutoHideButton::m_bOverlappingTabs` 은 `TRUE`, 프레임 워크는 아이콘과 레이블을로 자동 숨기기 단추를 표시 합니다. 비활성 창에 대 한 프레임 워크의 자동 숨기기 아이콘을 표시합니다.  
  
 경우 `CMFCAutoHideButton::m_bOverlappingTabs` 은 `FALSE`, 프레임 워크는 아이콘과 레이블을으로 관련된 자동 숨기기 단추를 표시 창에서 그룹에 없는 경우, 또는.  
  
##  <a name="setborders"></a>CPane::SetBorders  
 창의 테두리 값을 설정합니다.  
  
```  
void SetBorders(
    int cxLeft = 0,  
    int cyTop = 0,  
    int cxRight = 0,  
    int cyBottom = 0);  
  
void SetBorders(LPCRECT lpRect);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `cxLeft`  
 픽셀, 창의 왼쪽된 테두리의 너비를 지정 합니다.  
  
 [in] `cyTop`  
 창의 위쪽 테두리의 픽셀에서 너비를 지정 합니다.  
  
 [in] `cxRight`  
 창의 오른쪽 테두리의 픽셀에서 너비를 지정 합니다.  
  
 [in] `cyBottom`  
 창의 아래쪽 테두리의 픽셀에서 너비를 지정 합니다.  
  
 [in] `lpRect`  
 A [CRect](../../atl-mfc-shared/reference/crect-class.md) 창의 각 테두리의 픽셀에서 너비를 포함 하는 개체입니다.  
  
### <a name="remarks"></a>설명  
 창 테두리의 크기를 설정 하려면이 함수를 호출 합니다.  
  
##  <a name="setclienthotspot"></a>CPane::SetClientHotSpot  
 설정의 *핫 스폿* 는 창에 대 한 합니다.  
  
```  
void SetClientHotSpot(const CPoint& ptNew);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `ptNew`  
 A `CPoint` 새 핫 스폿을 지정 하는 개체입니다.  
  
### <a name="remarks"></a>설명  
 *핫 스폿* 는 사용자가 선택한 창을 이동 하려면 보유 하는 창에서 점으로 합니다. 창 도킹된 위치에서 끌어 놓으면 핫 스폿 부드러운 애니메이션에 사용 됩니다.  
  
##  <a name="setdockstate"></a>CPane::SetDockState  
 도킹 된 창에 대 한 상태 정보를 복원 합니다.  
  
```  
virtual void SetDockState(CDockingManager* pDockManager);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDockManager`  
 주 프레임 창에 대 한 고 도킹 관리자에 대 한 포인터입니다.  
  
### <a name="remarks"></a>설명  
 이 메서드는 창에 대 한 최근 도킹 상태 정보를 복원 하기 위해 프레임 워크에서 호출 됩니다. 에 최근 도킹 상태 정보를 저장 하는 창을 [M_recentdockinfo](#m_recentdockinfo)합니다. 자세한 내용은 참조는 [CRecentDockSiteInfo 클래스](../../mfc/reference/crecentdocksiteinfo-class.md)합니다.  
  
 외부 소스에서 창 정보를 로드할 때 도킹 상태를 설정 하려면이 메서드를 호출할 수 있습니다.  
  
##  <a name="setexclusiverowmode"></a>CPane::SetExclusiveRowMode  
 배타 행 모드를 해제 하거나 사용 합니다.  
  
```  
virtual void SetExclusiveRowMode(BOOL bExclusive = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bExclusive`  
 `TRUE`배타 행 모드를 사용 하도록 설정 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 배타적 행 모드를 사용 하지 않도록 설정 하거나 설정 하려면이 메서드를 호출 합니다. 창을 배타 행 모드일 때 다른 도구 모음 같은 행을 공유할 수 없습니다 것입니다.  
  
 기본적으로 도구 모음을 모두 사용 하지 않도록 설정 하는 배타 행 모드 있고 메뉴 모음에 배타 행 모드를 사용 합니다.  
  
##  <a name="setminsize"></a>CPane::SetMinSize  
 창 크기에 허용 되는 최소값을 설정 합니다.  
  
```  
void SetMinSize(const CSize& size);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `size`  
 A `CSize` 허용 크기는 창에 대 한 최소값을 포함 하는 개체입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="setvirtualrect"></a>CPane::SetVirtualRect  
 설정의 *가상 사각형* 창.  
  
```  
void SetVirtualRect(
    const CRect& rect,  
    BOOL bMapToParent = TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rect`  
 A `CRect` 설정할 가상 사각형을 지정 하는 개체입니다.  
  
 [in] `bMapToParent`  
 지정 `TRUE` 경우 `rect` 부모 창 기준으로 하는 점을 포함 합니다.  
  
### <a name="remarks"></a>설명  
 A *가상 사각형* 이동할 때 창의 원래 위치를 저장 합니다. 프레임 워크 원래 위치로 복원 하려면 가상 사각형을 사용할 수 있습니다.  
  
 창을 프로그래밍 방식으로 이동 하려는 경우가 아니면 가상 사각형에 관련 된 메서드를 호출 하지 마십시오.  
  
##  <a name="setminiframertc"></a>CPane::SetMiniFrameRTC  
 기본 미니 프레임 창에 대 한 런타임 클래스 정보를 설정합니다.  
  
```  
void SetMiniFrameRTC(CRuntimeClass* pClass);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] [out]`pClass`  
 미니 프레임 창에 대 한 런타임 클래스 정보를 지정합니다.  
  
### <a name="remarks"></a>설명  
 창을 움직이는 있을 때 추가 됩니다 한 [CPaneFrameWnd](../../mfc/reference/cpaneframewnd-class.md) (미니 프레임) 창. 사용자 지정을 제공할 수 있습니다 `CPaneFrameWnd`-파생 클래스가 될 때 사용 [cpane:: Createdefaultminiframe](#createdefaultminiframe) 호출 됩니다.  
  
##  <a name="stretchpanedeferwndpos"></a>CPane::StretchPaneDeferWndPos  
 가로 또는 세로로 도킹 스타일에 따라 창을 늘어납니다.  
  
```  
virtual int StretchPaneDeferWndPos(
    int nStretchSize,  
    HDWP& hdwp);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nStretchSize`  
 스트레치 창에서 픽셀 양입니다. 창 축소 하는 음수 값을 사용 합니다.  
  
 [in] `hdwp`  
 사용되지 않습니다.  
  
### <a name="return-value"></a>반환 값  
 창 스트레치 되었는지 (픽셀)는 실제 크기입니다.  
  
### <a name="remarks"></a>설명  
 필요에 따라이 수정 `nStretchSize` 하 고 창 크기 제한을 초과 하지 않도록 합니다. 호출 하 여 이러한 제한을 가져옵니다 [CPane::GetAvailableStretchSize](#getavailablestretchsize) 및 [CPane::GetAvailableExpandSize](#getavailableexpandsize)합니다.  
  
##  <a name="toggleautohide"></a>CPane::ToggleAutoHide  
 자동 숨기기 모드를 설정/해제 합니다.  
  
```  
virtual void ToggleAutoHide();
```  
  
### <a name="remarks"></a>설명  
 자동 숨기기 모드를 전환 하려면이 메서드를 호출 합니다. 자동 숨기기 모드로 전환 하기 위해 창은 주 프레임 창에 도킹 해야 합니다.  
  
##  <a name="undockpane"></a>CPane::UndockPane  
 도킹 사이트, 기본 슬라이더 또는 현재 도킹 되는 미니 프레임 창에서 창에서를 제거 합니다.  
  
```  
virtual void UndockPane(BOOL bDelay = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bDelay`  
 경우 `FALSE`, 프레임 워크를 호출 하 여 [:: Adjustdockinglayout](../../mfc/reference/cbasepane-class.md#adjustdockinglayout) 도킹 레이아웃을 조정 해야 합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드를 사용 하 여 프로그래밍 방식으로 창을 도킹을 해제 합니다.  
  
##  <a name="updatevirtualrect"></a>CPane::UpdateVirtualRect  
 가상 사각형을 업데이트합니다.  
  
```  
void UpdateVirtualRect();  
void UpdateVirtualRect(CPoint ptOffset);  
  void UpdateVirtualRect(CSize sizeNew);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `ptOffset`  
 A `CPoint` 를 창에서 이동할 기준이 되는 오프셋을 지정 하는 개체입니다.  
  
 [in] `sizeNew`  
 A `CSize` 는 창에 대 한 새 크기를 지정 하는 개체입니다.  
  
### <a name="remarks"></a>설명  
 첫 번째 오버 로드는 현재 위치와 창 크기를 사용 하 여 가상 사각형을 설정 합니다.  
  
 두 번째 오버 로드 가상 사각형으로 지정 된 크기 만큼 이동 `ptOffset`합니다.  
  
 세 번째 오버 로드는 창 고에 지정 된 크기의 현재 위치를 사용 하 여 가상 사각형을 설정 `sizeNew`합니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CBasePane 클래스](../../mfc/reference/cbasepane-class.md)
