---
title: is_void 类 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- type_traits/std::is_void
dev_langs:
- C++
helpviewer_keywords:
- is_void class
- is_void
ms.assetid: 99b0de3b-1b38-4949-b053-080e5363174e
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 13fee96611e2a2618de6ea6e1671ece9986a22d9
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="isvoid-class"></a>is_void 类

测试类型是否为 void。

## <a name="syntax"></a>语法

```cpp
template <class T>
struct is_void;
```

### <a name="parameters"></a>参数

`T` 查询的类型。

## <a name="remarks"></a>备注

如果类型 `T` 是 `void` 或 `void`的 cv 限定窗体，则类型谓词的实例为 true，否则为 false。

## <a name="example"></a>示例

```cpp
// std__type_traits__is_void.cpp
// compile with: /EHsc
#include <type_traits>
#include <iostream>

struct trivial
    {
    int val;
    };

int main()
    {
    std::cout << "is_void<trivial> == " << std::boolalpha
        << std::is_void<trivial>::value << std::endl;
    std::cout << "is_void<void()> == " << std::boolalpha
        << std::is_void<void()>::value << std::endl;
    std::cout << "is_void<void> == " << std::boolalpha
        << std::is_void<void>::value << std::endl;

    return (0);
    }

```

```Output
is_void<trivial> == false
is_void<void()> == false
is_void<void> == true
```

## <a name="requirements"></a>要求

**标头：**\<type_traits>

**命名空间：** std

## <a name="see-also"></a>请参阅

[<type_traits>](../standard-library/type-traits.md)<br/>
