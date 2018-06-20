---
title: Ajout d’informations d’affichage du texte mis en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: b912d81c1413fb40b6ddccc2f54bc393a6b67857
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782888"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Ajout d’informations d’affichage du texte mis en forme

  
  
**S’applique à**: Outlook 
  
Pour indiquer l’emplacement dans le texte mis en forme, où une pièce jointe est rendue, vous devez insérer une séquence de caractères d’espace réservé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message. La séquence d’espace réservé est composée des caractères suivants : `\objattph`.
  
 **Pour ajouter des informations de rendu pour le texte du message mis en forme**
  
- Lors de l’écriture du flux de texte à la propriété du message **PR_RTF_COMPRESSED** , insérez la séquence d’espace réservé et un espace à l’emplacement où la pièce jointe doit être affichée. 
    
- Définissez la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de chaque pièce jointe à une valeur numérique. La valeur la plus faible doit être affectée à la propriété **PR_RENDERING_POSITION** de la première pièce jointe dans le texte mis en forme ; la valeur la plus élevée pour la dernière pièce jointe. 
    

