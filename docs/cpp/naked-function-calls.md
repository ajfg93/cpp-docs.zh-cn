---
title: 裸函数调用 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
dev_langs:
- C++
helpviewer_keywords:
- virtual device drivers
- VXD virtual device drivers
- virtual device drivers, naked function calls
- naked functions
- prolog code
- epilog code
- naked keyword [C++]
- naked keyword [C++], storage-class attribute
ms.assetid: 2a66847a-a43f-4541-a7be-c9f5f29b5fdb
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: b9d7b42f08d68af9838bf908efdbcc59a0540b91
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="naked-function-calls"></a>Naked 函数调用
## <a name="microsoft-specific"></a>Microsoft 专用  
 函数声明与`naked`属性发出而无需 prolog 或 epilog 代码，使你能够编写使用您自己自定义 prolog/epilog 序列[内联汇编程序](../assembler/inline/inline-assembler.md)。 将裸函数作为高级功能提供。 利用这些函数，您可以声明从 C/C++ 之外的上下文中调用的函数，从而作出有关参数位置或保留哪些寄存器的各种假设。 示例包括例程（如中断处理程序）。 此功能对于虚拟设备驱动程序 (VxDs) 的编写器特别有用。  
  
## <a name="what-do-you-want-to-know-more-about"></a>你想进一步了解什么？  
  
-   [naked](../cpp/naked-cpp.md)  
  
-   [裸函数的规则和限制](../cpp/rules-and-limitations-for-naked-functions.md)  
  
-   [有关编写 Prolog/Epilog 代码的注意事项](../cpp/considerations-for-writing-prolog-epilog-code.md)  
  
**结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
 [调用约定](../cpp/calling-conventions.md)