---
title: "ISessionPropertiesImpl::GetProperties"
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
ms.topic: article
ms.assetid: 48726c2a-9599-4fc5-9940-a932faef91ab
caps.latest.revision: 8
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
# ISessionPropertiesImpl::GetProperties
Returns the list of properties in the **DBPROPSET_SESSION** property group that are currently set on the session.  
  
## Syntax  
  
```  
  
      STDMETHOD(GetProperties)(   
   ULONG cPropertyIDSets,   
   const DBPROPIDSET rgPropertyIDSets[],   
   ULONG * pcPropertySets,   
   DBPROPSET ** prgPropertySets    
);  
```  
  
#### Parameters  
 See [ISessionProperties::GetProperties](https://msdn.microsoft.com/en-us/library/ms723643.aspx) in the *OLE DB Programmer's Reference*.  
  
## Requirements  
 **Header:** atldb.h  
  
## See Also  
 [ISessionPropertiesImpl Class](../VS_visualcpp/ISessionPropertiesImpl-Class.md)   
 [ISessionPropertiesImpl::SetProperties](../VS_visualcpp/ISessionPropertiesImpl--SetProperties.md)