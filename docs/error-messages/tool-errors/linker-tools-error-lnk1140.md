---
title: 链接器工具错误 LNK1140 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-diagnostics
ms.topic: error-reference
f1_keywords:
- LNK1140
dev_langs:
- C++
helpviewer_keywords:
- LNK1140
ms.assetid: 468d7651-a7cd-47b9-aead-5bb2fab56121
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fc0d59589a1882aca4ef2deb419e1e4f1081e52b
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="linker-tools-error-lnk1140"></a>链接器工具错误 LNK1140
程序数据库; 模块太多/PDB 链接： 无  
  
 项目包含多个 4096 模块。  
  
### <a name="to-fix-by-using-the-following-possible-solutions"></a>使用以下可能的解决方案进行修复  
  
1.  重新链接使用[/PDB： 无](../../build/reference/pdb-use-program-database.md)。  
  
2.  不使用调试信息编译某些模块。  
  
3.  减少模块的数。