---
title: 编译器错误 C3387 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3387
dev_langs:
- C++
helpviewer_keywords:
- C3387
ms.assetid: c54d9925-ed14-4976-b8db-e8d4dc84e536
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 5469088b6707faa31e1d49157dcbc9991ffb7060
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3387"></a>编译器错误 C3387
member: __declspec （dllexport) /\__declspec(dllimport) 不能应用于成员托管或 WinRT 类型  
  
 `dllimport`和[dllexport](../../cpp/dllexport-dllimport.md) `__declspec`修饰符都不是有效的托管成员或 Windows 运行时类型。  
  
 下面的示例将生成 C3387，并演示如何修复此错误：  
  
```  
// C3387a.cpp  
// compile with: /clr /c  
ref class X2 {  
   void __declspec(dllexport) mf() {   // C3387  
   // try the following line instead  
   // void mf() {  
   }  
};  
```