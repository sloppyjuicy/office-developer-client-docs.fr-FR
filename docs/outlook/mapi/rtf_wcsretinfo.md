---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cfa18c215fc98610b836db31e2a07581291910be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426169"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette structure fournit des informations sur un flux au format natif renvoyé par la décompression du corps d'un message encapsulé en format RTF compressé.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Membres

_size_
  
> Taille de la structure **RTF_WCSRETINFO** en nombre d'octets. 
    
_ulStreamFlags_
  
> Il s'agit d'une valeur qui indique le format du corps natif. Cette valeur est valide uniquement si l'indicateur **MAPI_NATIVE_BODY** est transmis dans le paramètre _ulFlags_ de la structure [RTF_WCSINFO](rtf_wcsinfo.md) qui est transmise à la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Il peut s'agir de l'une des valeurs suivantes: 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Cette valeur est utilisée uniquement si _ulFlags_ inclut l'indicateur **MAPI_NATIVE_BODY** et si le corps est au format RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Cette valeur est utilisée uniquement si _ulFlags_ inclut l'indicateur **MAPI_NATIVE_BODY** et si le corps est au format de texte brut.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Cette valeur est utilisée uniquement si _ulFlags_ inclut l'indicateur **MAPI_NATIVE_BODY** et si le corps est au format html (Hypertext Markup Language).  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

