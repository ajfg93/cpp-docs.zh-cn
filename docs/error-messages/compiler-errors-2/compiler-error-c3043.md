---
title: 编译器错误 C3043 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- C3043
dev_langs:
- C++
helpviewer_keywords:
- C3043
ms.assetid: 0ef55e63-e82b-48eb-9d44-690950ac34c6
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fdbb8f3cf9a0e996bc6ace521cd2bdd8b5e5dcc8
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="compiler-error-c3043"></a>编译器错误 C3043
OpenMP“critical”指令不能嵌套在同名的“critical”指令中  
  
 [critical](../../parallel/openmp/reference/critical.md) 指令不能嵌套在具有相同名称的 `critical` 指令中。  
  
 下面的示例生成 C3043：  
  
```  
// C3043.cpp  
// compile with: /openmp /c  
#include "omp.h"  
  
int main() {  
   int n1 = 1, n2 = 2, n3 = 3;  
  
   #pragma omp parallel  
   {  
      ++n2;  
  
      #pragma omp critical(MyTest)  
      {  
         ++n2;  
  
         #pragma omp critical(MyTest)   // C3043  
         // try the following line instead  
         // #pragma omp critical(MyTest2)  
         {  
            ++n3;  
         }  
      }  
   }  
}  
```