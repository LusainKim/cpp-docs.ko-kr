---
title: "CMFCRibbonGallery 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCRibbonGallery
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::CMFCRibbonGallery
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::AddGroup
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::AddSubItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::Clear
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::EnableMenuResize
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::EnableMenuSideBar
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetCompactSize
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetDroppedDown
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetGroupName
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetGroupOffset
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetIconsInRow
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetItemToolTip
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetLastSelectedItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetPaletteID
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetRegularSize
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::GetSelectedItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::HasMenu
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsButtonMode
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsMenuResizeEnabled
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsMenuResizeVertical
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::IsMenuSideBar
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnAfterChangeRect
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnDraw
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnEnable
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnRTLChanged
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::RedrawIcons
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::RemoveItemToolTips
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SelectItem
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetACCData
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetButtonMode
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetGroupName
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetIconsInRow
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetItemToolTip
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetPalette
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::SetPaletteID
- AFXRIBBONPALETTEGALLERY/CMFCRibbonGallery::OnDrawPaletteIcon
dev_langs: C++
helpviewer_keywords:
- CMFCRibbonGallery [MFC], CMFCRibbonGallery
- CMFCRibbonGallery [MFC], AddGroup
- CMFCRibbonGallery [MFC], AddSubItem
- CMFCRibbonGallery [MFC], Clear
- CMFCRibbonGallery [MFC], EnableMenuResize
- CMFCRibbonGallery [MFC], EnableMenuSideBar
- CMFCRibbonGallery [MFC], GetCompactSize
- CMFCRibbonGallery [MFC], GetDroppedDown
- CMFCRibbonGallery [MFC], GetGroupName
- CMFCRibbonGallery [MFC], GetGroupOffset
- CMFCRibbonGallery [MFC], GetIconsInRow
- CMFCRibbonGallery [MFC], GetItemToolTip
- CMFCRibbonGallery [MFC], GetLastSelectedItem
- CMFCRibbonGallery [MFC], GetPaletteID
- CMFCRibbonGallery [MFC], GetRegularSize
- CMFCRibbonGallery [MFC], GetSelectedItem
- CMFCRibbonGallery [MFC], HasMenu
- CMFCRibbonGallery [MFC], IsButtonMode
- CMFCRibbonGallery [MFC], IsMenuResizeEnabled
- CMFCRibbonGallery [MFC], IsMenuResizeVertical
- CMFCRibbonGallery [MFC], IsMenuSideBar
- CMFCRibbonGallery [MFC], OnAfterChangeRect
- CMFCRibbonGallery [MFC], OnDraw
- CMFCRibbonGallery [MFC], OnEnable
- CMFCRibbonGallery [MFC], OnRTLChanged
- CMFCRibbonGallery [MFC], RedrawIcons
- CMFCRibbonGallery [MFC], RemoveItemToolTips
- CMFCRibbonGallery [MFC], SelectItem
- CMFCRibbonGallery [MFC], SetACCData
- CMFCRibbonGallery [MFC], SetButtonMode
- CMFCRibbonGallery [MFC], SetGroupName
- CMFCRibbonGallery [MFC], SetIconsInRow
- CMFCRibbonGallery [MFC], SetItemToolTip
- CMFCRibbonGallery [MFC], SetPalette
- CMFCRibbonGallery [MFC], SetPaletteID
- CMFCRibbonGallery [MFC], OnDrawPaletteIcon
ms.assetid: 9734c9c9-981c-4b3f-8c59-264fd41811b4
caps.latest.revision: "28"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: 6cb4772f685a38db39c946a5e6f4e77df87998a5
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cmfcribbongallery-class"></a>CMFCRibbonGallery 클래스
Office 2007 스타일의 리본 갤러리를 구현합니다.  
 [!INCLUDE[cpp_fp_under_construction](../../mfc/reference/includes/cpp_fp_under_construction_md.md)]  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCRibbonGallery : public CMFCRibbonButton  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCRibbonGallery::CMFCRibbonGallery](#cmfcribbongallery)|`CMFCRibbonGallery` 개체를 생성하고 초기화합니다.|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCRibbonGallery::AddGroup](#addgroup)|갤러리에 새 그룹을 추가합니다.|  
|[CMFCRibbonGallery::AddSubItem](#addsubitem)|드롭다운 메뉴에 새 메뉴 항목을 추가합니다.|  
|[CMFCRibbonGallery::Clear](#clear)|갤러리의 내용을 지웁니다.|  
|[CMFCRibbonGallery::EnableMenuResize](#enablemenuresize)|메뉴 패널의 크기를 조정 하지 않도록 설정 하거나 사용 합니다.|  
|[CMFCRibbonGallery::EnableMenuSideBar](#enablemenusidebar)|팝업 메뉴의 왼쪽 세로 막대를 사용 하지 않도록 설정 하거나 사용 합니다.|  
|[CMFCRibbonGallery::GetCompactSize](#getcompactsize)|(재정의 [cmfcribbonbutton:: Getcompactsize](../../mfc/reference/cmfcribbonbutton-class.md#getcompactsize).)|  
|[CMFCRibbonGallery::GetDroppedDown](#getdroppeddown)|(재정의 [CMFCRibbonBaseElement::GetDroppedDown](../../mfc/reference/cmfcribbonbaseelement-class.md#getdroppeddown).)|  
|[CMFCRibbonGallery::GetGroupName](#getgroupname)|지정된 된 인덱스에 있는 그룹의 이름을 반환 합니다.|  
|[CMFCRibbonGallery::GetGroupOffset](#getgroupoffset)||  
|[CMFCRibbonGallery::GetIconsInRow](#geticonsinrow)|리본 갤러리의 행에 있는 항목의 수를 반환합니다.|  
|[CMFCRibbonGallery::GetItemToolTip](#getitemtooltip)|갤러리의 항목과 연결 된 도구 설명 텍스트를 반환 합니다.|  
|[CMFCRibbonGallery::GetLastSelectedItem](#getlastselecteditem)|사용자가 선택한 갤러리에 있는 마지막 항목의 인덱스를 반환 합니다.|  
|[CMFCRibbonGallery::GetPaletteID](#getpaletteid)|현재 갤러리의 명령 ID를 반환합니다.|  
|[CMFCRibbonGallery::GetRegularSize](#getregularsize)|(재정의 [cmfcribbonbutton:: Getregularsize](../../mfc/reference/cmfcribbonbutton-class.md#getregularsize).)|  
|[CMFCRibbonGallery::GetSelectedItem](#getselecteditem)||  
|[CMFCRibbonGallery::HasMenu](#hasmenu)|(재정의 [CMFCRibbonButton::HasMenu](../../mfc/reference/cmfcribbonbutton-class.md#hasmenu).)|  
|[CMFCRibbonGallery::IsButtonMode](#isbuttonmode)|갤러리 갤러리 단추에 포함 되는지 여부를 지정 합니다.|  
|[CMFCRibbonGallery::IsMenuResizeEnabled](#ismenuresizeenabled)|크기 조정 메뉴는 사용 가능 여부를 지정 합니다.|  
|[CMFCRibbonGallery::IsMenuResizeVertical](#ismenuresizevertical)||  
|[CMFCRibbonGallery::IsMenuSideBar](#ismenusidebar)|세로 막대 사용 되는지 여부를 지정 합니다.|  
|[CMFCRibbonGallery::OnAfterChangeRect](#onafterchangerect)|(`CMFCRibbonButton::OnAfterChangeRect`를 재정의합니다.)|  
|[CMFCRibbonGallery::OnDraw](#ondraw)|(재정의 [cmfcribbonbutton:: Ondraw](../../mfc/reference/cmfcribbonbutton-class.md#ondraw).)|  
|[CMFCRibbonGallery::OnEnable](#onenable)|(`CMFCRibbonBaseElement::OnEnable`를 재정의합니다.)|  
|[CMFCRibbonGallery::OnRTLChanged](#onrtlchanged)|(재정의 [CMFCRibbonBaseElement::OnRTLChanged](../../mfc/reference/cmfcribbonbaseelement-class.md#onrtlchanged).)|  
|[CMFCRibbonGallery::RedrawIcons](#redrawicons)|갤러리를 다시 그립니다.|  
|[CMFCRibbonGallery::RemoveItemToolTips](#removeitemtooltips)|갤러리에 있는 모든 항목에서 도구 설명을 제거합니다.|  
|[CMFCRibbonGallery::SelectItem](#selectitem)||  
|[CMFCRibbonGallery::SetACCData](#setaccdata)|(재정의 [cmfcribbonbutton:: Setaccdata](../../mfc/reference/cmfcribbonbutton-class.md#setaccdata).)|  
|[CMFCRibbonGallery::SetButtonMode](#setbuttonmode)|드롭 다운 단추 또는 리본에서 직접 색상표도 리본 갤러리를 표시할지 여부를 지정 합니다.|  
|[CMFCRibbonGallery::SetGroupName](#setgroupname)|그룹의 이름을 설정합니다.|  
|[CMFCRibbonGallery::SetIconsInRow](#seticonsinrow)|갤러리에서 각 행의 항목 수를 정의합니다.|  
|[CMFCRibbonGallery::SetItemToolTip](#setitemtooltip)|갤러리에서 항목에 대 한 도구 설명 텍스트를 설정합니다.|  
|[CMFCRibbonGallery::SetPalette](#setpalette)|리본 갤러리를 색상표를 연결합니다.|  
|[CMFCRibbonGallery::SetPaletteID](#setpaletteid)|전송 된 명령 ID를 정의 고 `WM_COMMAND` 갤러리 항목을 선택 하는 경우 메시지입니다.|  
  
### <a name="protected-methods"></a>Protected 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCRibbonGallery::OnDrawPaletteIcon](#ondrawpaletteicon)|갤러리 아이콘을 그릴 때 프레임 워크에서 호출 됩니다.|  
  
## <a name="remarks"></a>설명  
 갤러리 단추는 사용자가 열 때 갤러리를 표시 한다는 일반 메뉴 단추 처럼 동작 합니다. 갤러리에서 항목을 선택할 때 프레임 워크 보냅니다는 `WM_COMMAND` 단추의 명령 ID와 함께 메시지입니다. 메시지를 처리 하는 경우 호출 해야 [CMFCRibbonGallery::GetLastSelectedItem](#getlastselecteditem) 갤러리에서 선택 된 항목을 찾으려고 합니다.  
  
## <a name="example"></a>예  
 다음 예제에서 다양 한 메서드를 사용 하는 방법을 보여 줍니다는 `CMFCRibbonGallery` 구성 하는 클래스는 `CMFCRibbonGallery` 개체입니다. 이 예제에서는 갤러리의 행 마다 항목의 수를 지정, 메뉴 패널의 크기 조정 가능 하 고, 팝업 메뉴의 왼쪽에 세로 막대를 활성화 하 고 리본 메뉴 모음에 직접 색상표로 리본 갤러리를 표시 하는 방법을 보여 줍니다. 이 코드 조각은 [클라이언트 그리기 샘플](../../visual-cpp-samples.md)의 일부입니다.  
  
 [!code-cpp[NVC_MFC_DrawClient#6](../../mfc/reference/codesnippet/cpp/cmfcribbongallery-class_1.cpp)]  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md) [CMFCRibbonBaseElement](../../mfc/reference/cmfcribbonbaseelement-class.md) [CMFCRibbonButton](../../mfc/reference/cmfcribbonbutton-class.md)  
  
 [CMFCRibbonGallery](../../mfc/reference/cmfcribbongallery-class.md)  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxRibbonPaletteGallery.h  
  
##  <a name="addgroup"></a>CMFCRibbonGallery::AddGroup  
 갤러리에 새 그룹을 추가합니다.  
  
```  
void AddGroup(
    LPCTSTR lpszGroupName,  
    UINT uiImagesPaletteResID,  
    int cxPaletteImage);

 
void AddGroup(
    LPCTSTR lpszGroupName,  
    CMFCToolBarImages& imagesGroup);

 
void AddGroup(
    LPCTSTR lpszGroupName,  
    int nIconsNum);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `lpszGroupName`  
 그룹의 이름을 지정합니다.  
  
 [in] `uiImagesPaletteResID`  
 그룹에 대 한 이미지가 포함 된 이미지 목록의 리소스 ID를 지정 합니다.  
  
 [in] `cxPaletteImage`  
 픽셀 이미지의 너비를 지정합니다.  
  
 [in] `imagesGroup`  
 그룹 이미지를 포함 하는 이미지 목록에 대 한 참조입니다.  
  
 [in] `nIconsNum`  
 그룹의 아이콘 수를 지정합니다. 사용자 지정 (소유자 그리기)에 대해서만이 매개 변수를 지정 해야 그룹입니다.  
  
### <a name="remarks"></a>설명  
 이 메서드를 호출 하 여 리본 갤러리에 있는 항목이 여러 그룹으로 나눌 수 있습니다. 각 그룹 캡션을 가질 수 있습니다.  
  
##  <a name="addsubitem"></a>CMFCRibbonGallery::AddSubItem  
 드롭다운 메뉴에 새 메뉴 항목을 추가합니다.  
  
```  
void AddSubItem(
    CMFCRibbonBaseElement* pSubItem,  
    int nIndex=-1,  
    BOOL bOnTop=FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pSubItem`  
 메뉴에 추가할 항목에 대 한 포인터입니다.  
  
 [in] `nIndex`  
 위치의 0부터 시작 하는 인덱스 항목을 삽입할 위치를 지정 합니다.  
  
 [in] `bOnTop`  
 `TRUE`리본 갤러리; 하기 전에 항목을 삽입할 지정 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 이 메서드를 호출 하 여 팝업 갤러리 팝업 메뉴 항목과 함께 결합할 수 있습니다. 앞 이나 뒤 갤러리 메뉴 항목을 배치할 수 있습니다.  
  
 앞에서 갤러리 항목을 삽입 하려면 설정 `bOnTop` 를 `TRUE`합니다. 설정 `bOnTop` 를 `FALSE` 갤러리 아래 항목을 삽입 합니다.  
  
> [!NOTE]
>  매개 변수 `nIndex` 갤러리의 위쪽 및 아래쪽 갤러리에 삽입 하는 인덱스를 지정 합니다. 예를 들어 앞에서 갤러리 항목 한 위치는 삽입 해야 설정 `nIndex` 1로 및 `bOnTop` 를 `TRUE`합니다. 마찬가지로, 갤러리 아래에 항목 한 위치를 삽입 해야 하는 경우 설정할 `nIndex` 1 및 `bOnTop` 를 `FALSE`합니다.  
  
##  <a name="clear"></a>CMFCRibbonGallery::Clear  
 갤러리의 내용을 지웁니다.  
  
```  
virtual void Clear();
```  
  
### <a name="remarks"></a>설명  
 리본 갤러리에서 모든 콘텐츠를 제거 하려면이 메서드를 호출 합니다. 리본 갤러리에는 새 리본 갤러리 또는 그룹 집합을 연결 하기 전에 수행 되어야 합니다.  
  
##  <a name="cmfcribbongallery"></a>CMFCRibbonGallery::CMFCRibbonGallery  
 생성 하 고 초기화는 [CMFCRibbonGallery](../../mfc/reference/cmfcribbongallery-class.md) 개체입니다.  
  
```  
CMFCRibbonGallery (
    UINT nID,  
    LPCTSTR lpszText,  
    int nSmallImageIndex,  
    int nLargeImageIndex,  
    CMFCToolBarImages& imagesPalette);

 
CMFCRibbonGallery (
    UINT nID,  
    LPCTSTR lpszText,  
    int nSmallImageIndex,  
    int nLargeImageIndex,  
    UINT uiImagesPaletteResID=0,  
    int cxPaletteImage=0);

 
CMFCRibbonGallery (
    UINT nID,  
    LPCTSTR lpszText,  
    int nSmallImageIndex,  
    int nLargeImageIndex,  
    CSize sizeIcon,  
    int nIconsNum,  
    BOOL bDefaultButtonStyle=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 `nID`  
 단추를 클릭할 때 실행할 명령의 명령 ID를 지정 합니다.  
  
 `lpszText`  
 단추에 표시할 텍스트를 지정 합니다.  
  
 `nSmallImageIndex`  
 단추에 표시할 작은 이미지의 0부터 시작 하는 인덱스입니다.  
  
 `nLargeImageIndex`  
 큰 단추에 표시할 이미지의 0부터 시작 하는 인덱스입니다.  
  
 `imagesPalette`  
 에 대 한 참조는 [CMFCToolBarImages](../../mfc/reference/cmfctoolbarimages-class.md) 갤러리에 표시할 이미지를 포함 하는 개체입니다.  
  
 `uiImagesPaletteResID`  
 갤러리에 표시할 이미지 목록은의 리소스 ID입니다.  
  
 `cxPaletteImage`  
 갤러리에서 이미지를 픽셀 단위로 너비를 지정 합니다.  
  
 `sizeIcon`  
 갤러리 이미지를 픽셀 단위로 크기를 지정 합니다.  
  
 `nIconsNum`  
 갤러리의 아이콘 수를 지정합니다.  
  
 `bDefaultButtonStyle`  
 기본값 또는 소유자가 그린 단추를 사용할 것인지 지정 합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="enablemenuresize"></a>CMFCRibbonGallery::EnableMenuResize  
 메뉴 패널의 크기를 조정 하지 않도록 설정 하거나 사용 합니다.  
  
```  
void EnableMenuResize(
    BOOL bEnable = TRUE,  
    BOOL bVertcalOnly = FALSE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
 `TRUE`메뉴; 크기를 조정 하는 사용 하도록 설정 하려면 그렇지 않으면 `FALSE`합니다.  
  
 [in] `bVertcalOnly`  
 `TRUE`갤러리만; 세로로 조정할 수 있는 지정 하려면 `FALSE` 갤러리 수 있도록 지정 하려면 조정할 세로 및 가로로 합니다.  
  
### <a name="remarks"></a>설명  
 리본 갤러리를 크기 조정 사용 하지 않도록 설정 하거나 설정 하려면이 메서드를 사용 합니다. 크기를 조정할 때 리본 갤러리 사용자 크기를 조정 하는 데 사용할 수 있는 위치 조정 막대를 표시 합니다.  
  
##  <a name="enablemenusidebar"></a>CMFCRibbonGallery::EnableMenuSideBar  
 팝업 메뉴의 왼쪽 세로 막대를 사용 하지 않도록 설정 하거나 사용 합니다.  
  
```  
void EnablMenuSideBar(BOOL bEnable=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
 `TRUE`세로 막대, 로깅을 지정 하려면 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
 메뉴의 왼쪽에 Office XP 스타일 세로 막대를 사용 하지 않도록 설정 하거나 설정 하려면이 메서드를 호출 합니다.  
  
##  <a name="getcompactsize"></a>CMFCRibbonGallery::GetCompactSize  

  
```  
virtual CSize GetCompactSize(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="getdroppeddown"></a>CMFCRibbonGallery::GetDroppedDown  

  
```  
virtual CMFCRibbonBaseElement* GetDroppedDown();
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="getgroupname"></a>CMFCRibbonGallery::GetGroupName  
 지정된 된 인덱스에 있는 그룹의 이름을 반환 합니다.  
  
```  
LPCTSTR GetGroupName(int nGroupIndex) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nGroupIndex`  
 그룹을 검색 하려면 해당 이름에 대 한 0부터 시작 인덱스를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 지정된 된 인덱스에 있는 그룹의 이름입니다. 잘못 된 인덱스가 전달 실패 한 어설션이 발생 합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getgroupoffset"></a>CMFCRibbonGallery::GetGroupOffset  

  
```  
virtual int GetGroupOffset() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="geticonsinrow"></a>CMFCRibbonGallery::GetIconsInRow  
 리본 갤러리의 행에 있는 항목의 수를 반환합니다.  
  
```  
int GetIconsInRow() const;  
```  
  
### <a name="return-value"></a>반환 값  
 행에 있는 항목의 수입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getitemtooltip"></a>CMFCRibbonGallery::GetItemToolTip  
 갤러리의 항목과 연결 된 도구 설명 텍스트를 반환 합니다.  
  
```  
LPCTSTR GetItemToolTip(int nItemIndex) const;  
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nItemIndex`  
 도구 설명 텍스트를 검색할 항목의 0부터 시작 인덱스를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 리본 갤러리에 있는 항목에 할당 된 도구 설명 문자열에 대 한 포인터입니다. 것이 `NULL` 도구 설명이 해당 항목에 할당 된 경우.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getlastselecteditem"></a>CMFCRibbonGallery::GetLastSelectedItem  
 사용자가 선택한 리본 갤러리에 있는 마지막 항목의 인덱스를 반환 합니다.  
  
```  
static int GetLastSelectedItem(UINT uiCmdID);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `uiCmdID`  
 리본 갤러리 열리는 메뉴 항목의 명령 ID를 지정 합니다.  
  
### <a name="return-value"></a>반환 값  
 사용자가 리본 갤러리에서 모든 항목을 선택 하면 라이브러리에서 보냅니다는 `WM_COMMAND` 리본 갤러리 열리는 메뉴 단추의 명령 ID와 함께 메시지입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getpaletteid"></a>CMFCRibbonGallery::GetPaletteID  
 현재 색상표의 명령 ID를 반환합니다.  
  
```  
int GetPaletteID() const;  
```  
  
### <a name="return-value"></a>반환 값  
 현재 선택 된 색상표의 명령 ID입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="getregularsize"></a>CMFCRibbonGallery::GetRegularSize  

  
```  
virtual CSize GetRegularSize(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="getselecteditem"></a>CMFCRibbonGallery::GetSelectedItem  

  
```  
int GetSelectedItem() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="hasmenu"></a>CMFCRibbonGallery::HasMenu  

  
```  
virtual BOOL HasMenu() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="isbuttonmode"></a>CMFCRibbonGallery::IsButtonMode  
 색상표 갤러리 단추에 포함 되는지 여부를 지정 합니다.  
  
```  
BOOL IsButtonMode() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`색상표 드롭 다운 메뉴 단추;으로 표시 되 면 `FALSE` 이면 색상표 리본 메뉴에 직접 표시 됩니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="ismenuresizeenabled"></a>CMFCRibbonGallery::IsMenuResizeEnabled  
 메뉴 크기 조정 사용 되는지 여부를 지정 합니다.  
  
```  
BOOL IsMenuResizeEnabled() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`크기 조정 메뉴를 사용할 수 있는; 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="ismenuresizevertical"></a>CMFCRibbonGallery::IsMenuResizeVertical  

  
```  
BOOL IsMenuResizeVertical() const;  
```  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="ismenusidebar"></a>CMFCRibbonGallery::IsMenuSideBar  
 세로 막대 사용 되는지 여부를 지정 합니다.  
  
```  
BOOL IsMenuSideBar() const;  
```  
  
### <a name="return-value"></a>반환 값  
 `TRUE`Office XP 스타일 세로 막대는 팝업 메뉴;의 왼쪽에 그려지는 경우 그렇지 않으면 `FALSE`합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="onafterchangerect"></a>CMFCRibbonGallery::OnAfterChangeRect  

  
```  
virtual void OnAfterChangeRect(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="remarks"></a>설명  
  
##  <a name="ondraw"></a>CMFCRibbonGallery::OnDraw  

  
```  
virtual void OnDraw(CDC* pDC);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
  
### <a name="remarks"></a>설명  
  
##  <a name="ondrawpaletteicon"></a>CMFCRibbonGallery::OnDrawPaletteIcon  
 갤러리 아이콘을 그릴 때 프레임 워크에서 호출 됩니다.  
  
```  
virtual void OnDrawPaletteIcon(
    CDC* pDC,  
    CRect rectIcon,  
    int nIconIndex,  
    CMFCRibbonGalleryIcon* pIcon,  
    COLORREF clrText);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pDC`  
 그리기에 사용 되는 장치 컨텍스트에 대 한 포인터입니다.  
  
 [in] `rectIcon`  
 그릴 아이콘의 경계 사각형을 지정 합니다.  
  
 [in] `nIconIndex`  
 그릴 아이콘의 갤러리 아이콘의 이미지 목록에서 0부터 시작 하는 인덱스를 지정 합니다.  
  
 [in] `pIcon`  
 그리고 있는 아이콘에 대 한 포인터입니다.  
  
 [in] `clrText`  
 그릴 항목 텍스트의 색을 지정 합니다.  
  
### <a name="remarks"></a>설명  
 리본 갤러리의 모양을 사용자 지정 하는 파생된 클래스에서이 메서드를 재정의할 수 있습니다.  
  
##  <a name="onenable"></a>CMFCRibbonGallery::OnEnable  

  
```  
virtual void OnEnable(BOOL bEnable);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bEnable`  
  
### <a name="remarks"></a>설명  
  
##  <a name="onrtlchanged"></a>CMFCRibbonGallery::OnRTLChanged  

  
```  
virtual void OnRTLChanged(BOOL bIsRTL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bIsRTL`  
  
### <a name="remarks"></a>설명  
  
##  <a name="redrawicons"></a>CMFCRibbonGallery::RedrawIcons  
 갤러리를 다시 그립니다.  
  
```  
void RedrawIcons();
```  
  
### <a name="remarks"></a>설명  
 갤러리 다시 그리게이 함수를 호출 합니다. 런타임 시 갤러리의 내용을 변경 하면이 메서드를 호출 해야 합니다.  
  
##  <a name="removeitemtooltips"></a>CMFCRibbonGallery::RemoveItemToolTips  
 갤러리에 있는 모든 항목에서 도구 설명을 제거합니다.  
  
```  
void RemoveItemToolTips();
```  
  
### <a name="remarks"></a>설명  
  
##  <a name="selectitem"></a>CMFCRibbonGallery::SelectItem  

  
```  
void SelectItem(int nItemIndex);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nItemIndex`  
  
### <a name="remarks"></a>설명  
  
##  <a name="setaccdata"></a>CMFCRibbonGallery::SetACCData  
 리본 갤러리에서 내게 필요한 옵션 데이터를 사용하여 지정된 `CAccessibilityData` 개체를 채웁니다.  
  
```  
virtual BOOL SetACCData(
    CWnd* pParent,   
    CAccessibilityData& data);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `pParent`  
 리본 갤러리 창의 부모 창입니다.  
  
 [out] `data`  
 리본 갤러리에서 내게 필요한 옵션 데이터를 받는 `CAccessibilityData` 개체입니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
 해당 메서드에 성공하면 `TRUE`이고, 그렇지 않으면 `FALSE`입니다.  
  
##  <a name="setbuttonmode"></a>CMFCRibbonGallery::SetButtonMode  
 드롭 다운 단추 또는 리본에서 직접 색상표도 리본 갤러리를 표시할지 여부를 결정 합니다.  
  
```  
void SetButtonMode(BOOL bSet=TRUE);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `bSet`  
 `TRUE`리본 갤러리 드롭 다운 메뉴 단추;으로 표시 하려면 `FALSE` 리본에서 직접 리본 갤러리의 내용을 표시 합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="setgroupname"></a>CMFCRibbonGallery::SetGroupName  
 그룹의 이름을 설정합니다.  
  
```  
void SetGroupName(
    int nGroupIndex,  
    LPCTSTR lpszGroupName);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nGroupIndex`  
 이름이 변경 되 고 있는 그룹에 대 한 0부터 시작 하는 인덱스를 지정 합니다.  
  
 [in] `lpszGroupName`  
 그룹에 대 한 새 이름을 지정합니다.  
  
### <a name="remarks"></a>설명  
 이름이 변경 되는 그룹 추가 되어를 사용 하 여 [CMFCRibbonGallery::AddGroup](#addgroup) 메서드.  
  
##  <a name="seticonsinrow"></a>CMFCRibbonGallery::SetIconsInRow  
 갤러리에서 각 행의 항목 수를 지정합니다.  
  
```  
void SetIconsInRow(int nIconsInRow);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nIconsInRow`  
 갤러리의 각 행에 표시할 항목 수를 지정 합니다.  
  
### <a name="remarks"></a>설명  
 리본 갤러리의 너비를 지정 하려면이 메서드를 사용 합니다.  
  
##  <a name="setitemtooltip"></a>CMFCRibbonGallery::SetItemToolTip  
 갤러리에서 항목에 대 한 도구 설명 텍스트를 설정합니다.  
  
```  
void SetItemToolTip(
    int nItemIndex,  
    LPCTSTR lpszToolTip);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nItemIndex`  
 도구 설명에 연결 하는 색상표 항목의 0부터 시작 하는 인덱스입니다.  
  
 [in] `lpszToolTip`  
 도구 설명에 표시할 텍스트입니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="setpalette"></a>CMFCRibbonGallery::SetPalette  
 리본 갤러리를 색상표를 연결합니다.  
  
```  
void SetPalette(CMFCToolBarImages& imagesPalette);

 
void SetPalette(
    UINT uiImagesPaletteResID,  
    int cxPaletteImage);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `imagesPalette`  
 갤러리에 표시할 아이콘이 포함 된 이미지 목록을 지정 합니다.  
  
 [in] `uiImagesPaletteResID`  
 갤러리에 표시할 아이콘을 포함 하는 이미지 목록의 리소스 ID를 지정 합니다.  
  
 [in] `cxPaletteImage`  
 갤러리에서 이미지를 픽셀 단위로 너비를 지정 합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="setpaletteid"></a>CMFCRibbonGallery::SetPaletteID  
 전송 된 명령 ID 정의 **WM_COMMAND** 메시지는 사용자가 갤러리 항목을 선택 합니다.  
  
```  
void SetPaletteID(UINT nID);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `nID`  
 전송 된 명령 ID를 지정는 **WM_COMMAND** 메시지는 사용자가 갤러리 항목을 선택 합니다.  
  
### <a name="remarks"></a>설명  
 사용자가 선택한 갤러리에서 특정 항목을 확인 하려면 호출는 [CMFCRibbonGallery::GetLastSelectedItem](#getlastselecteditem) 정적 메서드입니다.  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCRibbonButton 클래스](../../mfc/reference/cmfcribbonbutton-class.md)   
 [CMFCRibbonGalleryMenuButton 클래스](../../mfc/reference/cmfcribbongallerymenubutton-class.md)
