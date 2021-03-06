---
title: CXMLAccessor 类 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- ATL::CXMLAccessor
- CXMLAccessor
- ATL.CXMLAccessor
dev_langs:
- C++
helpviewer_keywords:
- CXMLAccessor class
ms.assetid: c88c082c-ec2f-4351-8947-a330b15e448a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 916e9dbe4e142192e4e716f57f97d5bd6865c709
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="cxmlaccessor-class"></a>CXMLAccessor 类
可以在不知道数据存储区的架构 （基础结构） 时，作为字符串数据访问数据源。  
  
## <a name="syntax"></a>语法

```cpp
class CXMLAccessor : public CDynamicStringAccessorW  
```  
  
## <a name="members"></a>成员  
  
### <a name="methods"></a>方法  
  
|||  
|-|-|  
|[GetXMLColumnData](../../data/oledb/cxmlaccessor-getxmlcolumndata.md)|检索列信息。|  
|[GetXMLRowData](../../data/oledb/cxmlaccessor-getxmlrowdata.md)|检索行的表的全部内容。|  
  
## <a name="remarks"></a>备注  
 但是，`CXMLAccessor`区别`CDynamicStringAccessorW`，因为它将转换从数据存储为 XML 格式 （有标记） 数据访问的所有数据。 这是非常适合 XML 感知的网页的输出。 XML 标记名称将与数据存储区的列名称尽可能匹配。  
  
 使用`CDynamicAccessor`方法以获取列信息。 此列信息用于在运行时动态创建取值函数。  
  
 列信息存储在缓冲区创建和管理此类。 获取列信息使用[GetXMLColumnData](../../data/oledb/cxmlaccessor-getxmlcolumndata.md)或通过使用的行获取列数据[GetXMLRowData](../../data/oledb/cxmlaccessor-getxmlrowdata.md)。  
  
## <a name="example"></a>示例  
 [!code-cpp[NVC_OLEDB_Consumer#14](../../data/oledb/codesnippet/cpp/cxmlaccessor-class_1.cpp)]  
  
## <a name="requirements"></a>要求  
 **标头**：atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [OLE DB 使用者模板](../../data/oledb/ole-db-consumer-templates-cpp.md)   
 [OLE DB 使用者模板参考](../../data/oledb/ole-db-consumer-templates-reference.md)   
 [CAccessor 类](../../data/oledb/caccessor-class.md)   
 [CDynamicAccessor 类](../../data/oledb/cdynamicaccessor-class.md)   
 [CDynamicParameterAccessor 类](../../data/oledb/cdynamicparameteraccessor-class.md)   
 [CDynamicStringAccessor 类](../../data/oledb/cdynamicstringaccessor-class.md)   
 [CDynamicStringAccessorA 类](../../data/oledb/cdynamicstringaccessora-class.md)   
 [CDynamicStringAccessorW 类](../../data/oledb/cdynamicstringaccessorw-class.md)   
 [CManualAccessor 类](../../data/oledb/cmanualaccessor-class.md)