---
title: wcrtomb | Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-standard-libraries
ms.topic: reference
apiname:
- wcrtomb
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
- api-ms-win-crt-convert-l1-1-0.dll
apitype: DLLExport
f1_keywords:
- wcrtomb
dev_langs:
- C++
helpviewer_keywords:
- wide characters, converting
- wcrtomb function
- multibyte characters
- characters, converting
ms.assetid: 717f1b21-2705-4b7f-b6d0-82adc5224340
author: corob-msft
ms.author: corob
ms.workload:
- cplusplus
ms.openlocfilehash: eca27e81cbb1df26d04059974cdc1ce5313bafa3
ms.sourcegitcommit: be2a7679c2bd80968204dee03d13ca961eaa31ff
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/03/2018
---
# <a name="wcrtomb"></a>wcrtomb

将宽字符转换为多字节字符表示形式。 此函数有一个更安全的版本；请参阅 [wcrtomb_s](wcrtomb-s.md)。

## <a name="syntax"></a>语法

```C
size_t wcrtomb(
   char *mbchar,
   wchar_t wchar,
   mbstate_t *mbstate
);
template <size_t size>
size_t wcrtomb(
   char (&mbchar)[size],
   wchar_t wchar,
   mbstate_t *mbstate
); // C++ only
```

### <a name="parameters"></a>参数

*mbchar*<br/>
生成的多字节转换字符。

*wchar*<br/>
要转换的宽字符。

*mbstate*<br/>
指向的指针**mbstate_t**对象。

## <a name="return-value"></a>返回值

返回表示已转换多字节字符所需的字节数，如果发生错误则为 -1。

## <a name="remarks"></a>备注

**Wcrtomb**函数将宽字符，从开始中包含的指定的转换状态转换*mbstate*中, 包含的值从*wchar*，到地址由*mbchar*。 返回值是表示相应的多字节字符，所需的字节数，但它不会返回多个**MB_CUR_MAX**字节。

如果*mbstate*为 null，内部**mbstate_t**对象，其中包含的转换状态*mbchar*使用。 如果字符序列*wchar*没有相应的多字节字符表示形式，则返回-1 和**errno**设置为**EILSEQ**。

**Wcrtomb**函数不同于[wctomb、 _wctomb_l](wctomb-wctomb-l.md)通过其可重启性。 转换状态存储在*mbstate*以便后续调用相同的或其他可重启函数。 混合使用可重启函数和不可重启函数时，结果不确定。 例如，应用程序将使用**wcsrlen**而非**wcsnlen**，如果的后续调用**wcsrtombs**而不是使用**wcstombs**.

在 C++ 中，此函数具有一个调用此函数的更新、更安全副本的模板重载。 有关详细信息，请参阅 [Secure Template Overloads](../../c-runtime-library/secure-template-overloads.md)。

## <a name="exceptions"></a>异常

**Wcrtomb**函数是多线程安全，前提是当前线程中的函数不调用**setlocale**执行此函数时，可以在时*mbstate*为 null。

## <a name="example"></a>示例

```C
// crt_wcrtomb.c
// compile with: /W3
// This program converts a wide character
// to its corresponding multibyte character.

#include <string.h>
#include <stdio.h>
#include <wchar.h>

int main( void )
{
    size_t      sizeOfCovertion = 0;
    mbstate_t   mbstate;
    char        mbStr = 0;
    wchar_t*    wcStr = L"Q";

    // Reset to initial conversion state
    memset(&mbstate, 0, sizeof(mbstate));

    sizeOfCovertion = wcrtomb(&mbStr, *wcStr, &mbstate); // C4996
    // Note: wcrtomb is deprecated; consider using wcrtomb_s instead
    if (sizeOfCovertion > 0)
    {
        printf("The corresponding wide character \"");
        wprintf(L"%s\"", wcStr);
        printf(" was converted to the \"%c\" ", mbStr);
        printf("multibyte character.\n");
    }
    else
    {
        printf("No corresponding multibyte character "
               "was found.\n");
    }
}
```

```Output
The corresponding wide character "Q" was converted to the "Q" multibyte character.
```

## <a name="requirements"></a>要求

|例程|必需的标头|
|-------------|---------------------|
|**wcrtomb**|\<wchar.h>|

## <a name="see-also"></a>请参阅

[数据转换](../../c-runtime-library/data-conversion.md)<br/>
[区域设置](../../c-runtime-library/locale.md)<br/>
[多字节字符序列的解释](../../c-runtime-library/interpretation-of-multibyte-character-sequences.md)<br/>
[mbsinit](mbsinit.md)<br/>
