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
# <a name="writing-uncompressed-formatted-text"></a><span data-ttu-id="44a0c-103">Écriture de texte mis en forme non compressé</span><span class="sxs-lookup"><span data-stu-id="44a0c-103">Writing Uncompressed Formatted Text</span></span>

  
  
<span data-ttu-id="44a0c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44a0c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44a0c-105">Lors de la préparation de l'envoi d'un message avec du texte mis en forme, définissez la propriété **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) du message sur texte compressé ou non compressé.</span><span class="sxs-lookup"><span data-stu-id="44a0c-105">When preparing to send a message with formatted text, either set the message's **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) property to compressed or uncompressed text.</span></span> <span data-ttu-id="44a0c-106">L'écriture de texte compressé dans la propriété **PR_RTF_COMPRESSED** est une opération gourmande en ressources processeur qui peut avoir un impact considérable sur les performances.</span><span class="sxs-lookup"><span data-stu-id="44a0c-106">Writing compressed text in the **PR_RTF_COMPRESSED** property is a very CPU intensive operation and can dramatically affect performance.</span></span> 
  
<span data-ttu-id="44a0c-107">Pour améliorer les performances de l'envoi des messages mis en forme, procédez comme suit:</span><span class="sxs-lookup"><span data-stu-id="44a0c-107">To improve the performance of sending formatted messages, either:</span></span>
  
- <span data-ttu-id="44a0c-108">Mettez à niveau l'UC, une solution qui n'est pas toujours plausible.</span><span class="sxs-lookup"><span data-stu-id="44a0c-108">Upgrade the CPU, a solution that is not always plausible.</span></span>
    
    - <span data-ttu-id="44a0c-109">Des</span><span class="sxs-lookup"><span data-stu-id="44a0c-109">Or -</span></span>
    
- <span data-ttu-id="44a0c-110">Écrire du texte non compressé dans la propriété **PR_RTF_COMPRESSED** .</span><span class="sxs-lookup"><span data-stu-id="44a0c-110">Write uncompressed text in the **PR_RTF_COMPRESSED** property.</span></span> 
    
<span data-ttu-id="44a0c-111">La procédure de définition d' **PR_RTF_COMPRESSED** avec du texte non compressé est identique à celle de la définition avec du texte compressé, à une exception près.</span><span class="sxs-lookup"><span data-stu-id="44a0c-111">The procedure for setting **PR_RTF_COMPRESSED** with uncompressed text is the same as for setting it with compressed text, with one exception.</span></span> <span data-ttu-id="44a0c-112">Lors de l'appel de [WrapCompressedRTFStream](wrapcompressedrtfstream.md), définissez l'indicateur STORE_UNCOMPRESSED_RTF dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="44a0c-112">When calling [WrapCompressedRTFStream](wrapcompressedrtfstream.md), set the STORE_UNCOMPRESSED_RTF flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="44a0c-113">Le fait de définir le texte non compressé présente un inconvénient: il augmente la taille des messages.</span><span class="sxs-lookup"><span data-stu-id="44a0c-113">Setting uncompressed text has the disadvantage in that it increases the size of messages.</span></span> 
  

