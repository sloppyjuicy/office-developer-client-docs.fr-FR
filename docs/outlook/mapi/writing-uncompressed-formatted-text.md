---
title: Écriture de texte mis en forme non compressé
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c78d4d00-bc31-4d0b-8af0-dd0b8f3febfe
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: d34168743926681ee7169a593e302755b193aae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577043"
---
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="b0b25-103">Écriture de texte mis en forme non compressé</span><span class="sxs-lookup"><span data-stu-id="b0b25-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="b0b25-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0b25-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0b25-105">Lors de la préparation d’envoyer un message avec le texte mis en forme, soit définir la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message en texte compressé ou non compressé.</span><span class="sxs-lookup"><span data-stu-id="b0b25-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="b0b25-106">Écriture de texte compressé dans la propriété **PR_RTF_COMPRESSED** est une opération intensive du processeur très et peut affecter considérablement les performances.</span><span class="sxs-lookup"><span data-stu-id="b0b25-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="b0b25-107">Pour améliorer les performances de l’envoi des messages mis en forme, soit :</span><span class="sxs-lookup"><span data-stu-id="b0b25-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="b0b25-108">Mise à niveau de l’UC, une solution qui n’est pas toujours plausible.</span><span class="sxs-lookup"><span data-stu-id="b0b25-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="b0b25-109">Ou -</span><span class="sxs-lookup"><span data-stu-id="b0b25-109">Or -</span></span>
    
- <span data-ttu-id="b0b25-110">Écriture de texte non compressé dans la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="b0b25-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="b0b25-111">La procédure de configuration **PR_RTF_COMPRESSED** avec du texte non compressée est la même que pour l’affectation de texte compressé, avec une exception.</span><span class="sxs-lookup"><span data-stu-id="b0b25-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="b0b25-112">Lors de l’appel [WrapCompressedRTFStream](wrapcompressedrtfstream.md), définir l’indicateur STORE_UNCOMPRESSED_RTF dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b0b25-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="b0b25-113">Définition de texte non compressé présente les inconvénients en ce sens qu’elle augmente la taille des messages.</span><span class="sxs-lookup"><span data-stu-id="b0b25-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

