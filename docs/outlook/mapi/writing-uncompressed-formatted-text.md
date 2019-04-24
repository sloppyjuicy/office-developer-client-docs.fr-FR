---
title: Écriture de texte mis en forme non compressé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 7ad12fbc9671d0a21c6c6e6d4615b45a17a72fce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325752"
---
# <a name="writing-uncompressed-formatted-text"></a>Écriture de texte mis en forme non compressé

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Lors de la préparation de l'envoi d'un message avec du texte mis en forme, définissez la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message sur texte compressé ou non compressé. L'écriture de texte compressé dans la propriété **PR_RTF_COMPRESSED** est une opération gourmande en ressources processeur qui peut avoir un impact considérable sur les performances. 
  
Pour améliorer les performances de l'envoi des messages mis en forme, procédez comme suit:
  
- Mettez à niveau l'UC, une solution qui n'est pas toujours plausible.
    
    - Des
    
- Écrire du texte non compressé dans la propriété **PR_RTF_COMPRESSED** . 
    
La procédure de définition d' **PR_RTF_COMPRESSED** avec du texte non compressé est identique à celle de la définition avec du texte compressé, à une exception près. Lors de l'appel de [WrapCompressedRTFStream](wrapcompressedrtfstream.md), définissez l'indicateur STORE_UNCOMPRESSED_RTF dans le paramètre _ulFlags_ . Le fait de définir le texte non compressé présente un inconvénient: il augmente la taille des messages. 
  

