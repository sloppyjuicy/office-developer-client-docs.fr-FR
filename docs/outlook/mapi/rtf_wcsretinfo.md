---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: bf8cf115c6188b5058717437c470e11797ff5b9a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564961"
---
# <a name="rtfwcsretinfo"></a>RTF_WCSRETINFO

**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette structure fournit des informations sur un flux de données au format natif renvoyé à partir de décompresser le corps d’un message est encapsulé dans compressé texte enrichi (RTF).
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Members

_size_
  
> La taille de la structure **RTF_WCSRETINFO** en nombre d’octets. 
    
_ulStreamFlags_
  
> Il s’agit d’une valeur qui indique le format du corps natif. Cette valeur est valide uniquement si l’indicateur **MAPI_NATIVE_BODY** est passé dans le paramètre _ulFlags_ de la structure [RTF_WCSINFO](rtf_wcsinfo.md) qui est transmis à la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Cela peut être une des valeurs suivantes : 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format texte brut.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Cette valeur est uniquement utilisée si _ulFlags_ inclut l’indicateur **MAPI_NATIVE_BODY** , et le corps est au format HTML Hypertext Markup Language ().  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

