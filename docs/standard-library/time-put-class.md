---
title: time_put 类 | Microsoft Docs
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
f1_keywords:
- xloctime/std::time_put
- locale/std::time_put::char_type
- locale/std::time_put::iter_type
- locale/std::time_put::do_put
- locale/std::time_put::put
dev_langs:
- C++
helpviewer_keywords:
- std::time_put [C++]
- std::time_put [C++], char_type
- std::time_put [C++], iter_type
- std::time_put [C++], do_put
- std::time_put [C++], put
ms.assetid: df79493e-3331-48d2-97c3-ac3a745f0791
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: fbd4cf162ba16ac5c9ae9c6bf018be2988507bcb
ms.sourcegitcommit: d55ac596ba8f908f5d91d228dc070dad31cb8360
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/08/2018
---
# <a name="timeput-class"></a>time_put 类

此模板类描述一个对象来充当区域设置 facet，以便控制时间值向 `CharType` 类型序列的转换。

## <a name="syntax"></a>语法

```cpp
template <class CharType,
    class OutputIterator = ostreambuf_iterator<CharType>>
class time_put : public locale::facet;
```

### <a name="parameters"></a>参数

`CharType` 用于在程序内的字符进行编码的类型。

`OutputIterator` 时间向其中放入函数的迭代器的类型写入其输出结果。

## <a name="remarks"></a>备注

对于任何区域设置 facet，静态对象 ID 的初始存储值为零。 首次尝试访问其存储值后，将在 **ID** 中存储唯一正值。

### <a name="constructors"></a>构造函数

