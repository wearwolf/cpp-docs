---
title: "Compiler Error CS0528"
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
  - "CS0528"
dev_langs: 
  - "CSharp"
helpviewer_keywords: 
  - "CS0528"
ms.assetid: 8f5dde55-7e4f-4ffa-be14-0e0f3a538118
caps.latest.revision: 7
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
# Compiler Error CS0528
'interface' is already listed in interface list  
  
 An interface-inheritance list includes a duplicate. An [interface](../Topic/interface%20\(C%23%20Reference\).md) can only be specified once in the inheritance list.  
  
 The following sample generates CS0528:  
  
```  
// CS0528.cs  
namespace x  
{  
   public interface a  
   {  
   }  
  
   public class b : a, a   // CS0528  
   {  
      public void Main()  
      {  
      }  
   }  
}  
```