---
title: CToolTipCtrl 类 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
f1_keywords:
- CToolTipCtrl
- AFXCMN/CToolTipCtrl
- AFXCMN/CToolTipCtrl::CToolTipCtrl
- AFXCMN/CToolTipCtrl::Activate
- AFXCMN/CToolTipCtrl::AddTool
- AFXCMN/CToolTipCtrl::AdjustRect
- AFXCMN/CToolTipCtrl::Create
- AFXCMN/CToolTipCtrl::CreateEx
- AFXCMN/CToolTipCtrl::DelTool
- AFXCMN/CToolTipCtrl::GetBubbleSize
- AFXCMN/CToolTipCtrl::GetCurrentTool
- AFXCMN/CToolTipCtrl::GetDelayTime
- AFXCMN/CToolTipCtrl::GetMargin
- AFXCMN/CToolTipCtrl::GetMaxTipWidth
- AFXCMN/CToolTipCtrl::GetText
- AFXCMN/CToolTipCtrl::GetTipBkColor
- AFXCMN/CToolTipCtrl::GetTipTextColor
- AFXCMN/CToolTipCtrl::GetTitle
- AFXCMN/CToolTipCtrl::GetToolCount
- AFXCMN/CToolTipCtrl::GetToolInfo
- AFXCMN/CToolTipCtrl::HitTest
- AFXCMN/CToolTipCtrl::Pop
- AFXCMN/CToolTipCtrl::Popup
- AFXCMN/CToolTipCtrl::RelayEvent
- AFXCMN/CToolTipCtrl::SetDelayTime
- AFXCMN/CToolTipCtrl::SetMargin
- AFXCMN/CToolTipCtrl::SetMaxTipWidth
- AFXCMN/CToolTipCtrl::SetTipBkColor
- AFXCMN/CToolTipCtrl::SetTipTextColor
- AFXCMN/CToolTipCtrl::SetTitle
- AFXCMN/CToolTipCtrl::SetToolInfo
- AFXCMN/CToolTipCtrl::SetToolRect
- AFXCMN/CToolTipCtrl::SetWindowTheme
- AFXCMN/CToolTipCtrl::Update
- AFXCMN/CToolTipCtrl::UpdateTipText
dev_langs:
- C++
helpviewer_keywords:
- CToolTipCtrl [MFC], CToolTipCtrl
- CToolTipCtrl [MFC], Activate
- CToolTipCtrl [MFC], AddTool
- CToolTipCtrl [MFC], AdjustRect
- CToolTipCtrl [MFC], Create
- CToolTipCtrl [MFC], CreateEx
- CToolTipCtrl [MFC], DelTool
- CToolTipCtrl [MFC], GetBubbleSize
- CToolTipCtrl [MFC], GetCurrentTool
- CToolTipCtrl [MFC], GetDelayTime
- CToolTipCtrl [MFC], GetMargin
- CToolTipCtrl [MFC], GetMaxTipWidth
- CToolTipCtrl [MFC], GetText
- CToolTipCtrl [MFC], GetTipBkColor
- CToolTipCtrl [MFC], GetTipTextColor
- CToolTipCtrl [MFC], GetTitle
- CToolTipCtrl [MFC], GetToolCount
- CToolTipCtrl [MFC], GetToolInfo
- CToolTipCtrl [MFC], HitTest
- CToolTipCtrl [MFC], Pop
- CToolTipCtrl [MFC], Popup
- CToolTipCtrl [MFC], RelayEvent
- CToolTipCtrl [MFC], SetDelayTime
- CToolTipCtrl [MFC], SetMargin
- CToolTipCtrl [MFC], SetMaxTipWidth
- CToolTipCtrl [MFC], SetTipBkColor
- CToolTipCtrl [MFC], SetTipTextColor
- CToolTipCtrl [MFC], SetTitle
- CToolTipCtrl [MFC], SetToolInfo
- CToolTipCtrl [MFC], SetToolRect
- CToolTipCtrl [MFC], SetWindowTheme
- CToolTipCtrl [MFC], Update
- CToolTipCtrl [MFC], UpdateTipText
ms.assetid: 8973f70c-b73a-46c7-908d-758f364b9a97
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: de230a82adaaafc149d2ed5a762977205c798b03
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="ctooltipctrl-class"></a>CToolTipCtrl Class
封装“工具提示控件”功能，此控件是一个小型弹出窗口，显示说明应用程序中工具用途的单行文本。  
  
## <a name="syntax"></a>语法  
  
```  
class CToolTipCtrl : public CWnd  
```  
  
## <a name="members"></a>成员  
  