|构造函数|描述|
|-|-|
|[time_put](#time_put)|`time_put` 类型的对象的构造函数。|

### <a name="typedefs"></a>Typedef

|类型名称|描述|
|-|-|
|[char_type](#char_type)|一种类型，此类型用于描述区域设置使用的字符。|
|[iter_type](#iter_type)|一种类型，此类型描述输出迭代器。|

### <a name="member-functions"></a>成员函数

|成员函数|描述|
|-|-|
|[do_put](#do_put)|一种以 `CharType` 序列的形式输出时间和日期信息的虚拟函数。|
|[put](#put)|以 `CharType` 的形式输出时间和日期信息。|

## <a name="requirements"></a>要求

**标头：** \<locale>

**命名空间：** std

## <a name="char_type"></a>  time_put::char_type

一种类型，此类型用于描述区域设置使用的字符。

```cpp
typedef CharType char_type;
```

### <a name="remarks"></a>备注

该类型是模板参数 **CharType** 的同义词。

## <a name="do_put"></a>  time_put::do_put

一种以 **CharType** 序列的形式输出时间和日期信息的虚拟函数。

```cpp
virtual iter_type do_put(
    iter_type next,
    ios_base& _Iosbase,
    const tm* _Pt,
    char _Fmt,
    char _Mod = 0) const;
```

### <a name="parameters"></a>参数

`next` 要插入的序列字符表示的日期和时间的其中一个输出迭代器。

`_Iosbase` 未使用。

`_Pt` 输出时间和日期信息。

`_Fmt` 输出的格式。 有关有效值的范围，请参阅 [strftime、wcsftime、_strftime_l、_wcsftime_l](../c-runtime-library/reference/strftime-wcsftime-strftime-l-wcsftime-l.md)。

`_Mod` 对于格式修饰符。 有关有效值的范围，请参阅 [strftime、wcsftime、_strftime_l、_wcsftime_l](../c-runtime-library/reference/strftime-wcsftime-strftime-l-wcsftime-l.md)。

### <a name="return-value"></a>返回值

插入最后一个元素后第一个位置的迭代器。

### <a name="remarks"></a>备注

受保护的虚拟成员函数从存储于对象 \* `_Pt`（**tm** 类型）中的时间值生成开始于 `next` 的有序元素。 该函数返回一个迭代器，指定在生成的输出外下一个要插入元素的位置。

通过使用与 `strftime` 相同的规则及 `_Pt` 的最后一个参数生成输出，在数组中生成一系列 `char` 元素。 假定将每个这样的 `char` 元素通过简单的、一对一的映射映射到 **CharType** 类型的等效元素。 如果 `_Mod` 等于零，有效格式为“%F”，其中 F 替换为 `_Fmt`。 否则，有效格式为“%MF”，其中 M 替换为 `_Mod`。

### <a name="example"></a>示例

请参阅 [put](#put) 的示例，它调用 `do_put`。

## <a name="iter_type"></a>  time_put::iter_type

一种类型，此类型描述输出迭代器。

```cpp
typedef OutputIterator iter_type;
```

### <a name="remarks"></a>备注

该类型是模板参数 **OutputIterator** 的同义词。

## <a name="put"></a>  time_put::put

以 **CharType** 序列的形式输出时间和日期信息。

```cpp
iter_type put(iter_type next,
    ios_base& _Iosbase,
    char_type _Fill,
    const tm* _Pt,
    char _Fmt,
    char _Mod = 0) const;

iter_type put(iter_type next,
    ios_base& _Iosbase,
    char_type _Fill,
    const tm* _Pt,
    const CharType* first,
    const CharType* last) const;
```

### <a name="parameters"></a>参数

`next` 要插入的序列字符表示的日期和时间的其中一个输出迭代器。

`_Iosbase` 未使用。

`_Fill` 类型的字符**CharType**用于间距。

`_Pt` 输出时间和日期信息。

`_Fmt` 输出的格式。 有关有效值的范围，请参阅 [strftime、wcsftime、_strftime_l、_wcsftime_l](../c-runtime-library/reference/strftime-wcsftime-strftime-l-wcsftime-l.md)。

`_Mod` 对于格式修饰符。 有关有效值的范围，请参阅 [strftime、wcsftime、_strftime_l、_wcsftime_l](../c-runtime-library/reference/strftime-wcsftime-strftime-l-wcsftime-l.md)。

`first` 输出的格式设置字符串的开头。 有关有效值的范围，请参阅 [strftime、wcsftime、_strftime_l、_wcsftime_l](../c-runtime-library/reference/strftime-wcsftime-strftime-l-wcsftime-l.md)。

`last` 输出格式设置字符串的末尾。 有关有效值的范围，请参阅 [strftime、wcsftime、_strftime_l、_wcsftime_l](../c-runtime-library/reference/strftime-wcsftime-strftime-l-wcsftime-l.md)。

### <a name="return-value"></a>返回值

插入最后一个元素后第一个位置的迭代器。

### <a name="remarks"></a>备注

成员函数返回 [do_put](#do_put)（`next`、`_Iosbase`、`_Fill`、`_Pt`、`_Fmt` 和 `_Mod`）。 第二个成员函数复制到 \* `next` ++ [ `first`, `last`) 间隔中的任何元素而不是百分号 (%)。 在间隔 [ `first`, `last`) 中，对于后跟字符 *C* 的百分号，函数会改为评估 `next` = `do_put`( `next`, `_Iosbase`, `_Fill`, `_Pt`, *C*, 0) 并跳过 *C*。但如果 *C* 是集 EOQ # 中的限定符字符（后跟 [ `first`, `last`) 间隔中的字符 `C2`），此函数会改为评估 `next` = `do_put`( `next`, `_Iosbase`, `_Fill`, `_Pt`, `C2`, *C*) 并跳过 `C2`。

### <a name="example"></a>示例

```cpp
// time_put_put.cpp
// compile with: /EHsc
#include <locale>
#include <iostream>
#include <sstream>
#include <time.h>
using namespace std;
int main( )
{
   locale loc;
   basic_stringstream<char> pszPutI;
   ios_base::iostate st = 0;
   struct tm t;
   memset( &t, 0, sizeof( struct tm ) );

   t.tm_hour = 5;
   t.tm_min = 30;
   t.tm_sec = 40;
   t.tm_year = 00;
   t.tm_mday = 4;
   t.tm_mon = 6;

   pszPutI.imbue( loc );
   char *pattern = "x: %X %x";
   use_facet <time_put <char> >
   (loc).put(basic_ostream<char>::_Iter(pszPutI.rdbuf( )),
          pszPutI, ' ', &t, pattern, pattern+strlen(pattern));

      cout << "num_put( ) = " << pszPutI.rdbuf( )->str( ) << endl;

      char strftimebuf[255];
      strftime(&strftimebuf[0], 255, pattern, &t);
      cout << "strftime( ) = " << &strftimebuf[0] << endl;
}
```

```Output
num_put( ) = x: 05:30:40 07/04/00
strftime( ) = x: 05:30:40 07/04/00
```

## <a name="time_put"></a>  time_put::time_put

类型为 `time_put` 的对象的构造函数。

```cpp
explicit time_put(size_t _Refs = 0);
```

### <a name="parameters"></a>参数

`_Refs` 用于指定类型的对象的内存管理的整数值。

### <a name="remarks"></a>备注

`_Refs` 参数可能的值及其含义：

- 0：对象的生存期由包含该对象的区域设置管理。

- 1：必须手动管理对象的生存期。

- \> 1： 未定义这些值。

构造函数初始化与与其基对象[locale::facet](../standard-library/locale-class.md#facet_class)(*_Refs*)。

## <a name="see-also"></a>请参阅

[\<locale>](../standard-library/locale.md)<br/>
[time_base 类](../standard-library/time-base-class.md)<br/>
[C++ 标准库中的线程安全](../standard-library/thread-safety-in-the-cpp-standard-library.md)<br/>
