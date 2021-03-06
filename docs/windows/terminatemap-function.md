---
title: TerminateMap 函数 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- module/Microsoft::WRL::Details::TerminateMap
dev_langs:
- C++
helpviewer_keywords:
- TerminateMap function
ms.assetid: 1c314a61-da5d-49bb-ac44-c34ee3c23b66
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: b4787fec0a6b4b9f55c500b66786372945d9a523
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="terminatemap-function"></a>TerminateMap 函数
支持 WRL 基础结构，不应在代码中直接使用。  
  
## <a name="syntax"></a>语法  
  
```  
inline bool TerminateMap(  
   _In_ ModuleBase *module,   
   _In_opt_z_ const wchar_t *serverName,   
    bool forceTerminate) throw()  
```  
  
## <a name="parameters"></a>参数  
 `module`  
 A[模块](../windows/module-class.md)。  
  
 `serverName`  
 由参数指定的模块中的类工厂的子集名称`module`。  
  
 `forceTerminate`  
 `true` 若要终止类而不考虑它们的工厂处于活动状态;`false`不终止的类工厂，如果任何工厂处于活动状态。  
  
## <a name="return-value"></a>返回值  
 `true` 如果所有类工厂均已都终止;否则为`false`。  
  
## <a name="remarks"></a>备注  
 关闭指定模块中的类工厂。  
  
## <a name="requirements"></a>要求  
 **标头：** module.h  
  
 **Namespace:** Microsoft::WRL::Details  
  
## <a name="see-also"></a>请参阅  
 [Microsoft::WRL::Details 命名空间](../windows/microsoft-wrl-details-namespace.md)