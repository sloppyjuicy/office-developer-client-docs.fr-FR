---
title: Ajout d'informations de rendu au texte mis en forme
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 790180f9-8864-47d4-97fb-35fe16b957c0
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: a67fc7cbb3be5c7a23cb85e60dc33d853614cda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420611"
---
# <a name="adding-rendering-information-to-formatted-text"></a>Ajout d'informations de rendu au texte mis en forme

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour indiquer l'emplacement du texte mis en forme dans lequel une pièce jointe est affichée, vous devez insérer une séquence de caractères d'espace réservé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message. La séquence d'espace réservé est composée des caractères suivants: `\objattph`.
  
 **Pour ajouter des informations de rendu au texte du message mis en forme**
  
- Lors de l'écriture du flux de texte dans la propriété **PR_RTF_COMPRESSED** du message, insérez la séquence d'espace réservé et un espace à la position où la pièce jointe doit être affichée. 
    
- Définissez la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de chaque pièce jointe sur une valeur numérique. La valeur la plus faible doit être affectée à la propriété **PR_RENDERING_POSITION** de la première pièce jointe qui doit apparaître dans le texte mis en forme; valeur la plus élevée à la dernière pièce jointe. 
    

