---
title: Contenu des messages
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 5e8debcd5a60357f05dfb7b6bde1faf972e50a26
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784879"
---
# <a name="message-content"></a><span data-ttu-id="106ec-103">Contenu des messages</span><span class="sxs-lookup"><span data-stu-id="106ec-103">Message Content</span></span>

  
  
<span data-ttu-id="106ec-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="106ec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="106ec-105">Il existe deux codages possibles pour le contenu du message : un à l’aide de MIME, l’autre à l’aide d’uuencode.</span><span class="sxs-lookup"><span data-stu-id="106ec-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="106ec-106">MIME est le codage par défaut.</span><span class="sxs-lookup"><span data-stu-id="106ec-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="106ec-107">En outre, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui détermine les informations TNEF doivent être incluses dans un message sortant ou non.</span><span class="sxs-lookup"><span data-stu-id="106ec-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="106ec-108">Ainsi, il existe un total de quatre façons de codage du contenu des messages :</span><span class="sxs-lookup"><span data-stu-id="106ec-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="106ec-109">MIME avec TNEF</span><span class="sxs-lookup"><span data-stu-id="106ec-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="106ec-110">MIME sans TNEF</span><span class="sxs-lookup"><span data-stu-id="106ec-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="106ec-111">UUEncode avec TNEF</span><span class="sxs-lookup"><span data-stu-id="106ec-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="106ec-112">UUEncode sans TNEF</span><span class="sxs-lookup"><span data-stu-id="106ec-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="106ec-113">Comment choisir MIME ou uuencode pour les messages sortants n’est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="106ec-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="106ec-114">Les propriétés suivantes sont exclues TNEF : **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="106ec-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="106ec-115">Toutes les autres propriétés de message transmissible sont incluses dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="106ec-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="106ec-116">Les suggestions suivantes sont destinées à fournir une liste des paramètres de l’implémentation peut décider comment prendre en charge :</span><span class="sxs-lookup"><span data-stu-id="106ec-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="106ec-117">S’il faut encoder à l’aide de MIME ou uuencode pour les messages sortants : boolean.</span><span class="sxs-lookup"><span data-stu-id="106ec-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="106ec-118">À utiliser pour les messages sortants jeu de caractères : chaîne (copié directement dans le paramètre charset) ou énumération (traduit en interne pour la chaîne de jeu de caractères).</span><span class="sxs-lookup"><span data-stu-id="106ec-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

