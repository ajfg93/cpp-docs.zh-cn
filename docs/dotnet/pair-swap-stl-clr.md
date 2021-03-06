---
title: pair::swap (STL/CLR) |Microsoft 文档
ms.custom: ''
ms.date: 11/04/2016
ms.technology:
- cpp-cli
ms.topic: reference
f1_keywords:
- cliext::pair::swap
dev_langs:
- C++
helpviewer_keywords:
- swap member [STL/CLR]
ms.assetid: 7f5cbfa0-3702-40ab-a3f4-ffde02126095
author: mikeblome
ms.author: mblome
ms.workload:
- cplusplus
- dotnet
ms.openlocfilehash: 537cbbfcc3c2ad92dd023d3733e6420a2af9e32a
ms.sourcegitcommit: 76b7653ae443a2b8eb1186b789f8503609d6453e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/04/2018
---
# <a name="pairswap-stlclr"></a>pair::swap (STL/CLR)
交换两个对的内容。  
  
## <a name="syntax"></a>语法  
  
```  
void swap(pair<Value1, Value2>% right);  
```  
  
#### <a name="parameters"></a>参数  
 右  
 对要与其交换内容。  
  
## <a name="remarks"></a>备注  
 成员函数交换之间的值的存储的对`*this`和`right`。  
  
## <a name="example"></a>示例  
  
```  
// cliext_pair_swap.cpp   
// compile with: /clr   
#include <cliext/adapter>   
#include <cliext/deque>   
  
typedef cliext::collection_adapter<   
    System::Collections::ICollection> Mycoll;   
int main()   
    {   
    cliext::deque<wchar_t> d1;   
    d1.push_back(L'a');   
    d1.push_back(L'b');   
    d1.push_back(L'c');   
    Mycoll c1(%d1);   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// construct another container with repetition of values   
    cliext::deque<wchar_t> d2(5, L'x');   
    Mycoll c2(%d2);   
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
// swap and redisplay   
    c1.swap(c2);   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    for each (wchar_t elem in c2)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
    return (0);   
    }  
  
```  
  
```Output  
a b c  
x x x x x  
x x x x x  
a b c  
```  
  
## <a name="requirements"></a>要求  
 **标头：** \<cliext/实用工具 >  
  
 **Namespace:** cliext  
  
## <a name="see-also"></a>请参阅  
 [对 (STL/CLR)](../dotnet/pair-stl-clr.md)   
 [pair::operator= (STL/CLR)](../dotnet/pair-operator-assign-stl-clr.md)