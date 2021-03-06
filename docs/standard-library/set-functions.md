---
title: '&lt;set&gt; 函数 | Microsoft Docs'
ms.custom: ''
ms.date: 11/04/2016
ms.topic: reference
f1_keywords:
- set/std::swap (map)
- set/std::swap (multiset)
ms.assetid: d1277d14-8502-46c0-b820-bcda820f9406
ms.openlocfilehash: aac2aaa09f609cd88c2bfab0e3fb66f4edade293
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="ltsetgt-functions"></a>&lt;set&gt; 函数

|||
|-|-|
|[swap (map)](#swap)|[swap (multiset)](#swap_multiset)|

## <a name="swap"></a>swap (map)

交换两个集的元素。

```cpp
template <class Key, class Traits, class Allocator>
void swap(set<Key, Traits, Allocator>& left, set<Key, Traits, Allocator>& right);
```

### <a name="parameters"></a>参数

`right` 提供要交换的元素集或者其元素将要与那些集交换的集`left`。

`left` 其元素将要与那些集交换的集`right`。

### <a name="remarks"></a>备注

模板函数是容器类上专用化的算法，用以执行成员函数 `left.`[swap](../standard-library/set-class.md#swap)( `right`)。 这是由编译器进行的函数模板偏序实例。 模板函数以此种方式重载时，模板与函数调用的匹配并不唯一，随后编译器会选择此模板函数的最专用化版本。 模板函数的通用版本

`template` \< **classT**> **void swap**( **T&**, **T&**)

在此算法中，类按赋值进行工作，这是一种慢速操作。 每个容器中的专用化版本速度快很多，因为专用化版本可适用于容器类的内部表示形式。

### <a name="example"></a>示例

有关使用 `swap` 模板函数的示例，请参阅成员类 [set::swap](../standard-library/set-class.md#swap) 的代码示例。

## <a name="swap_multiset"></a>  swap (multiset)

交换两个多重集的元素。

```cpp
template <class Key, class Traits, class Allocator>
void swap(multiset<Key, Traits, Allocator>& left, multiset<Key, Traits, Allocator>& right);
```

### <a name="parameters"></a>参数

`right` 多重集合提供要交换的元素或其元素将要与那些多重集合交换多重集合`left`。

`left` 其元素将要与那些多重集合交换多重集合`right`。

### <a name="remarks"></a>备注

模板函数是容器类多重集上专用化的算法，用以执行成员函数 `left.`[swap](../standard-library/multiset-class.md#swap)(`right`)。 这是由编译器进行的函数模板偏序实例。 模板函数以此种方式重载时，模板与函数调用的匹配并不唯一，随后编译器会选择此模板函数的最专用化版本。 模板函数的通用版本

`template` \< **classT**> **void swap**( **T&**, **T&**)

在此算法中，类按赋值进行工作，这是一种慢速操作。 每个容器中的专用化版本速度快很多，因为专用化版本可适用于容器类的内部表示形式。

### <a name="example"></a>示例

有关使用 `swap` 的模板函数的示例，请参阅成员类 [multiset::swap](../standard-library/multiset-class.md#swap) 的代码示例。

## <a name="see-also"></a>请参阅

[\<set>](../standard-library/set.md)<br/>
