---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: Cette structure vous permet de spécifier des informations pour décompresser le corps d’un message au format RTF compressé et de renvoyer le flux de corps dans son format natif.
ms.openlocfilehash: 4ed1ec2b8a2782ef439470dc59d1bf4d8d76a0a6
ms.sourcegitcommit: 0a067f44281eddabff15fff565fb80eaa543b660
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/23/2022
ms.locfileid: "63763207"
---
# <a name="rtf_wcsinfo"></a>RTF_WCSINFO

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette structure vous permet de spécifier des informations pour décompresser le corps d’un message au format RTF (Compressed Rich Text Format) et, éventuellement, de renvoyer le flux de corps dans son format natif.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Membres

 _taille_
  
> Taille de la structure **RTF_WCSINFO** nombre d’octets. 
    
 _ulFlags_
  
> Il s’agit du masque de bits des indicateurs d’option [pour la fonction WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Les indicateurs d’option pris en charge sont : 
    
|Flag |Description |
|:-----|:-----|
|MAPI_MODIFY  <br/> |Cela indique si le client a l’intention d’écrire l’interface de flux wrapped renvoyée. |
|STORE_UNCOMPRESSED_RTF  <br/> |Cela indique si le RTF décompressé est supposé être écrit dans le flux vers qui pointe le pointeur  _lpCompressedRTFStream_ de la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . |
|MAPI_NATIVE_BODY  <br/> |Cela indique si le flux décompressé est également converti en corps natif avant de renvoyer le flux. Cet indicateur ne peut pas être combiné avec **l’MAPI_MODIFY’indicateur** . |
   
 _ulInCodePage_
  
> Il s’agit de la valeur de page de code du message. En règle générale, cette valeur est obtenue à partir de la propriété canonique [PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) sur le message. Cette valeur est utilisée uniquement lorsque **l’indicateur MAPI_NATIVE_BODY** est transmis  _dans ulFlags_. Sinon, cette valeur est ignorée.
    
 _ulOutCodePage_
  
> Il s’agit de la valeur de page de code du flux décompressé renvoyé que vous souhaitez. Si elle est définie sur une valeur non nulle, la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convertit le flux en page de code spécifiée. Si cette valeur est définie sur zéro, MAPI décide de la page de code à utiliser. Cette valeur est utilisée uniquement lorsque **l’indicateur MAPI_NATIVE_BODY** est transmis dans  _ulFlags_ et que le format du corps n’est pas RTF. Sinon, cette valeur est ignorée.
    
## <a name="see-also"></a>Voir aussi



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

