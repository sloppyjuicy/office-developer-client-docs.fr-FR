---
title: Contenu du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435459"
---
# <a name="message-content"></a><span data-ttu-id="32a8d-103">Contenu du message</span><span class="sxs-lookup"><span data-stu-id="32a8d-103">Message Content</span></span>

  
  
<span data-ttu-id="32a8d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="32a8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="32a8d-105">Il existe deux codages possibles pour le contenu du message : l’un utilisant MIME, l’autre utilisant uuencode.</span><span class="sxs-lookup"><span data-stu-id="32a8d-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="32a8d-106">MIME est le codage préféré.</span><span class="sxs-lookup"><span data-stu-id="32a8d-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="32a8d-107">En outre, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui détermine si les informations TNEF doivent être incluses ou non dans un message sortant.</span><span class="sxs-lookup"><span data-stu-id="32a8d-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="32a8d-108">Il existe donc un total de quatre façons d’encodage du contenu des messages :</span><span class="sxs-lookup"><span data-stu-id="32a8d-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="32a8d-109">MIME avec TNEF</span><span class="sxs-lookup"><span data-stu-id="32a8d-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="32a8d-110">MIME sans TNEF</span><span class="sxs-lookup"><span data-stu-id="32a8d-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="32a8d-111">uuencode avec TNEF</span><span class="sxs-lookup"><span data-stu-id="32a8d-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="32a8d-112">uuencode sans TNEF</span><span class="sxs-lookup"><span data-stu-id="32a8d-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="32a8d-113">La manière de choisir MIME ou uuencode pour les messages sortants n’est pas spécifiée.</span><span class="sxs-lookup"><span data-stu-id="32a8d-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="32a8d-114">Les propriétés suivantes sont exclues du TNEF **: \* PR_SENDER_**, **PR_ATTACH_DATA_ \***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="32a8d-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="32a8d-115">Toutes les autres propriétés de message transmises sont incluses dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="32a8d-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="32a8d-116">Les suggestions suivantes sont destinées à fournir une liste de paramètres que l’implémentation peut prendre en charge :</span><span class="sxs-lookup"><span data-stu-id="32a8d-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="32a8d-117">S’il faut coder à l’aide de MIME ou uuencode pour les messages sortants : booléen.</span><span class="sxs-lookup"><span data-stu-id="32a8d-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="32a8d-118">Jeu de caractères à utiliser pour les messages sortants : chaîne (copiée directement dans le paramètre charset) ou enumeration (traduite en chaîne de caractères en interne).</span><span class="sxs-lookup"><span data-stu-id="32a8d-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

