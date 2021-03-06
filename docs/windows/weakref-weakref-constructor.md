---
title: 'Weakref:: Weakref 构造函数 |Microsoft 文档'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-windows
ms.topic: reference
f1_keywords:
- client/Microsoft::WRL::WeakRef::WeakRef
dev_langs:
- C++
helpviewer_keywords:
- WeakRef, constructor
ms.assetid: 589f87e0-8dcc-4e82-aab2-f2f66f1ec47c
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- uwp
ms.openlocfilehash: ae70dabdd86fedf82c26c0c7d9a09d842e2310e7
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="weakrefweakref-constructor"></a>WeakRef::WeakRef 构造函数
初始化 WeakRef 类的新实例。  
  
## <a name="syntax"></a>语法  
  
```  
WeakRef();  
WeakRef(  
   decltype(__nullptr)  
);  
  
WeakRef(  
   _In_opt_ IWeakReference* ptr  
);  
  
WeakRef(  
   const ComPtr<IWeakReference>& ptr  
);  
  
WeakRef(  
   const WeakRef& ptr  
);  
  
WeakRef(  
   _Inout_ WeakRef&& ptr  
);  
```  
  
#### <a name="parameters"></a>参数  
 `ptr`  
 指针、 引用或对初始化当前 WeakRef 对象的现有对象的右值引用。  
  
## <a name="remarks"></a>备注  
 第一个构造函数初始化一个空的 WeakRef 对象。 第二个构造函数初始化 WeakRef 对象从指针到 IWeakReference 接口。 第三个构造函数初始化 WeakRef 对象的引用 ComPtr\<IWeakReference > 对象。 第四个和第五个构造函数初始化 WeakRef 对象的另一个 WeakRef 对象。  
  
## <a name="requirements"></a>要求  
 **标头：** client.h  
  
 **命名空间：** Microsoft::WRL  
  
## <a name="see-also"></a>请参阅  
 [WeakRef 类](../windows/weakref-class.md)