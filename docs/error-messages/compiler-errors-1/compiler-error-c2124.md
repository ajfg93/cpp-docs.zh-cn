---
title: 编译器错误 C2124 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C2124
dev_langs:
- C++
helpviewer_keywords:
- C2124
ms.assetid: 93392aaa-5582-4d68-8cc5-bd9c62a0ae7e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 79936fc45e2dbf7fc7af4bfe64cf3fc92512122b
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c2124"></a>编译器错误 C2124
被零除或对零求模  
  
 常量表达式的分母为零。 若要解决此错误，请勿将零作为除数。  
  
 下面的示例生成 C2124：  
  
```  
// C2124.cpp  
int main() {  
  int i = 1 / 0;   // C2124  do not divide by zero  
  int i2 = 12 / 2;   // OK  
}  
```