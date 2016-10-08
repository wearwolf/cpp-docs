---
title: "ATL Program or Control Source and Header Files"
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
ms.assetid: cb65372f-4880-4007-b582-a52eaa568fd1
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
# ATL Program or Control Source and Header Files
The following files are created when you create an ATL project in Visual Studio, depending on the options you select for the project you create.  
  
 All of these files are located in the *Projname* directory, and in either the Header Files (.h files) folder or Source Files (.cpp files) folder in Solution Explorer.  
  
|File name|Description|  
|---------------|-----------------|  
|*Projname*.h|The main include file containing the C++ interface definitions and GUID declarations of the items defined in ATLSample.idl. It is regenerated by MIDL during compilation.|  
|*Projname*.cpp|The main program source file. It contains the implementation of your DLL's exports for an in-process server and the implementation of `WinMain` for a local server. For a service, this additionally implements all the service management functions.|  
|Resource.h|The header file for the resource file.|  
|StdAfx.cpp|Includes the files StdAfx.h and Atlimpl.cpp.|  
|StdAfx.h|Includes the ATL header files.|  
  
## See Also  
 [File Types Created for Visual C++ Projects](../VS_visualcpp/File-Types-Created-for-Visual-C---Projects.md)   
 [MFC Program or Control Source and Header Files](../VS_visualcpp/MFC-Program-or-Control-Source-and-Header-Files.md)   
 [CLR Projects](../VS_visualcpp/Files-Created-for-CLR-Projects.md)