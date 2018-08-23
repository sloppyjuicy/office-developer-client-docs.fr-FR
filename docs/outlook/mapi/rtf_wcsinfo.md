---
title: RTF_WCSINFO
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0c94501e-0ec7-e836-33a7-adcf5a61b375
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 2dd9f002401f8de52a9ad187b7e5850d47caf8a7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587382"
---
# <a name="rtfwcsinfo"></a>RTF_WCSINFO

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Cette structure vous permet de spécifier des informations pour décompresser le corps d’un message dans compressé texte enrichi (RTF) et, éventuellement, retourner le flux de corps dans son format natif.
  
## <a name="quick-info"></a>Informations rapides

```cpp
typedef struct { 
    ULONG size; 
    ULONG ulFlags; 
    ULONG ulInCodePage; 
    ULONG ulOutCodePage; 
} RTF_WCSINFO;

```

## <a name="members"></a>Members

 _size_
  
> La taille de la structure **RTF_WCSINFO** en nombre d’octets. 
    
 _ulFlags_
  
> Il s’agit de masque de bits d’indicateurs d’option de la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) . Les indicateurs d’option prise en charge sont les suivants : 
    
|||
|:-----|:-----|
|N'  <br/> |Indique si le client a l’intention d’écrire l’interface flux encapsulé qui est renvoyé.  <br/> |
|STORE_UNCOMPRESSED_RTF  <br/> |Indique si le format RTF décompressé est supposé être écrits dans le flux est indiqué par le pointeur _lpCompressedRTFStream_ de la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) .  <br/> |
|MAPI_NATIVE_BODY  <br/> |Cela indique si le flux décompressé est également converti au corps natif avant de retourner le flux. Cet indicateur ne peut être combiné avec l’indicateur **ne** .  <br/> |
   
 _ulInCodePage_
  
> Il s’agit de la valeur de page de code du message. En règle générale, cette valeur est obtenue à partir de la [Propriété canonique PidTagInternetCodepage](pidtaginternetcodepage-canonical-property.md) dans le message. Cette valeur est uniquement utilisée lors de l’indicateur **MAPI_NATIVE_BODY** est passé dans _ulFlags_. Dans le cas contraire, cette valeur est ignorée.
    
 _ulOutCodePage_
  
> Il s’agit de la valeur de page de code du flux décompressé renvoyée que vous souhaitez. Si cela est défini sur une valeur différente de zéro, la fonction [WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md) convertit le flux de la page de code spécifié. Si cela est défini sur une valeur nulle, MAPI décide de page de codes à utiliser. Cette valeur est utilisée uniquement lorsque l’indicateur **MAPI_NATIVE_BODY** est passé dans _ulFlags_, et le format du corps n’est pas au format RTF. Dans le cas contraire, cette valeur est ignorée.
    
## <a name="see-also"></a>Voir aussi



[WrapCompressedRTFStreamEx](wrapcompressedrtfstreamex.md)

