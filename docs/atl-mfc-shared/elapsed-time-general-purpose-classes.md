---
title: 运行时间： 的通用类 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-mfc
ms.topic: reference
dev_langs:
- C++
helpviewer_keywords:
- adding dates
- calculating dates and times
- dates, calculating intervals
- elapsed time, calculating
- elapsed time
- time, elapsed
- intervals, date and time
- calculations, date and time
ms.assetid: e5c5d3d2-ce1d-409e-875c-98848434e716
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: ff7ef11bb20124a05e2e85c408ce27de8f982546
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="elapsed-time-general-purpose-classes"></a>运行时间： 的通用类
下面的过程演示如何计算两个区别`CTime`对象和 get`CTimeSpan`结果。  
  
#### <a name="to-calculate-elapsed-time"></a>若要计算经过的时间  
  
1.  使用`CTime`和`CTimeSpan`对象以计算经过的时间，，如下所示：  
  
     [!code-cpp[NVC_ATLMFC_Utilities#174](../atl-mfc-shared/codesnippet/cpp/elapsed-time-general-purpose-classes_1.cpp)]  
  
     一旦你计算`elapsedTime`，您可以使用成员函数的`CTimeSpan`提取已用时间值的组件。  
  
## <a name="see-also"></a>请参阅  
 [日期和时间：通用类](../atl-mfc-shared/date-and-time-general-purpose-classes.md)

