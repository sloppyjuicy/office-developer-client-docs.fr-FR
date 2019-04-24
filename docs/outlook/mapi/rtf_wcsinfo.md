---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6bec29aa0e88e0224f9cd6049553f2df6379e23d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344645"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Cette structure vous permet de spécifier des informations pour décompresser le corps d'un message au format RTF compressé et, éventuellement, renvoyer le flux de corps dans son format natif.
  
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

 _size_
  
> Taille de la structure **RTF_WCSINFO** en nombre d'octets. 
    
 _ulFlags_
  
> Il s'agit du masque de masque des indicateurs d'option pour la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Les indicateurs d'option pris en charge sont les suivants: 
    
|||
|:-----|:-----|
|MAPI_MODIFY  <br/> |Cela indique si le client envisage d'écrire l'interface de flux encapsulé qui est renvoyée.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Cela indique si le format RTF décompressé est supposé être écrit dans le flux désigné par le pointeur _lpCompressedRTFStream_ de la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Cela indique si le flux décompressé est également converti en corps natif avant de renvoyer le flux. Cet indicateur ne peut pas être combiné avec l'indicateur **MAPI_MODIFY** .  <br/> |
   
 _ulInCodePage_
  
> Il s'agit de la valeur de la page de code du message. En règle générale, cette valeur est obtenue à partir de la [propriété canonique PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) du message. Cette valeur est utilisée uniquement lorsque l'indicateur **MAPI_NATIVE_BODY** est passé dans _ulFlags_. Dans le cas contraire, cette valeur est ignorée.
    
 _ulOutCodePage_
  
> Il s'agit de la valeur de page de code du flux décompressé renvoyé que vous souhaitez. Si la valeur est différente de zéro, la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convertit le flux en la page de code spécifiée. Si cette valeur est définie sur zéro, MAPI décide de la page de code à utiliser. Cette valeur est utilisée uniquement lorsque l'indicateur **MAPI_NATIVE_BODY** est passé dans _ulFlags_et le format Body n'est pas au format RTF. Dans le cas contraire, cette valeur est ignorée.
    
## <a name="see-also"></a>Voir aussi



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

