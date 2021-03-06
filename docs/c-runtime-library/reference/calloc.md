---
title: calloc | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- calloc
apilocation:
- msvcrt.dll
- msvcr80.dll
- msvcr90.dll
- msvcr100.dll
- msvcr100_clr0400.dll
- msvcr110.dll
- msvcr110_clr0400.dll
- msvcr120.dll
- msvcr120_clr0400.dll
- ucrtbase.dll
- api-ms-win-crt-heap-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- calloc
dev_langs:
- C++
helpviewer_keywords:
- memory allocation, arrays
- calloc function
ms.assetid: 17bb79a1-98cf-4096-90cb-1f9365cd6829
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: 6986e1caec25cd544919039f690544af429524af
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="calloc"></a>calloc

使用初始化为 0 的元素分配内存中的数组。

## <a name="syntax"></a>语法

```C
void *calloc(
   size_t num,
   size_t size
);
```

### <a name="parameters"></a>参数

*数*<br/>
元素数量。

*size*<br/>
每个元素的长度（以字节为单位）。

## <a name="return-value"></a>返回值

**calloc**将指针返回到分配的空间。 返回值将指向保证适当对齐任何类型的对象的存储的存储空间。 若要获取指向类型而**void**，使用类型强制转换返回值上。

## <a name="remarks"></a>备注

**Calloc**函数为数组分配存储空间*数*元素，每个长度*大小*字节。 将每个元素初始化为 0。

**calloc**设置**errno**到**ENOMEM**如果内存分配失败或内存量请求超过 **_HEAP_MAXREQ**。 有关此代码及其他错误代码的信息，请参阅 [errno、_doserrno、_sys_errlist 和 _sys_nerr](../../c-runtime-library/errno-doserrno-sys-errlist-and-sys-nerr.md)。

**calloc**调用**malloc**用于 c + + [_set_new_mode](set-new-mode.md)函数可设置新的处理程序模式。 新的处理程序模式指示是否在失败时， **malloc**是由设置调用新处理程序例程[_set_new_handler](set-new-handler.md)。 默认情况下， **malloc**不调用新处理程序例程上分配内存失败。 你可以重写此默认行为，以便，当**calloc**无法分配内存， **malloc**调用新处理程序例程中相同的方式**新**就是秒当失败时出于同样的原因。 若要重写默认值，请在程序的早期调用：

```C
_set_new_mode(1);
```

或链接到 NEWMODE.OBJ（请参阅[链接选项](../../c-runtime-library/link-options.md)）。

当与 C 运行时库的调试版本链接应用程序**calloc**解析为[_calloc_dbg](calloc-dbg.md)。 有关在调试过程中如何托管堆的详细信息，请参阅 [CRT 调试堆](/visualstudio/debugger/crt-debug-heap-details)。

**calloc**标记`__declspec(noalias)`和`__declspec(restrict)`，这意味着保证函数不能修改全局变量，并且指针返回不使用别名。 有关详细信息，请参阅 [noalias](../../cpp/noalias.md) 和[限制](../../cpp/restrict.md)。

## <a name="requirements"></a>要求

|例程|必需的标头|
|-------------|---------------------|
|**calloc**|\<stdlib.h> 和 \<malloc.h>|

有关其他兼容性信息，请参阅 [兼容性](../../c-runtime-library/compatibility.md)。

## <a name="example"></a>示例

```C
// crt_calloc.c
// This program uses calloc to allocate space for
// 40 long integers. It initializes each element to zero.

#include <stdio.h>
#include <malloc.h>

int main( void )
{
   long *buffer;

   buffer = (long *)calloc( 40, sizeof( long ) );
   if( buffer != NULL )
      printf( "Allocated 40 long integers\n" );
   else
      printf( "Can't allocate memory\n" );
   free( buffer );
}
```

```Output
Allocated 40 long integers
```

## <a name="see-also"></a>请参阅

[内存分配](../../c-runtime-library/memory-allocation.md)<br/>
[free](free.md)<br/>
[malloc](malloc.md)<br/>
[realloc](realloc.md)<br/>
