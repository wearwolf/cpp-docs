---
title: "set::lower_bound (STL-CLR)"
ms.custom: na
ms.date: 10/03/2016
ms.devlang: 
  - C++
ms.prod: visual-studio-dev14
ms.reviewer: na
ms.suite: na
ms.technology: 
  - devlang-cpp
ms.tgt_pltfrm: na
ms.topic: reference
H1: set::lower_bound (STL/CLR)
ms.assetid: d4da5b8b-ddf2-4d36-8092-f1be81b42348
caps.latest.revision: 13
manager: ghogen
translation.priority.ht: 
  - cs-cz
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pl-pl
  - pt-br
  - ru-ru
  - tr-tr
  - zh-cn
  - zh-tw
---
# set::lower_bound (STL-CLR)
Finds beginning of range that matches a specified key.  
  
## Syntax  
  
```  
iterator lower_bound(key_type key);  
```  
  
#### Parameters  
 key  
 Key value to search for.  
  
## Remarks  
 The member function determines the first element `X` in the controlled sequence that has equivalent ordering to `key`. If no such element exists, it returns [set::end (STL/CLR)](../VS_visualcpp/set--end--STL-CLR-.md)`()`; otherwise it returns an iterator that designates `X`. You use it to locate the beginning of a sequence of elements currently in the controlled sequence that match a specified key.  
  
## Example  
  
```  
// cliext_set_lower_bound.cpp   
// compile with: /clr   
#include <cliext/set>   
  
typedef cliext::set<wchar_t> Myset;   
int main()   
    {   
    Myset c1;   
    c1.insert(L'a');   
    c1.insert(L'b');   
    c1.insert(L'c');   
  
// display initial contents " a b c"   
    for each (wchar_t elem in c1)   
        System::Console::Write(" {0}", elem);   
    System::Console::WriteLine();   
  
    System::Console::WriteLine("lower_bound(L'x')==end() = {0}",   
        c1.lower_bound(L'x') == c1.end());   
  
    System::Console::WriteLine("*lower_bound(L'a') = {0}",   
        *c1.lower_bound(L'a'));   
    System::Console::WriteLine("*lower_bound(L'b') = {0}",   
        *c1.lower_bound(L'b'));   
    return (0);   
    }  
  
```  
  
  **a b c**  
**lower_bound(L'x')==end() = True**  
**\*lower_bound(L'a') = a**  
**\*lower_bound(L'b') = b**   
## Requirements  
 **Header:** <cliext/set>  
  
 **Namespace:** cliext  
  
## See Also  
 [set (STL/CLR)](../VS_visualcpp/set--STL-CLR-.md)   
 [set::count (STL/CLR)](../VS_visualcpp/set--count--STL-CLR-.md)   
 [set::equal_range (STL/CLR)](../VS_visualcpp/set--equal_range--STL-CLR-.md)   
 [set::find (STL/CLR)](../VS_visualcpp/set--find--STL-CLR-.md)   
 [set::upper_bound (STL/CLR)](../VS_visualcpp/set--upper_bound--STL-CLR-.md)