---
title: Écriture non compressée du texte mis en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 9baf3397255d6138caaad84de5ff5621bd6c9555
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787492"
---
# <a name="writing-uncompressed-formatted-text"></a>Écriture non compressée du texte mis en forme

  
  
**S’applique à**: Outlook 
  
Lors de la préparation d’envoyer un message avec le texte mis en forme, soit définir la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message en texte compressé ou non compressé. Écriture de texte compressé dans la propriété **PR_RTF_COMPRESSED** est une opération intensive du processeur très et peut affecter considérablement les performances. 
  
Pour améliorer les performances de l’envoi des messages mis en forme, soit :
  
- Mise à niveau de l’UC, une solution qui n’est pas toujours plausible.
    
    - Ou -
    
- Écriture de texte non compressé dans la propriété **PR_RTF_COMPRESSED** . 
    
La procédure de configuration **PR_RTF_COMPRESSED** avec du texte non compressée est la même que pour l’affectation de texte compressé, avec une exception. Lors de l’appel [WrapCompressedRTFStream](wrapcompressedrtfstream.md), définir l’indicateur STORE_UNCOMPRESSED_RTF dans le paramètre _ulFlags_ . Définition de texte non compressé présente les inconvénients en ce sens qu’elle augmente la taille des messages. 
  

