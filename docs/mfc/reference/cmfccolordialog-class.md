---
title: "CMFCColorDialog 클래스 | Microsoft Docs"
ms.custom: 
ms.date: 11/04/2016
ms.reviewer: 
ms.suite: 
ms.technology: cpp-windows
ms.tgt_pltfrm: 
ms.topic: reference
f1_keywords:
- CMFCColorDialog
- AFXCOLORDIALOG/CMFCColorDialog
- AFXCOLORDIALOG/CMFCColorDialog::CMFCColorDialog
- AFXCOLORDIALOG/CMFCColorDialog::GetColor
- AFXCOLORDIALOG/CMFCColorDialog::GetPalette
- AFXCOLORDIALOG/CMFCColorDialog::RebuildPalette
- AFXCOLORDIALOG/CMFCColorDialog::SetCurrentColor
- AFXCOLORDIALOG/CMFCColorDialog::SetNewColor
- AFXCOLORDIALOG/CMFCColorDialog::SetPageOne
- AFXCOLORDIALOG/CMFCColorDialog::SetPageTwo
dev_langs: C++
helpviewer_keywords:
- CMFCColorDialog [MFC], CMFCColorDialog
- CMFCColorDialog [MFC], GetColor
- CMFCColorDialog [MFC], GetPalette
- CMFCColorDialog [MFC], RebuildPalette
- CMFCColorDialog [MFC], SetCurrentColor
- CMFCColorDialog [MFC], SetNewColor
- CMFCColorDialog [MFC], SetPageOne
- CMFCColorDialog [MFC], SetPageTwo
ms.assetid: 235bbbbc-a3b1-46e0-801b-fb55093ec579
caps.latest.revision: "30"
author: mikeblome
ms.author: mblome
manager: ghogen
ms.workload: cplusplus
ms.openlocfilehash: bc8b547b72a7094bb6337e9e412f8548a48820f8
ms.sourcegitcommit: 8fa8fdf0fbb4f57950f1e8f4f9b81b4d39ec7d7a
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/21/2017
---
# <a name="cmfccolordialog-class"></a>CMFCColorDialog 클래스
`CMFCColorDialog` 색 선택 대화 상자 클래스를 나타냅니다.  
  
## <a name="syntax"></a>구문  
  
```  
class CMFCColorDialog : public CDialogEx  
```  
  
## <a name="members"></a>멤버  
  
### <a name="public-constructors"></a>Public 생성자  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCColorDialog::CMFCColorDialog](#cmfccolordialog)|`CMFCColorDialog` 개체를 생성합니다.|  
|`CMFCColorDialog::~CMFCColorDialog`|소멸자|  
  
### <a name="public-methods"></a>Public 메서드  
  
