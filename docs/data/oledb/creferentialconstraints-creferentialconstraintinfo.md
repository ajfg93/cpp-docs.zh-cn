---
title: CReferentialConstraints，CReferentialConstraintInfo |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- m_szUniqueName
- m_szCatalog
- DELETE_RULE
- m_szUniqueCatalog
- CONSTRAINT_NAME
- CReferentialConstraintInfo
- MATCH_OPTION
- m_szSchema
- m_szDeleteRule
- m_szUpdateRule
- m_szUniqueSchema
- CReferentialConstraints
- m_szName
- CONSTRAINT_CATALOG
- m_szMatchOption
- CONSTRAINT_SCHEMA
dev_langs:
- C++
helpviewer_keywords:
- m_szUniqueSchema
- DESCRIPTION class data member
- m_szSchema
- CONSTRAINT_CATALOG
- CReferentialConstraints typedef class
- m_szUniqueName
- m_szCatalog
- CONSTRAINT_NAME
- m_szDeleteRule
- DELETE_RULE
- MATCH_OPTION
- CONSTRAINT_SCHEMA
- m_szName
- m_szDescription
- m_szMatchOption
- m_szUniqueCatalog
- m_szUpdateRule
- CReferentialConstraintInfo parameter class
ms.assetid: 5d485358-be29-41c2-b0ce-19e023598e73
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: cb1a60994b286b68e9c381c9faa8718020739161
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="creferentialconstraints-creferentialconstraintinfo"></a>CReferentialConstraints，CReferentialConstraintInfo
调用 typedef 类**CReferentialConstraints**来实现其参数类**CReferentialConstraintInfo**。  
  
## <a name="remarks"></a>备注  
 请参阅[架构行集类和 Typedef 类](../../data/oledb/schema-rowset-classes-and-typedef-classes.md)有关使用 typedef 类的详细信息。  
  
 此类标识引用定义的约束，在目录中，属于给定用户。  
  
 下表列出了类数据成员及其对应的 OLE DB 列。 请参阅[REFERENTIAL_CONSTRAINTS 行集](https://msdn.microsoft.com/en-us/library/ms719737.aspx)中*OLE DB 程序员参考*有关的架构和列的详细信息。  
  
|数据成员|OLE DB 列|  
|------------------|--------------------|  
|m_szCatalog|CONSTRAINT_CATALOG|  
|m_szSchema|CONSTRAINT_SCHEMA|  
|m_szName|CONSTRAINT_NAME|  
|m_szUniqueCatalog|UNIQUE_CONSTRAINT_CATALOG|  
|m_szUniqueSchema|UNIQUE_CONSTRAINT_SCHEMA|  
|m_szUniqueName|UNIQUE_CONSTRAINT_NAME|  
|m_szMatchOption|MATCH_OPTION|  
|m_szUpdateRule|UPDATE_RULE|  
|m_szDeleteRule|DELETE_RULE|  
|m_szDescription|说明|  
  
## <a name="requirements"></a>要求  
 **标头：** atldbsch.h  
  
## <a name="see-also"></a>请参阅  
 [CRestrictions 类](../../data/oledb/crestrictions-class.md)