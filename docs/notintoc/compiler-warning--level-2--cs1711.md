---
title: "Compiler Warning (level 2) CS1711"
ms.custom: na
ms.date: "10/13/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-csharp"
ms.tgt_pltfrm: na
ms.topic: "article"
f1_keywords: 
  - "CS1711"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS1711"
ms.assetid: 0021275a-43eb-4295-929e-bb3283577a11
caps.latest.revision: 12
ms.author: "billchi"
manager: "douge"
translation.priority.ht: 
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "ru-ru"
  - "zh-cn"
  - "zh-tw"
translation.priority.mt: 
  - "cs-cz"
  - "pl-pl"
  - "pt-br"
  - "tr-tr"
---
# Compiler Warning (level 2) CS1711
XML comment on 'type' has a typeparam tag for 'parameter', but there is no type parameter by that name  
  
 The documentation of a generic type includes a tag for the type parameter that has the wrong name.  
  
## Example  
 The following code generates warning CS1711.  
  
```  
// cs1711.cs  
// compile with: /doc:cs1711.xml  
// CS1711 expected  
using System;  
///<typeparam name="WrongName">can be an int</typeparam>  
class CMain  
{  
    public static void Main() { }  
}  
```