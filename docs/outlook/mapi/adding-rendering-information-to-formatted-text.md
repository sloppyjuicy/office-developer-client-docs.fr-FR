---
title: Ajout d’informations de rendu au texte mis en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a6018c05d1191211242066425e4ae546c1618094
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594557"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Ajout d’informations de rendu au texte mis en forme

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour indiquer l’emplacement dans le texte mis en forme, où une pièce jointe est rendue, vous devez insérer une séquence de caractères d’espace réservé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message. La séquence d’espace réservé est composée des caractères suivants : `\objattph`.
  
 **Pour ajouter des informations de rendu pour le texte du message mis en forme**
  
- Lors de l’écriture du flux de texte à la propriété du message **PR_RTF_COMPRESSED** , insérez la séquence d’espace réservé et un espace à l’emplacement où la pièce jointe doit être affichée. 
    
- Définissez la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de chaque pièce jointe à une valeur numérique. La valeur la plus faible doit être affectée à la propriété **PR_RENDERING_POSITION** de la première pièce jointe dans le texte mis en forme ; la valeur la plus élevée pour la dernière pièce jointe. 
    