|이름|설명|  
|----------|-----------------|  
|[CMFCColorDialog::GetColor](#getcolor)|현재 선택 된 색을 반환합니다.|  
|[CMFCColorDialog::GetPalette](#getpalette)|색의 팔레트를 반환합니다.|  
|`CMFCColorDialog::PreTranslateMessage`|창 메시지를 변환 하 여 디스패치 되기 전에 [TranslateMessage](http://msdn.microsoft.com/library/windows/desktop/ms644955) 및 [DispatchMessage](http://msdn.microsoft.com/library/windows/desktop/ms644934) Windows 함수입니다. 구문 및 자세한 정보에 대 한 참조 [cwnd:: Pretranslatemessage](../../mfc/reference/cwnd-class.md#pretranslatemessage)합니다. (`CDialogEx::PreTranslateMessage`를 재정의합니다.)|  
|[CMFCColorDialog::RebuildPalette](#rebuildpalette)|시스템 표에서 색상표를 파생 시킵니다.|  
|[CMFCColorDialog::SetCurrentColor](#setcurrentcolor)|현재 선택 된 색을 설정합니다.|  
|[CMFCColorDialog::SetNewColor](#setnewcolor)|가장 지정된 RGB 값에 해당 하는 색을 설정합니다.|  
|[CMFCColorDialog::SetPageOne](#setpageone)|첫 번째 속성 페이지에 대 한 RGB 값을 선택합니다.|  
|[CMFCColorDialog::SetPageTwo](#setpagetwo)|두 번째 속성 페이지에 대 한 RGB 값을 선택합니다.|  
  
### <a name="protected-data-members"></a>보호된 데이터 멤버  
  
|name|설명|  
|----------|-----------------|  
|`m_bIsMyPalette`|`TRUE`색 선택 대화 상자는 자체 색상표를 사용 하는 경우 또는 `FALSE` 대화 상자에 지정 된 색상표를 사용 하는 경우는 `CMFCColorDialog` 생성자입니다.|  
|`m_bPickerMode`|`TRUE`사용자 선택 대화 상자;에서 색을 선택 하는 동안 그렇지 않으면 `FALSE`합니다.|  
|`m_btnColorSelect`|사용자가 선택한 색 단추입니다.|  
|`m_CurrentColor`|현재 선택 된 색입니다.|  
|`m_hcurPicker`|색을 선택 하는 데 사용 되는 커서입니다.|  
|`m_NewColor`|잠재 선택한 색을 영구적으로 선택 하거나 원래 색으로 되돌릴 수 있습니다.|  
|`m_pColourSheetOne`|색 선택 속성 시트의 첫 번째 속성 페이지에 대 한 포인터입니다.|  
|`m_pColourSheetTwo`|색 선택 속성 시트의 속성 페이지에 대 한 포인터입니다.|  
|`m_pPalette`|현재 논리 팔레트입니다.|  
|`m_pPropSheet`|색 선택 대화 상자에 대 한 속성 시트에 대 한 포인터입니다.|  
|`m_wndColors`|색 선택 control 개체입니다.|  
|`m_wndStaticPlaceHolder`|색 선택 속성 시트에 대 한 자리 표시자 인 정적 컨트롤입니다.|  
  
## <a name="remarks"></a>설명  
 색 선택 대화 상자는 두 개의 페이지와 속성 시트도 표시 됩니다. 첫 번째 페이지에서 시스템 팔레트;에서 표준 색 선택 두 번째 페이지에서 사용자 지정 색을 선택 합니다.  
  
 생성할 수 있습니다는 `CMFCColorDialog` 스택에 개체와 호출 후 `DoModal`, 초기 색상에 대 한 매개 변수로 전달는 `CMFCColorDialog` 생성자입니다. 색 선택 대화 상자는 다음 여러 개 만들어 [CMFCColorPickerCtrl 클래스](../../mfc/reference/cmfccolorpickerctrl-class.md) 각 색상표를 처리 하는 개체입니다.  
  
## <a name="inheritance-hierarchy"></a>상속 계층  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 [CDialog](../../mfc/reference/cdialog-class.md)  
  
 [CDialogEx](../../mfc/reference/cdialogex-class.md)  
  
 [CMFCColorDialog](../../mfc/reference/cmfccolordialog-class.md)  
  
## <a name="example"></a>예  
 다음 예제에서는 색 대화 상자에서 다양 한 메서드를 사용 하 여 구성 하는 방법의 `CMFCColorDialog` 클래스입니다. 이 예제에서는 현재 개체와의 대화 상자에서 새 색을 설정 하는 방법과 색 대화의 두 속성 페이지에서 선택한 색의 빨강, 녹색 및 파랑 구성 요소를 설정 하는 방법을 보여 줍니다. 이 예제는의 일부는 [새 컨트롤 샘플](../../visual-cpp-samples.md)합니다.  
  
 [!code-cpp[NVC_MFC_NewControls#3](../../mfc/reference/codesnippet/cpp/cmfccolordialog-class_1.cpp)]  
  
## <a name="requirements"></a>요구 사항  
 **헤더:** afxcolordialog.h  
  
##  <a name="cmfccolordialog"></a>CMFCColorDialog::CMFCColorDialog  
 `CMFCColorDialog` 개체를 생성합니다.  
  
```  
CMFCColorDialog(
    COLORREF clrInit=0,  
    DWORD dwFlags=0,  
    CWnd* pParentWnd=NULL,  
    HPALETTE hPal=NULL);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `clrInit`  
 기본 색 선택 합니다. 지정은 값이 없으면 기본값이 RGB(0,0,0) (검정)입니다.  
  
 [in] `dwFlags`  
 (예약 됨.)  
  
 [in] `pParentWnd`  
 대화 상자의 부모 또는 소유자 창에 대 한 포인터입니다.  
  
 [in] `hPal`  
 색상표에 대 한 핸들입니다.  
  
### <a name="return-value"></a>반환 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="getcolor"></a>CMFCColorDialog::GetColor  
 색 대화 상자에서 사용자가 선택한 색을 검색 합니다.  
  
```  
COLORREF GetColor() const;  
```  
  
### <a name="return-value"></a>반환 값  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) 색 대화 상자에서 선택한 색의 RGB 정보를 포함 하는 값입니다.  
  
### <a name="remarks"></a>설명  
 이 함수를 호출한 다음 호출에서 `DoModal` 메서드.  
  
##  <a name="getpalette"></a>CMFCColorDialog::GetPalette  
 현재 색 대화 상자에서 사용할 수 있는 색상표를 검색 합니다.  
  
```  
CPalette* GetPalette() const;  
```  
  
### <a name="return-value"></a>반환 값  
 에 대 한 포인터는 `CPalette` 에 지정 된 개체는 `CMFCColorDialog` 생성자입니다.  
  
### <a name="remarks"></a>설명  
 색상표에 사용자가 선택할 수는 색을 지정 합니다.  
  
##  <a name="rebuildpalette"></a>CMFCColorDialog::RebuildPalette  
 시스템 표에서 색상표를 파생 시킵니다.  
  
```  
void RebuildPalette();
```  
  
##  <a name="setcurrentcolor"></a>CMFCColorDialog::SetCurrentColor  
 대화 상자의 현재 색을 설정합니다.  
  
```  
void SetCurrentColor(COLORREF rgb);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rgb`  
 RGB 색상 값  
  
### <a name="remarks"></a>설명  
  
##  <a name="setnewcolor"></a>CMFCColorDialog::SetNewColor  
 현재 색 가장 유사한 현재 색상표에서 색을 설정 합니다.  
  
```  
void SetNewColor(COLORREF rgb);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `rgb`  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449) RGB 색을 지정 하는 합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="setpageone"></a>CMFCColorDialog::SetPageOne  
 색 대화의 첫 번째 속성 페이지에서 선택한 색의 빨강, 녹색 및 파랑 구성 요소를 명시적으로 지정합니다.  
  
```  
void SetPageOne(
    BYTE R,  
    BYTE G,  
    BYTE B);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `R`  
 RGB 값의 빨간색 구성 요소를 지정합니다.  
  
 [in] `G`  
 RGB 값의 녹색 구성 요소를 지정합니다.  
  
 [in] `B`  
 RGB 값의 파란색 구성 요소를 지정합니다.  
  
### <a name="remarks"></a>설명  
  
##  <a name="setpagetwo"></a>CMFCColorDialog::SetPageTwo  
 색 대화의 두 번째 속성 페이지에서 선택한 색의 빨강, 녹색 및 파랑 구성 요소를 명시적으로 지정합니다.  
  
```  
void SetPageTwo(
    BYTE R,  
    BYTE G,  
    BYTE B);
```  
  
### <a name="parameters"></a>매개 변수  
 [in] `R`  
 RGB 값의 빨간색 구성 요소를 지정합니다.  
  
 [in] `G`  
 RGB 값의 녹색 구성 요소를 지정합니다.  
  
 [in] `B`  
 RGB 값의 파란색 구성 요소를 지정합니다.  
  
### <a name="remarks"></a>설명  
  
## <a name="see-also"></a>참고 항목  
 [계층 구조 차트](../../mfc/hierarchy-chart.md)   
 [클래스](../../mfc/reference/mfc-classes.md)   
 [CMFCColorPickerCtrl 클래스](../../mfc/reference/cmfccolorpickerctrl-class.md)
