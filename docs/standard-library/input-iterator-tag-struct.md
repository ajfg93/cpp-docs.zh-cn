---
title: input_iterator_tag 结构 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- xutility/std::input_iterator_tag
dev_langs:
- C++
helpviewer_keywords:
- input_iterator_tag class
- input_iterator_tag struct
ms.assetid: ad68a4c6-f315-4ce1-8b74-c1fc71bd1577
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 797bc6353bd7396d409de073cc412480a803117f
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/07/2018
---
# <a name="inputiteratortag-struct"></a>input_iterator_tag 结构

一种为代表输入迭代器的 **iterator_category** 函数提供返回类型的类。

## <a name="syntax"></a>语法

结构 input_iterator_tag {};

## <a name="remarks"></a>备注

分类标记类用作算法选择的编译标记。 模板函数需要查找其迭代器参数的最特定的类别，以便可以在编译时使用最高效的算法。 对于每个 `Iterator` 类型的迭代器，`iterator_traits`< `Iterator`> **::iterator_category** 必须定义为最特定的类别标记，用于描述迭代器的行为。

当 **Iter** 描述一个可充当输入迭代器的对象时，其类型与 **iterator**\< **Iter**> **::iterator_category** 相同。

## <a name="example"></a>示例

有关如何使用 **iterator_tag** 的示例，请参阅 [iterator_traits](../standard-library/iterator-traits-struct.md) 或 [random_access_iterator_tag](../standard-library/random-access-iterator-tag-struct.md)。

## <a name="requirements"></a>要求

**标头：** \<iterator>

**命名空间：** std

## <a name="see-also"></a>请参阅

[C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
[C++ 标准库参考](../standard-library/cpp-standard-library-reference.md)<br/>
