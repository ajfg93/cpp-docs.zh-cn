---
title: _com_error::_com_error |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- _com_error::_com_error
dev_langs:
- C++
helpviewer_keywords:
- _com_error method [C++]
ms.assetid: 0a69e46c-caab-49ef-b091-eee401253ce6
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 7d26239f6edf98e90f9d4d773d654025da410a97
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="comerrorcomerror"></a>_com_error::_com_error
**Microsoft 专用**  
  
 构造 `_com_error` 对象。  
  
## <a name="syntax"></a>语法  
  
```  
  
      _com_error(  
   HRESULT hr,  
   IErrorInfo* perrinfo = NULL,  
   bool fAddRef=false  
) throw( );  
_com_error(  
   const _com_error& that   
) throw( );  
```  
  
#### <a name="parameters"></a>参数  
 `hr`  
 `HRESULT` 信息。  
  
 `perrinfo`  
 **IErrorInfo**对象。  
  
 **bool fAddRef = false**  
 导致构造函数在非 null 上调用 AddRef **IErrorInfo**接口。 这可以在接口的所有权传入 `_com_error` 对象的常见情况下提供正确的引用计数，例如：  
  
```  
throw _com_error(hr, perrinfo);  
```  
  
 如果你不希望你的代码将所有权转交到`_com_error`对象，与`AddRef`进行偏移需要**版本**中`_com_error`析构函数，按以下方式构造对象：  
  
```  
_com_error err(hr, perrinfo, true);  
```  
  
 `that`  
 一个现有的 `_com_error` 对象。  
  
## <a name="remarks"></a>备注  
 第一个构造函数创建一个新对象`HRESULT`和可选**IErrorInfo**对象。 第二个构造函数创建现有 `_com_error` 对象的副本。  
  
 **结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
 [_com_error 类](../cpp/com-error-class.md)