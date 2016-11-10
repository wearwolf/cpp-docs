---
title: "_mbctohira, _mbctohira_l, _mbctokata, _mbctokata_l"
ms.custom: na
ms.date: "10/14/2016"
ms.prod: "visual-studio-dev14"
ms.reviewer: na
ms.suite: na
ms.technology: 
  - "devlang-cpp"
ms.tgt_pltfrm: na
ms.topic: "article"
apiname: 
  - "_mbctohira"
  - "_mbctohira_l"
  - "_mbctokata"
  - "_mbctokata_l"
apilocation: 
  - "msvcrt.dll"
  - "msvcr80.dll"
  - "msvcr90.dll"
  - "msvcr100.dll"
  - "msvcr100_clr0400.dll"
  - "msvcr110.dll"
  - "msvcr110_clr0400.dll"
  - "msvcr120.dll"
  - "msvcr120_clr0400.dll"
  - "ucrtbase.dll"
  - "api-ms-win-crt-multibyte-l1-1-0.dll"
apitype: "DLLExport"
f1_keywords: 
  - "_mbctokata"
  - "mbctohira"
  - "_mbctohira"
  - "_mbctohira_l"
  - "mbctokata"
  - "mbctokata_l"
  - "mbctohira_l"
  - "_mbctokata_l"
dev_langs: 
  - "C++"
  - "C"
helpviewer_keywords: 
  - "_mbctokata function"
  - "_mbctokata_l function"
  - "_mbctohira_l function"
  - "mbctohira_l function"
  - "mbctohira function"
  - "mbctokata_l function"
  - "_mbctohira function"
  - "mbctokata function"
ms.assetid: f949afd7-44d4-4f08-ac8f-1fef2c915a1c
caps.latest.revision: 19
ms.author: "corob"
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
# _mbctohira, _mbctohira_l, _mbctokata, _mbctokata_l
Converts between hiragana and katakana characters.  
  
> [!IMPORTANT]
>  This API cannot be used in applications that execute in the [!INCLUDE[wrt](../atl/includes/wrt_md.md)]. For more information, see [CRT functions not supported with /ZW](http://msdn.microsoft.com/library/windows/apps/jj606124.aspx).  
  
## Syntax  
  
```  
unsigned int _mbctohira(  
   unsigned int c   
);  
unsigned int _mbctohira_l(  
   unsigned int c,  
   _locale_t locale  
);  
unsigned int _mbctokata(  
   unsigned int c   
);  
unsigned int _mbctokata_l(  
   unsigned int c,  
   _locale_t locale  
);  
```  
  
#### Parameters  
 `c`  
 Multibyte character to convert.  
  
 `locale`  
 Locale to use.  
  
## Return Value  
 Each of these functions returns the converted character `c`, if possible. Otherwise it returns the character `c` unchanged.  
  
## Remarks  
 The `_mbctohira` and `_mbctokata` functions test a character `c` and, if possible, apply one of the following conversions.  
  
|Routines|Converts|  
|--------------|--------------|  
|`_mbctohira,_mbctohira_l`|Multibyte katakana to multibyte hiragana.|  
|`_mbctokata,_mbctokata_l`|Multibyte hiragana to multibyte katakana.|  
  
 The output value is affected by the setting of the `LC_CTYPE` category setting of the locale; see [setlocale](../crt/setlocale--_wsetlocale.md) for more information. The versions of these functions are identical, except that the ones that don't have the `_l` suffix use the current locale for this locale-dependent behavior and the ones that do have the `_l` suffix instead use the locale parameter that's passed in. For more information, see [Locale](../crt/locale.md).  
  
 In earlier versions, `_mbctohira` was named `jtohira` and `_mbctokata` was named `jtokata`. For new code, use the new names.  
  
## Requirements  
  
|Routine|Required header|  
|-------------|---------------------|  
|`_mbctohira`|\<mbstring.h>|  
|`_mbctohira_l`|\<mbstring.h>|  
|`_mbctokata`|\<mbstring.h>|  
|`_mbctokata_l`|\<mbstring.h>|  
  
 For more compatibility information, see [Compatibility](../crt/compatibility.md).  
  
## .NET Framework Equivalent  
 Not applicable. To call the standard C function, use `PInvoke`. For more information, see [Platform Invoke Examples](../Topic/Platform%20Invoke%20Examples.md).  
  
## See Also  
 [Data Conversion](../crt/data-conversion.md)   
 [_mbcjistojms, _mbcjistojms_l, _mbcjmstojis, _mbcjmstojis_l](../crt/_mbcjistojms--_mbcjistojms_l--_mbcjmstojis--_mbcjmstojis_l.md)   
 [_mbctolower, _mbctolower_l, _mbctoupper, _mbctoupper_l](../crt/_mbctolower--_mbctolower_l--_mbctoupper--_mbctoupper_l.md)   
 [_mbctombb, _mbctombb_l](../crt/_mbctombb--_mbctombb_l.md)