### <a name="public-constructors"></a>公共构造函数  
  
|名称|描述|  
|----------|-----------------|  
|[CToolTipCtrl::CToolTipCtrl](#ctooltipctrl)|构造 `CToolTipCtrl` 对象。|  
  
### <a name="public-methods"></a>公共方法  
  
|名称|描述|  
|----------|-----------------|  
|[CToolTipCtrl::Activate](#activate)|激活和停用工具提示控件。|  
|[CToolTipCtrl::AddTool](#addtool)|使用工具提示控件注册一个工具。|  
|[CToolTipCtrl::AdjustRect](#adjustrect)|矩形和其窗口矩形，将显示工具提示控件的文本之间的转换。|  
|[CToolTipCtrl::Create](#create)|创建工具提示控件并将其附加到`CToolTipCtrl`对象。|  
|[CToolTipCtrl::CreateEx](#createex)|与指定的 Windows 扩展样式创建工具提示控件并将其附加到`CToolTipCtrl`对象。|  
|[CToolTipCtrl::DelTool](#deltool)|从工具提示控件中移除一个工具。|  
|[CToolTipCtrl::GetBubbleSize](#getbubblesize)|检索工具提示的大小。|  
|[CToolTipCtrl::GetCurrentTool](#getcurrenttool)|检索信息，例如大小、 位置和文本，当前的工具提示控件显示的工具提示窗口。|  
|[CToolTipCtrl::GetDelayTime](#getdelaytime)|检索初始、 弹出和重新显示持续时间的当前设置为一个工具提示控件。|  
|[CToolTipCtrl::GetMargin](#getmargin)|检索上、 左侧、 下，和设置工具提示窗口的右边距。|  
|[CToolTipCtrl::GetMaxTipWidth](#getmaxtipwidth)|检索有关工具提示窗口的最大宽度。|  
|[CToolTipCtrl::GetText](#gettext)|检索工具提示控件可为一种工具维护的文本。|  
|[CToolTipCtrl::GetTipBkColor](#gettipbkcolor)|检索工具提示窗口中的背景色。|  
|[CToolTipCtrl::GetTipTextColor](#gettiptextcolor)|检索工具提示窗口中的文本颜色。|  
|[CToolTipCtrl::GetTitle](#gettitle)|检索当前的工具提示控件的标题。|  
|[CToolTipCtrl::GetToolCount](#gettoolcount)|检索由工具提示控件维护的工具计数。|  
|[CToolTipCtrl::GetToolInfo](#gettoolinfo)|检索工具提示控件维护有关工具的信息。|  
|[CToolTipCtrl::HitTest](#hittest)|测试点以确定它是否位于给定工具的边框内。 如果是这样，则检索有关工具的信息。|  
|[CToolTipCtrl::Pop](#pop)|从视图中删除显示的工具提示窗口。|  
|[CToolTipCtrl::Popup](#popup)|导致当前的工具提示控件，显示在最后一个鼠标消息的坐标。|  
|[Ctooltipctrl:: Relayevent](#relayevent)|将鼠标消息传递给处理工具提示控件。|  
|[CToolTipCtrl::SetDelayTime](#setdelaytime)|设置初始、 弹出窗口中，并重新显示工具提示控件的持续时间。|  
|[CToolTipCtrl::SetMargin](#setmargin)|设置顶端、 左、 下、 和工具提示窗口的右边距。|  
|[CToolTipCtrl::SetMaxTipWidth](#setmaxtipwidth)|设置工具提示窗口的最大宽度。|  
|[CToolTipCtrl::SetTipBkColor](#settipbkcolor)|工具提示窗口中设置的背景色。|  
|[CToolTipCtrl::SetTipTextColor](#settiptextcolor)|工具提示窗口中设置的文本颜色。|  
|[CToolTipCtrl::SetTitle](#settitle)|将一个标准的图标和标题字符串添加到工具提示。|  
|[CToolTipCtrl::SetToolInfo](#settoolinfo)|设置工具提示维护的工具的信息。|  
|[CToolTipCtrl::SetToolRect](#settoolrect)|设置工具的新边框。|  
|[CToolTipCtrl::SetWindowTheme](#setwindowtheme)|设置工具提示窗口的视觉样式。|  
|[CToolTipCtrl::Update](#update)|强制当前的工具要重新绘制。|  
|[CToolTipCtrl::UpdateTipText](#updatetiptext)|设置工具提示文本的工具。|  
  
## <a name="remarks"></a>备注  
 "工具"是一个窗口，如子窗口或控件或一个窗口的客户端区域中，应用程序定义的矩形区域。 工具提示在大多数时间都是隐藏的，它仅在用户将光标置于工具上并在其上停留约半秒时间时显示。 工具提示显示在光标附近，并且在用户单击鼠标按钮，或将关闭该工具光标移动时消失。  
  
 `CToolTipCtrl` 提供一种功能的初始时间和持续时间的工具提示中，控件周围的工具提示文本、 本身，工具提示窗口的宽度和工具提示的背景和文本颜色的边距。 一个工具提示控件可以提供多个工具的信息。  
  
 `CToolTipCtrl` 类提供了 Windows 公共工具提示控件的功能。 此控件 (因此`CToolTipCtrl`类) 仅适用于在 Windows 95/98 和 Windows NT 版本 3.51 下运行的程序和更高版本。  
  
 有关启用工具提示的详细信息，请参阅[Windows 中的工具提示不派生自 CFrameWnd](../../mfc/tool-tips-in-windows-not-derived-from-cframewnd.md)。  
  
 有关详细信息使用`CToolTipCtrl`，请参阅[控件](../../mfc/controls-mfc.md)和[使用 CToolTipCtrl](../../mfc/using-ctooltipctrl.md)。  
  
## <a name="inheritance-hierarchy"></a>继承层次结构  
 [CObject](../../mfc/reference/cobject-class.md)  
  
 [CCmdTarget](../../mfc/reference/ccmdtarget-class.md)  
  
 [CWnd](../../mfc/reference/cwnd-class.md)  
  
 `CToolTipCtrl`  
  
## <a name="requirements"></a>要求  
 **标头：** afxcmn.h  
  
##  <a name="activate"></a>  CToolTipCtrl::Activate  
 调用此函数可激活或停用工具提示控件。  
  
```  
void Activate(BOOL bActivate);
```  
  
### <a name="parameters"></a>参数  
 `bActivate`  
 指定是否要激活或停用工具提示控件。  
  
### <a name="remarks"></a>备注  
 如果`bActivate`是**TRUE**，激活控件; 如果**FALSE**，它将停用。  
  
 工具提示控件处于活动状态，工具提示信息出现光标位于与该控件; 注册的工具上时非活动状态时，工具提示信息不即使不会出现，光标位于工具上时。  
  
### <a name="example"></a>示例  
  请参阅示例[CPropertySheet::GetTabControl](../../mfc/reference/cpropertysheet-class.md#gettabcontrol)。  
  
##  <a name="addtool"></a>  CToolTipCtrl::AddTool  
 使用工具提示控件注册一个工具。  
  
```  
BOOL AddTool(
    CWnd* pWnd,  
    UINT nIDText,  
    LPCRECT lpRectTool = NULL,  
    UINT_PTR nIDTool = 0);

 
BOOL AddTool(
    CWnd* pWnd,  
    LPCTSTR lpszText = LPSTR_TEXTCALLBACK,  
    LPCRECT lpRectTool = NULL,  
    UINT_PTR nIDTool = 0);
```  
  
### <a name="parameters"></a>参数  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `nIDText`  
 包含该工具的文本的字符串资源的 ID。  
  
 *lpRectTool*  
 指向[RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)结构，它包含坐标，该工具的边框。 相对于由标识的窗口的工作区的左上角的坐标为`pWnd`。  
  
 `nIDTool`  
 该工具的 ID。  
  
 `lpszText`  
 指向该工具的文本指针。 如果此参数包含值**LPSTR_TEXTCALLBACK**， **TTN_NEEDTEXT**通知消息将转到窗口的父级，`pWnd`指向。  
  
### <a name="return-value"></a>返回值  
 如果成功，则不为 0；否则为 0。  
  
### <a name="remarks"></a>备注  
 **LpRectTool**和**nIDTool**参数都必须有效，或者如果**lpRectTool**为 NULL， **nIDTool**必须为 0。  
  
 工具提示控件可以与多个工具相关联。 调用此函数可与该工具提示控件注册工具，以便当光标位于工具上时显示工具提示中存储的信息。  
  
> [!NOTE]
>  你不能将工具提示设置为静态控件使用`AddTool`。  
  
### <a name="example"></a>示例  
  请参阅示例[CPropertySheet::GetTabControl](../../mfc/reference/cpropertysheet-class.md#gettabcontrol)。  
  
##  <a name="adjustrect"></a>  CToolTipCtrl::AdjustRect  
 矩形和其窗口矩形，将显示工具提示控件的文本之间的转换。  
  
```  
BOOL AdjustRect(
    LPRECT lprc,  
    BOOL bLarger = TRUE);
```  
  
### <a name="parameters"></a>参数  
 `lprc`  
 指向[RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)保存工具提示窗口矩形或文本显示矩形的结构。  
  
 `bLarger`  
 如果**TRUE**，`lprc`用于指定文本显示矩形，并接收相应的窗口矩形。 如果**FALSE**，`lprc`用于指定窗口矩形，并接收对应的文本显示矩形。  
  
### <a name="return-value"></a>返回值  
 如果成功地调整矩形; 则为非 0否则为 0。  
  
### <a name="remarks"></a>备注  
 此成员函数计算从其窗口矩形或显示指定的文本显示矩形所需的工具提示窗口矩形的工具提示控件的文本显示矩形。  
  
 此成员函数实现的 Win32 消息行为[TTM_ADJUSTRECT](http://msdn.microsoft.com/library/windows/desktop/bb760352)，如 Windows SDK 中所述。  
  
##  <a name="create"></a>  CToolTipCtrl::Create  
 创建工具提示控件并将其附加到`CToolTipCtrl`对象。  
  
```  
virtual BOOL Create(CWnd* pParentWnd, DWORD dwStyle = 0);
```  
  
### <a name="parameters"></a>参数  
 `pParentWnd`  
 通常指定工具提示控件的父窗口`CDialog`。 它不能**NULL**。  
  
 `dwStyle`  
 指定工具提示控件的样式。 请参阅**备注**部分以了解更多信息。  
  
### <a name="return-value"></a>返回值  
 非零如果`CToolTipCtrl`对象是已成功创建; 否则为 0。  
  
### <a name="remarks"></a>备注  
 构造`CToolTipCtrl`中两个步骤。 首先，调用的构造函数来构造`CToolTipCtrl`对象，，然后调用**创建**创建工具提示控件并将其附加到`CToolTipCtrl`对象。  
  
 `dwStyle`参数可以是任意组合的[窗口样式](../../mfc/reference/styles-used-by-mfc.md#window-styles)。 此外，工具提示控件具有两个特定类的样式： **TTS_ALWAYSTIP**和**TTS_NOPREFIX**。  
  
|样式|含义|  
|-----------|-------------|  
|**TTS_ALWAYSTIP**|指定当光标位于工具，而不考虑工具提示控件的所有者窗口处于活动状态还是处于非活动状态时，将显示工具提示。 如果不使用此样式，该工具的所有者窗口处于活动状态，但不是在处于非活动状态时，将显示工具提示控件。|  
|**TTS_NOPREFIX**|此样式可防止系统去除号 (&) 从字符串的字符。 如果工具提示控件不具有**TTS_NOPREFIX**样式，系统自动去除 & 字符，以便应用程序以使用相同的字符串，为这两个菜单项和为工具提示控件中的文本。|  
  
 工具提示控件具有`WS_POPUP`和**WS_EX_TOOLWINDOW**窗口样式，不管是否指定它们在创建控件时。  
  
 若要创建具有扩展的窗口样式的工具提示控件，调用[CToolTipCtrl::CreateEx](#createex)而不是**创建**。  
  
### <a name="example"></a>示例  
  请参阅示例[CPropertySheet::GetTabControl](../../mfc/reference/cpropertysheet-class.md#gettabcontrol)。  
  
##  <a name="createex"></a>  CToolTipCtrl::CreateEx  
 创建控件 （子窗口），并将其与关联`CToolTipCtrl`对象。  
  
```  
virtual BOOL CreateEx(
    CWnd* pParentWnd,  
    DWORD dwStyle = 0,  
    DWORD dwStyleEx = 0);
```  
  
### <a name="parameters"></a>参数  
 `pParentWnd`  
 指向控件的父级的窗口的指针。  
  
 `dwStyle`  
 指定工具提示控件的样式。 请参阅**备注**部分[创建](#create)有关详细信息。  
  
 *dwStyleEx*  
 指定要创建的控件的扩展的样式。 扩展窗口样式的列表，请参阅`dwExStyle`参数[CreateWindowEx](http://msdn.microsoft.com/library/windows/desktop/ms632680) Windows SDK 中。  
  
### <a name="return-value"></a>返回值  
 如果成功则为非 0; 否则为 0。  
  
### <a name="remarks"></a>备注  
 使用`CreateEx`而不是**创建**将扩展的窗口样式，指定的 Windows 扩展的样式加**WS_EX_**。  
  
##  <a name="ctooltipctrl"></a>  CToolTipCtrl::CToolTipCtrl  
 构造 `CToolTipCtrl` 对象。  
  
```  
CToolTipCtrl();
```  
  
### <a name="remarks"></a>备注  
 必须调用**创建**后构造对象。  
  
### <a name="example"></a>示例  
 [!code-cpp[NVC_MFCControlLadenDialog#74](../../mfc/codesnippet/cpp/ctooltipctrl-class_1.h)]  
  
##  <a name="deltool"></a>  CToolTipCtrl::DelTool  
 移除指定工具`pWnd`和`nIDTool`从的工具提示控件支持的工具的集合。  
  
```  
void DelTool(
    CWnd* pWnd,  
    UINT_PTR nIDTool = 0);
```  
  
### <a name="parameters"></a>参数  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `nIDTool`  
 该工具的 ID。  
  
##  <a name="getbubblesize"></a>  CToolTipCtrl::GetBubbleSize  
 检索工具提示的大小。  
  
```  
CSize GetBubbleSize(LPTOOLINFO lpToolInfo) const;  
```  
  
### <a name="parameters"></a>参数  
 `lpToolInfo`  
 指向的工具提示的[TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)结构。  
  
### <a name="return-value"></a>返回值  
 工具提示的大小。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_GETBUBBLESIZE](http://msdn.microsoft.com/library/windows/desktop/bb760387)，如 Windows SDK 中所述。  
  
##  <a name="getcurrenttool"></a>  CToolTipCtrl::GetCurrentTool  
 检索信息，例如大小、 位置和文本，当前的工具提示控件显示的工具提示窗口。  
  
```  
BOOL GetCurrentTool(LPTOOLINFO lpToolInfo) const;  
```  
  
### <a name="parameters"></a>参数  
  
|参数|描述|  
|---------------|-----------------|  
|[out] `lpToolInfo`|指向[TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)接收有关当前的工具提示窗口的信息的结构。|  
  
### <a name="return-value"></a>返回值  
 `true` 如果成功，则检索的信息否则为 `false.`  
  
### <a name="remarks"></a>备注  
 此方法可发送[TTM_GETCURRENTTOOL](http://msdn.microsoft.com/library/windows/desktop/bb760389)消息，Windows SDK 中介绍。  
  
### <a name="example"></a>示例  
 下面的代码示例检索有关当前的工具提示窗口的信息。  
  
 [!code-cpp[NVC_MFC_CToolBarCtrl_s1#6](../../mfc/reference/codesnippet/cpp/ctooltipctrl-class_2.cpp)]  
  
##  <a name="getdelaytime"></a>  CToolTipCtrl::GetDelayTime  
 检索初始、 弹出窗口中，并重新显示当前为工具提示控件设置持续时间。  
  
```  
int GetDelayTime(DWORD dwDuration) const;  
```  
  
### <a name="parameters"></a>参数  
 `dwDuration`  
 将检索指定的持续时间值的标志。 此参数可以是以下值之一：  
  
- `TTDT_AUTOPOP` 检索工具提示窗口保持如果指针工具的边框内保持静止时可见的时间长度。  
  
- `TTDT_INITIAL` 检索工具提示窗口出现之前，鼠标指针必须保持静止工具的边框内的时间长度。  
  
- `TTDT_RESHOW` 检索后续工具提示窗口显示指针从一个工具移到另一个所需的时间的长度。  
  
### <a name="return-value"></a>返回值  
 指定的延迟时间 （毫秒）  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_GETDELAYTIME](http://msdn.microsoft.com/library/windows/desktop/bb760390)，如 Windows SDK 中所述。  
  
##  <a name="getmargin"></a>  CToolTipCtrl::GetMargin  
 检索上、 左侧、 下，和设置工具提示窗口的右边距。  
  
```  
void GetMargin(LPRECT lprc) const;  
```  
  
### <a name="parameters"></a>参数  
 `lprc`  
 地址`RECT`将接收边距信息的结构。 成员[RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)结构未定义的边框。 此消息，用于解释结构成员，如下所示：  
  
|成员|表示形式|  
|------------|--------------------|  
|**top**|上边框和工具提示文本，以像素为单位的顶部之间的距离。|  
|**left**|左边的框和左的末尾提示文本，以像素为单位之间的距离。|  
|**bottom**|下边框和底部的提示文本，以像素为单位之间的距离。|  
|**right**|右边框和右端的提示文本，以像素为单位之间的距离。|  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_GETMARGIN](http://msdn.microsoft.com/library/windows/desktop/bb760391)，如 Windows SDK 中所述。  
  
##  <a name="getmaxtipwidth"></a>  CToolTipCtrl::GetMaxTipWidth  
 检索有关工具提示窗口的最大宽度。  
  
```  
int GetMaxTipWidth() const;  
```  
  
### <a name="return-value"></a>返回值  
 工具提示窗口的最大宽度。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_GETMAXTIPWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb760392)，如 Windows SDK 中所述。  
  
##  <a name="gettext"></a>  CToolTipCtrl::GetText  
 检索工具提示控件可为一种工具维护的文本。  
  
```  
void GetText(
    CString& str,  
    CWnd* pWnd,  
    UINT_PTR nIDTool = 0) const;  
```  
  
### <a name="parameters"></a>参数  
 `str`  
 引用`CString`接收工具文本的对象。  
  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `nIDTool`  
 该工具的 ID。  
  
### <a name="remarks"></a>备注  
 `pWnd`和`nIDTool`参数确定的工具。 如果向工具提示控件的以前调用通过以前注册了该工具**CToolTipCtrl::AddTool**，所引用的对象`str`参数分配工具的文本。  
  
##  <a name="gettipbkcolor"></a>  CToolTipCtrl::GetTipBkColor  
 检索工具提示窗口中的背景色。  
  
```  
COLORREF GetTipBkColor() const;  
```  
  
### <a name="return-value"></a>返回值  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)值，该值表示的背景色。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_GETTIPBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760394)，如 Windows SDK 中所述。  
  
##  <a name="gettiptextcolor"></a>  CToolTipCtrl::GetTipTextColor  
 检索工具提示窗口中的文本颜色。  
  
```  
COLORREF GetTipTextColor() const;  
```  
  
### <a name="return-value"></a>返回值  
 A [COLORREF](http://msdn.microsoft.com/library/windows/desktop/dd183449)值，该值表示的文本颜色。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_GETTIPTEXTCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760395)，如 Windows SDK 中所述。  
  
##  <a name="gettitle"></a>  CToolTipCtrl::GetTitle  
 检索当前的工具提示控件的标题。  
  
```  
void GetTitle(PTTGETTITLE pttgt) const;  
```  
  
### <a name="parameters"></a>参数  
  
|参数|描述|  
|---------------|-----------------|  
|[out] `pttgt`|指向[TTGETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760260)结构，其中包含有关工具提示控件的信息。 此方法返回时，`pszTitle`的成员[TTGETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760260)结构指向标题的文本。|  
  
### <a name="remarks"></a>备注  
 此方法可发送[TTM_GETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760396)消息，Windows SDK 中介绍。  
  
##  <a name="gettoolcount"></a>  CToolTipCtrl::GetToolCount  
 检索向工具提示控件注册的工具计数。  
  
```  
int GetToolCount() const;  
```  
  
### <a name="return-value"></a>返回值  
 向工具提示控件注册的工具计数。  
  
##  <a name="gettoolinfo"></a>  CToolTipCtrl::GetToolInfo  
 检索工具提示控件维护有关工具的信息。  
  
```  
BOOL GetToolInfo(
    CToolInfo& ToolInfo,  
    CWnd* pWnd,  
    UINT_PTR nIDTool = 0) const;  
```  
  
### <a name="parameters"></a>参数  
 *ToolInfo*  
 引用`TOOLINFO`接收工具文本的对象。  
  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `nIDTool`  
 该工具的 ID。  
  
### <a name="return-value"></a>返回值  
 如果成功，则不为 0；否则为 0。  
  
### <a name="remarks"></a>备注  
 **Hwnd**和**uId**的成员[TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)结构引用*CToolInfo*确定的工具。 如果已向工具提示控件的以前调用通过注册该工具`AddTool`、`TOOLINFO`有关工具的信息填充结构。  
  
##  <a name="hittest"></a>  CToolTipCtrl::HitTest  
 测试点以确定它是否位于给定工具的边框内，如果是这样，检索有关工具的信息。  
  
```  
BOOL HitTest(
    CWnd* pWnd,  
    CPoint pt,  
    LPTOOLINFO lpToolInfo) const;  
```  
  
### <a name="parameters"></a>参数  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `pt`  
 指向`CPoint`对象，其中包含要测试的点的坐标。  
  
 `lpToolInfo`  
 指向[TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)结构，其中包含有关工具的信息。  
  
### <a name="return-value"></a>返回值  
 如果指定的命中测试信息的点在工具的边框; 则为非 0否则为 0。  
  
### <a name="remarks"></a>备注  
 如果此函数返回一个非零值，该结构的指向`lpToolInfo`填入点位于其矩形中工具的信息。  
  
 `TTHITTESTINFO`结构定义，如下所示：  
  
 `typedef struct _TT_HITTESTINFO { // tthti`  
  
 `HWND hwnd;   // handle of tool or window with tool`  
  
 `POINT pt;    // client coordinates of point to test`  
  
 `TOOLINFO ti; // receives information about the tool`  
  
 `} TTHITTESTINFO, FAR * LPHITTESTINFO;`  
  
 **hwnd**  
 指定工具的句柄。  
  
 **pt**  
 如果点在工具的边界矩形，请指定点的坐标。  
  
 **Ti**  
 有关工具的信息。 有关详细信息`TOOLINFO`结构，请参阅[CToolTipCtrl::GetToolInfo](#gettoolinfo)。  
  
##  <a name="pop"></a>  CToolTipCtrl::Pop  
 从视图中删除显示的工具提示窗口。  
  
```  
void Pop();
```  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_POP](http://msdn.microsoft.com/library/windows/desktop/bb760401)，如 Windows SDK 中所述。  
  
##  <a name="popup"></a>  CToolTipCtrl::Popup  
 导致当前的工具提示控件，显示在最后一个鼠标消息的坐标。  
  
```  
void Popup();
```  
  
### <a name="remarks"></a>备注  
 此方法可发送[TTM_POPUP](http://msdn.microsoft.com/library/windows/desktop/bb760402)消息，Windows SDK 中介绍。  
  
### <a name="example"></a>示例  
 下面的代码示例显示工具提示窗口。  
  
 [!code-cpp[NVC_MFC_CToolBarCtrl_s1#7](../../mfc/reference/codesnippet/cpp/ctooltipctrl-class_3.cpp)]  
  
##  <a name="relayevent"></a>  Ctooltipctrl:: Relayevent  
 将鼠标消息传递给处理工具提示控件。  
  
```  
void RelayEvent(LPMSG lpMsg);
```  
  
### <a name="parameters"></a>参数  
 `lpMsg`  
 指向[消息](http://msdn.microsoft.com/library/windows/desktop/ms644958)包含到中继的消息的结构。  
  
### <a name="remarks"></a>备注  
 工具提示控件处理仅以下消息，将它发送到通过`RelayEvent`:  
  
|WM_LBUTTONDOWN|WM_MOUSEMOVE|  
|---------------------|-------------------|  
|`WM_LBUTTONUP`|`WM_RBUTTONDOWN`|  
|`WM_MBUTTONDOWN`|`WM_RBUTTONUP`|  
|`WM_MBUTTONUP`||  
  
### <a name="example"></a>示例  
  请参阅示例[CPropertySheet::GetTabControl](../../mfc/reference/cpropertysheet-class.md#gettabcontrol)。  
  
##  <a name="setdelaytime"></a>  CToolTipCtrl::SetDelayTime  
 设置工具提示控件的延迟时间。  
  
```  
void SetDelayTime(UINT nDelay);

 
void SetDelayTime(
    DWORD dwDuration,  
    int iTime);
```  
  
### <a name="parameters"></a>参数  
 *nDelay*  
 指定新的延迟时间，以毫秒为单位。  
  
 `dwDuration`  
 将检索指定的持续时间值的标志。 请参阅[CToolTipCtrl::GetDelayTime](#getdelaytime)有关有效值的说明。  
  
 *iTime*  
 指定的延迟时间，以毫秒为单位。  
  
### <a name="remarks"></a>备注  
 延迟时间是时间的之前工具提示窗口出现，光标必须上一个工具中保持长度。 默认延迟时间为 500 毫秒。  
  
##  <a name="setmargin"></a>  CToolTipCtrl::SetMargin  
 设置顶端、 左、 下、 和工具提示窗口的右边距。  
  
```  
void SetMargin(LPRECT lprc);
```  
  
### <a name="parameters"></a>参数  
 `lprc`  
 地址`RECT`结构，其中包含要设置的边距信息。 成员`RECT`结构未定义的边框。 请参阅[CToolTipCtrl::GetMargin](#getmargin)有关边距信息的说明。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_SETMARGIN](http://msdn.microsoft.com/library/windows/desktop/bb760406)，如 Windows SDK 中所述。  
  
##  <a name="setmaxtipwidth"></a>  CToolTipCtrl::SetMaxTipWidth  
 设置工具提示窗口的最大宽度。  
  
```  
int SetMaxTipWidth(int iWidth);
```  
  
### <a name="parameters"></a>参数  
 *iWidth*  
 要设置最大的工具提示窗口宽度。  
  
### <a name="return-value"></a>返回值  
 以前的最大提示宽度。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_SETMAXTIPWIDTH](http://msdn.microsoft.com/library/windows/desktop/bb760408)，如 Windows SDK 中所述。  
  
##  <a name="settipbkcolor"></a>  CToolTipCtrl::SetTipBkColor  
 工具提示窗口中设置的背景色。  
  
```  
void SetTipBkColor(COLORREF clr);
```  
  
### <a name="parameters"></a>参数  
 `clr`  
 新的背景色。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_SETTIPBKCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760411)，如 Windows SDK 中所述。  
  
##  <a name="settiptextcolor"></a>  CToolTipCtrl::SetTipTextColor  
 工具提示窗口中设置的文本颜色。  
  
```  
void SetTipTextColor(COLORREF clr);
```  
  
### <a name="parameters"></a>参数  
 `clr`  
 新的文本颜色。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_SETTIPTEXTCOLOR](http://msdn.microsoft.com/library/windows/desktop/bb760413)，如 Windows SDK 中所述。  
  
##  <a name="settitle"></a>  CToolTipCtrl::SetTitle  
 将一个标准的图标和标题字符串添加到工具提示。  
  
```  
BOOL SetTitle(
    UINT uIcon,  
    LPCTSTR lpstrTitle);
```  
  
### <a name="parameters"></a>参数  
 *uIcon*  
 请参阅*图标*中[TTM_SETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760414) Windows SDK 中。  
  
 *lpstrTitle*  
 为标题字符串的指针。  
  
### <a name="return-value"></a>返回值  
 如果成功，则不为 0；否则为 0。  
  
### <a name="remarks"></a>备注  
 此成员函数实现的 Win32 消息行为[TTM_SETTITLE](http://msdn.microsoft.com/library/windows/desktop/bb760414)，如 Windows SDK 中所述。  
  
##  <a name="settoolinfo"></a>  CToolTipCtrl::SetToolInfo  
 设置工具提示维护的工具的信息。  
  
```  
void SetToolInfo(LPTOOLINFO lpToolInfo);
```  
  
### <a name="parameters"></a>参数  
 `lpToolInfo`  
 指向的指针[TOOLINFO](http://msdn.microsoft.com/library/windows/desktop/bb760256)结构，它指定要设置的信息。  
  
##  <a name="settoolrect"></a>  CToolTipCtrl::SetToolRect  
 设置工具的新边框。  
  
```  
void SetToolRect(
    CWnd* pWnd,  
    UINT_PTR nIDTool,  
    LPCRECT lpRect);
```  
  
### <a name="parameters"></a>参数  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `nIDTool`  
 该工具的 ID。  
  
 `lpRect`  
 指向[RECT](http://msdn.microsoft.com/library/windows/desktop/dd162897)结构，它指定的新边框。  
  
##  <a name="setwindowtheme"></a>  CToolTipCtrl::SetWindowTheme  
 设置工具提示窗口的视觉样式。  
  
```  
HRESULT SetWindowTheme(LPCWSTR pszSubAppName);
```  
  
### <a name="parameters"></a>参数  
 `pszSubAppName`  
 指向包含要设置的视觉样式的 Unicode 字符串的指针。  
  
### <a name="return-value"></a>返回值  
 未使用返回的值。  
  
### <a name="remarks"></a>备注  
 此成员函数模拟的功能[TTM_SETWINDOWTHEME](http://msdn.microsoft.com/library/windows/desktop/bb760418)消息时，Windows SDK 中所述。  
  
##  <a name="update"></a>  CToolTipCtrl::Update  
 强制当前的工具要重新绘制。  
  
```  
void Update();
```  
  
##  <a name="updatetiptext"></a>  CToolTipCtrl::UpdateTipText  
 更新此控件的工具的工具提示文本。  
  
```  
void UpdateTipText(
    LPCTSTR lpszText,  
    CWnd* pWnd,  
    UINT_PTR nIDTool = 0);

 
void UpdateTipText(
    UINT nIDText,  
    CWnd* pWnd,  
    UINT_PTR nIDTool = 0);
```  
  
### <a name="parameters"></a>参数  
 `lpszText`  
 指向该工具的文本指针。  
  
 `pWnd`  
 指向包含该工具窗口的指针。  
  
 `nIDTool`  
 该工具的 ID。  
  
 `nIDText`  
 包含该工具的文本的字符串资源的 ID。  
  
## <a name="see-also"></a>请参阅  
 [CWnd 类](../../mfc/reference/cwnd-class.md)   
 [层次结构图](../../mfc/hierarchy-chart.md)   
 [CToolBar 类](../../mfc/reference/ctoolbar-class.md)
