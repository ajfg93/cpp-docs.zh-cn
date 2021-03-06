---
title: ATL 连接点类 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-atl
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- CFirePropNotifyEvent class, connection point classes
- connection points [C++], ATL classes
- ATL, connection points
- CComDynamicUnkArray class, connection point classes
- CFirePropNotifyEvent class
- CComUnkArray class, connection point classes
ms.assetid: 9582ba71-7ace-4df4-9c9b-1b0636953efc
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 49acd19fcb25751ac9223b557b068383556f63f3
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="atl-connection-point-classes"></a>ATL 连接点类
ATL 使用以下类支持连接点：  
  
-   [IConnectionPointImpl](../atl/reference/iconnectionpointimpl-class.md)实现连接点。 它表示传出接口的 IID 作为模板参数传递。  
  
-   [IConnectionPointContainerImpl](../atl/reference/iconnectionpointcontainerimpl-class.md)实现连接点容器并管理的列表`IConnectionPointImpl`对象。  
  
-   [IPropertyNotifySinkCP](../atl/reference/ipropertynotifysinkcp-class.md)实现连接点表示[IPropertyNotifySink](http://msdn.microsoft.com/library/windows/desktop/ms692638)接口。  
  
-   [CComDynamicUnkArray](../atl/reference/ccomdynamicunkarray-class.md)管理任意数目的连接点和其的接收器间的连接。  
  
-   [CComUnkArray](../atl/reference/ccomunkarray-class.md)管理大量预定义的模板参数指定的连接。  
  
-   [CFirePropNotifyEvent](../atl/reference/cfirepropnotifyevent-class.md)通知客户端的接收器对象的属性已更改或即将更改。  
  
-   [IDispEventImpl](../atl/reference/idispeventimpl-class.md)为连接点的 ATL COM 对象提供支持。 这些连接点使用事件接收器映射，提供你的 COM 对象的映射。  
  
-   [IDispEventSimpleImpl](../atl/reference/idispeventsimpleimpl-class.md)与您的类将事件路由到适当的处理程序函数中的事件接收器映射一起工作。  
  
## <a name="see-also"></a>请参阅  
 [连接点](../atl/atl-connection-points.md)

