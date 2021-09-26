---
title: Écriture de texte mis en forme non compressé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bfa6527b177f5dcedc3c1f10a0f36c3c6301a5bc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619427"
---
# <a name="writing-uncompressed-formatted-text"></a>Écriture de texte mis en forme non compressé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de la préparation à l’envoi d’un message avec du texte mis en forme, définissez la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message sur du texte compressé ou non compressé. L’écriture de texte compressé **dans la propriété PR_RTF_COMPRESSED** est une opération très intensive du processeur et peut affecter considérablement les performances. 
  
Pour améliorer les performances d’envoi de messages formatés, vous pouvez :
  
- Mettre à niveau l’UC, une solution qui n’est pas toujours très simple.
    
    - Ou -
    
- Écrivez du texte non compressé dans **PR_RTF_COMPRESSED** propriété. 
    
La procédure de définition **PR_RTF_COMPRESSED** texte non compressé est la même que pour la définition avec du texte compressé, à une exception près. Lorsque vous [appelez WrapCompressedRTFStream,](wrapcompressedrtfstream.md)définissez l’STORE_UNCOMPRESSED_RTF dans le _paramètre ulFlags._ La définition de texte non compressé présente l’inconvénient d’augmenter la taille des messages. 
  

