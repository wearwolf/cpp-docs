---
title: "CComClassFactorySingleton Class"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "reference"
f1_keywords: 
  - "ATL.CComClassFactorySingleton"
  - "ATL.CComClassFactorySingleton<T>"
  - "ATL::CComClassFactorySingleton"
  - "ATL::CComClassFactorySingleton<T>"
  - "CComClassFactorySingleton"
dev_langs: 
  - "C++"
helpviewer_keywords: 
  - "CComClassFactorySingleton class"
ms.assetid: debb983c-382b-487b-8d42-7ea26dc158b8
caps.latest.revision: 16
ms.author: "mblome"
manager: "ghogen"
translation.priority.ht: 
  - "cs-cz"
  - "de-de"
  - "es-es"
  - "fr-fr"
  - "it-it"
  - "ja-jp"
  - "ko-kr"
  - "pl-pl"
  - "pt-br"
  - "ru-ru"
  - "tr-tr"
  - "zh-cn"
  - "zh-tw"
---
# CComClassFactorySingleton Class
This class derives from [CComClassFactory](../atl/ccomclassfactory-class.md) and uses [CComObjectGlobal](../atl/ccomobjectglobal-class.md) to construct a single object.  
  
> [!IMPORTANT]
>  This class and its members cannot be used in applications that execute in the Windows Runtime.  
  
## Syntax  
  
```
template<class T>  class CComClassFactorySingleton :  public CComClassFactory
```  
  
#### Parameters  
 `T`  
 Your class.  
  
 `CComClassFactorySingleton` derives from [CComClassFactory](../atl/ccomclassfactory-class.md) and uses [CComObjectGlobal](../atl/ccomobjectglobal-class.md) to construct a single object. Each call to the `CreateInstance` method simply queries this object for an interface pointer.  
  
## Members  
  
### Public Methods  
  
|Name|Description|  
|----------|-----------------|  
|[CComClassFactorySingleton::CreateInstance](../Topic/CComClassFactorySingleton::CreateInstance.md)|Queries `m_spObj` for an interface pointer.|  
  
### Public Data Members  
  
|Name|Description|  
|----------|-----------------|  
|[CComClassFactorySingleton::m_spObj](../Topic/CComClassFactorySingleton::m_spObj.md)|The [CComObjectGlobal](../atl/ccomobjectglobal-class.md) object constructed by `CComClassFactorySingleton`.|  
  
## Remarks  
 ATL objects normally acquire a class factory by deriving from [CComCoClass](../atl/ccomcoclass-class.md). This class includes the macro [DECLARE_CLASSFACTORY](../Topic/DECLARE_CLASSFACTORY.md), which declares `CComClassFactory` as the default class factory. To use `CComClassFactorySingleton`, specify the [DECLARE_CLASSFACTORY_SINGLETON](../Topic/DECLARE_CLASSFACTORY_SINGLETON.md) macro in your object's class definition. For example:  
  
 [!code[NVC_ATL_COM#10](../atl/codesnippet/CPP/ccomclassfactorysingleton-class_1.h)]  
  
## Inheritance Hierarchy  
 `CComObjectRootBase`  
  
 [CComObjectRootEx](../atl/ccomobjectrootex-class.md)  
  
 `IClassFactory`  
  
 [CComClassFactory](../atl/ccomclassfactory-class.md)  
  
 `CComClassFactorySingleton`  
  
## Requirements  
 **Header:** atlcom.h  
  
##  <a name="ccomclassfactorysingleton__createinstance"></a>  CComClassFactorySingleton::CreateInstance  
 Calls `QueryInterface` through [m_spObj](../Topic/CComClassFactorySingleton::m_spObj.md) to retrieve an interface pointer.  
  
```
STDMETHOD(CreateInstance)(LPUNKNOWN pUnkOuter,
    REFIID riid,
    void**  ppvObj);
```  
  
### Parameters  
 `pUnkOuter`  
 [in] If the object is being created as part of an aggregate, then `pUnkOuter` must be the outer unknown. Otherwise, `pUnkOuter` must be **NULL**.  
  
 `riid`  
 [in] The IID of the requested interface. If `pUnkOuter` is non- **NULL**, `riid` must be **IID_IUnknown**.  
  
 `ppvObj`  
 [out] A pointer to the interface pointer identified by `riid`. If the object does not support this interface, `ppvObj` is set to **NULL**.  
  
### Return Value  
 A standard `HRESULT` value.  
  
##  <a name="ccomclassfactorysingleton__m_spobj"></a>  CComClassFactorySingleton::m_spObj  
 The [CComObjectGlobal](../atl/ccomobjectglobal-class.md) object constructed by `CComClassFactorySingleton`.  
  
```
CComPtr<IUnknown> m_spObj;
```  
  
### Remarks  
 Each call to the [CreateInstance](../Topic/CComClassFactorySingleton::CreateInstance.md) method simply queries this object for an interface pointer.  
  
 Note that the current form of `m_spObj` presents a breaking change from the way that `CComClassFactorySingleton` worked in previous versions of ATL. In previous versions the `CComClassFactorySingleton` object was created at the same time as the class factory, during server initialization. In Visual C++.NET 2003, the object is created lazily, on the first request. This change could cause errors in programs that rely on early initialization.  
  
## See Also  
 [IClassFactory](http://msdn.microsoft.com/library/windows/desktop/ms694364)   
 [CComClassFactory2 Class](../atl/ccomclassfactory2-class.md)   
 [CComClassFactoryAutoThread Class](../atl/ccomclassfactoryautothread-class.md)   
 [CComObjectRootEx Class](../atl/ccomobjectrootex-class.md)   
 [CComGlobalsThreadModel](../Topic/CComGlobalsThreadModel.md)   
 [Class Overview](../atl/atl-class-overview.md)
