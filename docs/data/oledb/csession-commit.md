---
title: 'Csession:: Commit |Microsoft 文档'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-data
ms.topic: reference
f1_keywords:
- CSession.Commit
- ATL.CSession.Commit
- ATL::CSession::Commit
- CSession::Commit
dev_langs:
- C++
helpviewer_keywords:
- Commit method
ms.assetid: 1d5f56b9-000c-4bae-a975-89d3452f499f
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- data-storage
ms.openlocfilehash: 44fdeef9462bf30a30226ea292024a4cdb1bf8ca
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="csessioncommit"></a>CSession::Commit
提交事务。  
  
## <a name="syntax"></a>语法  
  
```cpp
HRESULT Commit(BOOL bRetaining = FALSE,   
   DWORD grfTC = XACTTC_SYNC,   
   DWORD grfRM = 0) const throw();  
```  
  
#### <a name="parameters"></a>参数  
 请参阅[itransaction:: 提交](https://msdn.microsoft.com/en-us/library/ms713008.aspx)中*OLE DB 程序员参考*。  
  
## <a name="return-value"></a>返回值  
 一个标准 `HRESULT`。  
  
## <a name="remarks"></a>备注  
 有关详细信息，请参阅[itransaction:: 提交](https://msdn.microsoft.com/en-us/library/ms713008.aspx)。  
  
## <a name="requirements"></a>要求  
 **标头:** atldbcli.h  
  
## <a name="see-also"></a>请参阅  
 [CSession 类](../../data/oledb/csession-class.md)