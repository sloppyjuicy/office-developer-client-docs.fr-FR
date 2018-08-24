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
# <a name="adding-rendering-information-to-formatted-text"></a><span data-ttu-id="2e0b9-103">Ajout d’informations de rendu au texte mis en forme</span><span class="sxs-lookup"><span data-stu-id="2e0b9-103">Adding Rendering Information to Formatted Text</span></span>

  
  
<span data-ttu-id="2e0b9-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e0b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e0b9-105">Pour indiquer l’emplacement dans le texte mis en forme, où une pièce jointe est rendue, vous devez insérer une séquence de caractères d’espace réservé dans la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-105">To indicate the location in formatted text where an attachment is rendered, you must insert a sequence of placeholder characters in the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property.</span></span> <span data-ttu-id="2e0b9-106">La séquence d’espace réservé est composée des caractères suivants : `\objattph`.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-106">The placeholder sequence is made up of the following characters:  `\objattph`.</span></span>
  
 <span data-ttu-id="2e0b9-107">**Pour ajouter des informations de rendu pour le texte du message mis en forme**</span><span class="sxs-lookup"><span data-stu-id="2e0b9-107">**To add rendering information to formatted message text**</span></span>
  
- <span data-ttu-id="2e0b9-108">Lors de l’écriture du flux de texte à la propriété du message **PR_RTF_COMPRESSED** , insérez la séquence d’espace réservé et un espace à l’emplacement où la pièce jointe doit être affichée.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-108">When writing the stream of text to the message's **PR_RTF_COMPRESSED** property, insert the placeholder sequence and a space character at the position where the attachment should be rendered.</span></span> 
    
- <span data-ttu-id="2e0b9-109">Définissez la propriété **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) de chaque pièce jointe à une valeur numérique.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-109">Set the **PR_RENDERING_POSITION** ([PidTagRenderingPosition](pidtagrenderingposition-canonical-property.md)) property of each attachment to a numeric value.</span></span> <span data-ttu-id="2e0b9-110">La valeur la plus faible doit être affectée à la propriété **PR_RENDERING_POSITION** de la première pièce jointe dans le texte mis en forme ; la valeur la plus élevée pour la dernière pièce jointe.</span><span class="sxs-lookup"><span data-stu-id="2e0b9-110">The lowest value should be assigned to the **PR_RENDERING_POSITION** property of the first attachment to appear in the formatted text; the highest value to the last attachment.</span></span> 
    

