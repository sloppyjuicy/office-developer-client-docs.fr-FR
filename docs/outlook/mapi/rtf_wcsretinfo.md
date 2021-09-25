---
title: RTF_WCSRETINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 62561d8d-33cb-e482-7fa0-132afe2b464a
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 65d3758cc0abe8835c43887558cdd9f60aeaca85
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609606"
---
# <a name="rtf_wcsretinfo"></a>RTF_WCSRETINFO

**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette structure fournit des informations sur un flux au format natif renvoyé par la décompressation du corps d’un message encapsulé au format RTF (Compressed Rich Text Format).
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    ULONG size;    
    ULONG ulStreamFlags; 
} RTF_WCSRETINFO;
```

## <a name="members"></a>Membres

_size_
  
> Taille de la structure **RTF_WCSRETINFO** nombre d’octets. 
    
_ulStreamFlags_
  
> Il s’agit d’une valeur qui indique le format du corps natif. Cette valeur n’est valide que si l’indicateur **MAPI_NATIVE_BODY** est transmis dans le paramètre _ulFlags_ de la structure [RTF_WCSINFO](rtf_wcsinfo.md) transmise à la fonction [WrapCompressedRTFStreamEx.](wrapcompressedrtfstreamex.md) Il peut s’y trouver avec l’une des valeurs suivantes : 
    
|||
|:-----|:-----|
|MAPI_NATIVE_BODY_TYPE_RTF  <br/> |Cette valeur est utilisée uniquement si  _ulFlags_ inclut **l’MAPI_NATIVE_BODY** et si le corps est RTF.  <br/> |
|MAPI_NATIVE_BODY_TYPE_PLAIN_TEXT  <br/> |Cette valeur est utilisée uniquement si  _ulFlags_ inclut **l’MAPI_NATIVE_BODY** et si le corps est au format texte simple.  <br/> |
|MAPI_NATIVE_BODY_TYPE_HTML  <br/> |Cette valeur est utilisée uniquement si  _ulFlags_ inclut **l’indicateur MAPI_NATIVE_BODY** et que le corps est au format HTML (Hypertext Markup Language).  <br/> |
   
## <a name="see-also"></a>Voir aussi

- [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

