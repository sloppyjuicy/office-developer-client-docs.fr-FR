---
title: Ajout d’informations de rendu au texte formaté
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d19ff541ac13a5d18216cc512f2824176ca7727a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631103"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Ajout d’informations de rendu au texte formaté

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour indiquer l’emplacement dans le texte mis en forme où une pièce jointe est rendue, vous devez insérer une séquence de caractères d’espace réservé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message. La séquence d’espaces réservé est composé des caractères suivants  `\objattph` :
  
 **Pour ajouter des informations de rendu au texte de message formaté**
  
- Lorsque vous écrivez le flux de texte dans la propriété **PR_RTF_COMPRESSED** du message, insérez la séquence d’espace réservé et un espace à l’endroit où la pièce jointe doit être rendue. 
    
- Définissez **la PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de chaque pièce jointe sur une valeur numérique. La valeur la plus faible doit être affectée à **la propriété PR_RENDERING_POSITION** de la première pièce jointe à apparaître dans le texte formaté ; valeur la plus élevée à la dernière pièce jointe. 
    

