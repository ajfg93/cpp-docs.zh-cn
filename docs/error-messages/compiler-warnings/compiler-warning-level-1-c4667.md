---
title: 编译器警告 （等级 1） C4667 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C4667
dev_langs:
- C++
helpviewer_keywords:
- C4667
ms.assetid: 5d2b7fe0-4f0e-4cd6-b432-ca02c3d194ab
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: af88dc89fce0d95ec252a9cbca4c7a37955244dc
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-warning-level-1-c4667"></a>编译器警告（等级 1）C4667
function： 没有匹配的函数模板定义强制实例化  
  
 无法实例化未声明的函数模板。  
  
 下面的示例将导致 C4667:  
  
```  
// C4667a.cpp  
// compile with: /LD /W1  
template  
void max(const int &, const int &); // C4667 expected  
```  
  
 若要避免此警告，首先声明的函数模板：  
  
```  
// C4667b.cpp  
// compile with: /LD  
// Declare the function template  
template<typename T>  
const T &max(const T &a, const T &b) {  
   return (a > b) ? a : b;  
}  
// Then forcibly instantiate it with a desired type ... i.e. 'int'  
//  
template  
const int &max(const int &, const int &);  
```