---
title: __inbytestring |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-tools
ms.topic: reference
f1_keywords:
- __inbytestring
- __inbytestring_cpp
dev_langs:
- C++
helpviewer_keywords:
- rep insb instruction
- __inbytestring intrinsic
ms.assetid: fe549556-e7a3-4af3-8ebf-8a7dc3cb233b
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 47fb619a3fbc38925f2d91ae344b00bf1be34db5
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="inbytestring"></a>__inbytestring
**Microsoft 专用**  
  
 从指定的端口使用读取数据`rep insb`指令。  
  
## <a name="syntax"></a>语法  
  
```  
void __inbytestring(  
   unsigned short Port,  
   unsigned char* Buffer,  
   unsigned long Count  
);  
```  
  
#### <a name="parameters"></a>参数  
 [in] `Port`  
 要读取的端口。  
  
 [out] `Buffer`  
 此处编写从端口读取的数据。  
  
 [in] `Count`  
 要读取数据的字节数。  
  
## <a name="requirements"></a>要求  
  
|内部函数|体系结构|  
|---------------|------------------|  
|`__inbytestring`|x86, [!INCLUDE[vcprx64](../assembler/inline/includes/vcprx64_md.md)]|  
  
 **标头文件** \<intrin.h >  
  
## <a name="remarks"></a>备注  
 此例程仅可用作内部函数。  
  
**结束 Microsoft 专用**  
  
## <a name="see-also"></a>请参阅  
 [编译器内部函数](../intrinsics/compiler-intrinsics.md)