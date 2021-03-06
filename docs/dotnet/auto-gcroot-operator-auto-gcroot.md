---
title: auto_gcroot::operator auto_gcroot |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- auto_gcroot.operator auto_gcroot
- auto_gcroot::operator auto_gcroot
- msclr.auto_gcroot.operator auto_gcroot
- msclr::auto_gcroot::operator auto_gcroot
dev_langs:
- C++
helpviewer_keywords:
- auto_gcroot operator
ms.assetid: 43e3f27a-9f68-444f-9149-a9282a9b935a
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: eb713f6dfd959441a409a59cc83cb87ab3299162
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="autogcrootoperator-autogcroot"></a>auto_gcroot::operator auto_gcroot
之间的类型强制转换运算符`auto_gcroot`和兼容的类型。  
  
## <a name="syntax"></a>语法  
  
```  
template<typename _other_type>  
operator auto_gcroot<_other_type>();  
```  
  
## <a name="return-value"></a>返回值  
 当前`auto_gcroot`强制转换为`auto_gcroot<_other_type>`。  
  
## <a name="example"></a>示例  
  
```  
// msl_auto_gcroot_op_auto_gcroot.cpp  
// compile with: /clr  
#include <msclr\auto_gcroot.h>  
  
using namespace System;  
using namespace msclr;  
  
ref class ClassA {  
protected:     
   String^ m_s;  
public:  
   ClassA( String^ s ) : m_s( s ) {}  
  
   virtual void PrintHello() {  
      Console::WriteLine( "Hello from {0} A!", m_s );  
   }  
};  
  
ref class ClassB : ClassA {  
public:  
   ClassB( String ^ s) : ClassA( s ) {}  
   virtual void PrintHello() new {  
      Console::WriteLine( "Hello from {0} B!", m_s );  
   }  
};  
  
int main() {  
   auto_gcroot<ClassB^> b = gcnew ClassB("first");  
   b->PrintHello();  
   auto_gcroot<ClassA^> a = (auto_gcroot<ClassA^>)b;  
   a->PrintHello();  
}  
```  
  
```Output  
Hello from first B!  
Hello from first A!  
```  
  
## <a name="requirements"></a>要求  
 **标头文件** \<msclr\auto_gcroot.h >  
  
 **Namespace** msclr  
  
## <a name="see-also"></a>请参阅  
 [auto_gcroot 成员](../dotnet/auto-gcroot-members.md)