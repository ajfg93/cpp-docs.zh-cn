---
title: final 说明符 |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-language
ms.topic: language-reference
f1_keywords:
- final_CPP
dev_langs:
- C++
helpviewer_keywords:
- final Identifier
ms.assetid: 649866d0-79d4-449f-ab74-f84b911b79a3
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: 82fb9e13fc5dbbafcc37905716a37322b2966c6d
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="final-specifier"></a>final 说明符
可以使用 `final` 关键字指定无法在派生类中重写的虚函数。 您还可以使用它指定无法继承的类。  
  
## <a name="syntax"></a>语法  
  
```  
  
function-declaration final;  
```  
  
```  
  
class class-name final base-classes  
```  
  
## <a name="remarks"></a>备注  
 `final` 只有在函数声明或类名称后使用时才是区分上下文的且具有特殊含义；否则，它不是保留的关键字。  
  
 在类声明中使用 `final` 时，`base-classes` 是声明的可选部分。  
  
## <a name="example"></a>示例  
 下面的示例使用 `final` 关键字指定无法重写虚函数。  
  
```cpp  
class BaseClass  
{  
    virtual void func() final;  
};  
  
class DerivedClass: public BaseClass  
{  
    virtual void func(); // compiler error: attempting to   
                         // override a final function  
};  
```  
  
 有关如何指定，可以重写成员函数的信息，请参阅[重写说明符](../cpp/override-specifier.md)。  
  
 下一个示例使用 `final` 关键字指定无法继承类。  
  
```cpp  
class BaseClass final   
{  
};  
  
class DerivedClass: public BaseClass // compiler error: BaseClass is   
                                     // marked as non-inheritable  
{  
};  
```  
  
## <a name="see-also"></a>请参阅  
 [关键字](../cpp/keywords-cpp.md)   
 [override 说明符](../cpp/override-specifier.md)