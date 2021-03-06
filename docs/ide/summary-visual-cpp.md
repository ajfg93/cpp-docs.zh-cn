---
title: '&lt;摘要&gt;（Visual c + +） |Microsoft 文档'
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-ide
ms.topic: conceptual
f1_keywords:
- <summary>
- summary
dev_langs:
- C++
helpviewer_keywords:
- <summary> C++ XML tag
- summary C++ XML tag
ms.assetid: cdeeefbb-1339-45d6-9002-10042a9a2726
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
ms.openlocfilehash: c0dff1d6ce31f6b26c0f8a46ef2ff620a4d40f93
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="ltsummarygt-visual-c"></a>&lt;摘要&gt;（Visual c + +）
\<summary> 标记应当用于描述类型或类型成员。 使用 [\<remarks>](../ide/remarks-visual-cpp.md) 可针对某个类型说明添加补充信息。  
  
## <a name="syntax"></a>语法  
  
```  
<summary>description</summary>  
```  
  
#### <a name="parameters"></a>参数  
 `description`  
 对象的摘要。  
  
## <a name="remarks"></a>备注  
 文本\<摘要 > 标记是有关在 IntelliSense 中，类型的信息的唯一源，并还显示在[对象浏览器](http://msdn.microsoft.com/en-us/f89acfc5-1152-413d-9f56-3dc16e3f0470)和代码注释 Web 报表中。  
  
 使用 [/doc](../build/reference/doc-process-documentation-comments-c-cpp.md) 进行编译可以将文档注释处理到文件中。  
  
## <a name="example"></a>示例  
  
```  
// xml_summary_tag.cpp  
// compile with: /LD /clr /doc  
// post-build command: xdcmake xml_summary_tag.dll  
  
/// Text for class MyClass.  
public ref class MyClass {  
public:  
   /// <summary>MyMethod is a method in the MyClass class.  
   /// <para>Here's how you could make a second paragraph in a description. <see cref="System::Console::WriteLine"/> for information about output statements.</para>  
   /// <seealso cref="MyClass::MyMethod2"/>  
   /// </summary>  
   void MyMethod(int Int1) {}  
  
   /// text  
   void MyMethod2() {}  
};  
```  
  
## <a name="see-also"></a>请参阅  
 [XML 文档](../ide/xml-documentation-visual-cpp.md)