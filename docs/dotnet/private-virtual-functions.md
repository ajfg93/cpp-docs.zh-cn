---
title: 私有虚函数 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: conceptual
dev_langs:
- C++
helpviewer_keywords:
- virtual functions, private
- derived classes, virtual functions
- access modifiers [C++], for class members
- member access [C++], virtual members
ms.assetid: 04448086-bf72-44be-9c1f-dfda1744949e
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 97b4d7d9f47901fa69aa50bfc6f405355cf378b8
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="private-virtual-functions"></a>私有虚函数
在派生类中处理私有虚函数的方式已从托管扩展中的 c + + 更改为 Visual c + +。  
  
 在托管扩展中，虚函数的访问级别不会不会限制可在派生类中重写的功能。 在新语法中，虚函数不能重写基类虚函数，它能访问它。 例如：  
  
```  
__gc class MyBaseClass {  
   // inaccessible to a derived class   
   virtual void g();  
};  
  
__gc class MyDerivedClass : public MyBaseClass {  
public:  
   // okay in Managed Extensions; g() overrides MyBaseClass::g()  
   // error in new syntax; cannot override: MyBaseClass::g() is inaccessible  
   void g();  
};  
```  
  
 没有这种设计的新语法的实际的映射。 其中一个只需具有以使基类成员可访问的即非私有。 继承的方法不需要具有相同的访问。 在此示例中，至少侵入性的更改是使 MyBaseClass 成员`protected`。 这种方式仍禁止对通过 MyBaseClass 方法的常规程序的访问。  
  
```  
ref class MyBaseClass {  
protected:  
   virtual void g();  
};  
  
ref class MyDerivedClass : MyBaseClass {  
public:  
   virtual void g() override;  
};  
```  
  
 请注意，没有显式`virtual`关键字在基的类中，在新语法中，将生成警告消息。  
  
## <a name="see-also"></a>请参阅  
 [类或接口中的成员声明 (C++/CLI)](../dotnet/member-declarations-within-a-class-or-interface-cpp-cli.md)   
 