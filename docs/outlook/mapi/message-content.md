---
title: Contenu du message
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ce643afe-e5b6-42f2-b3cf-4efb957c4f2e
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: c4d2439c06da292c9cc72c1506a1ae4d10c6704f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357000"
---
# <a name="message-content"></a><span data-ttu-id="b612a-103">Contenu du message</span><span class="sxs-lookup"><span data-stu-id="b612a-103">Message Content</span></span>

  
  
<span data-ttu-id="b612a-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b612a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b612a-105">Il existe deux codages possibles pour le contenu du message: l'un avec MIME, l'autre avec UUEncode.</span><span class="sxs-lookup"><span data-stu-id="b612a-105">There are two possible encodings for the message content: one using MIME, the other using uuencode.</span></span> <span data-ttu-id="b612a-106">MIME est le codage par défaut.</span><span class="sxs-lookup"><span data-stu-id="b612a-106">MIME is the preferred encoding.</span></span> <span data-ttu-id="b612a-107">De plus, MAPI définit une propriété par destinataire, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), qui régit si les informations TNEF doivent être incluses ou non dans un message sortant.</span><span class="sxs-lookup"><span data-stu-id="b612a-107">In addition, MAPI defines a per-recipient property, **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)), which governs whether or not TNEF information should be included in an outgoing message.</span></span> <span data-ttu-id="b612a-108">Il y a quatre façons de coder le contenu des messages:</span><span class="sxs-lookup"><span data-stu-id="b612a-108">So there are a total of four ways of encoding message content:</span></span>
  
- <span data-ttu-id="b612a-109">MIME avec TNEF</span><span class="sxs-lookup"><span data-stu-id="b612a-109">MIME with TNEF</span></span>
    
- <span data-ttu-id="b612a-110">MIME sans TNEF</span><span class="sxs-lookup"><span data-stu-id="b612a-110">MIME without TNEF</span></span>
    
- <span data-ttu-id="b612a-111">UUEncode avec TNEF</span><span class="sxs-lookup"><span data-stu-id="b612a-111">uuencode with TNEF</span></span>
    
- <span data-ttu-id="b612a-112">UUEncode sans TNEF</span><span class="sxs-lookup"><span data-stu-id="b612a-112">uuencode without TNEF</span></span>
    
<span data-ttu-id="b612a-113">Le choix entre MIME ou uuencode pour les messages sortants n'est pas spécifié.</span><span class="sxs-lookup"><span data-stu-id="b612a-113">How to choose MIME or uuencode for outbound messages is not specified.</span></span>
  
<span data-ttu-id="b612a-114">Les propriétés suivantes sont exclues de TNEF **:\*PR_SENDER_**, **PR_ATTACH_DATA_\***, **PR_BODY**.</span><span class="sxs-lookup"><span data-stu-id="b612a-114">The following properties are excluded from TNEF: **PR_SENDER_\***, **PR_ATTACH_DATA_\***, **PR_BODY**.</span></span> <span data-ttu-id="b612a-115">Toutes les autres propriétés de message transmissibles sont incluses dans le flux TNEF.</span><span class="sxs-lookup"><span data-stu-id="b612a-115">All other transmittable message properties are included in the TNEF stream.</span></span>
  
<span data-ttu-id="b612a-116">Les suggestions suivantes sont destinées à fournir une liste des paramètres que l'implémentation peut prendre en charge:</span><span class="sxs-lookup"><span data-stu-id="b612a-116">The following suggestions are intended to provide a list of parameters that the implementation can decide how to support:</span></span>
  
- <span data-ttu-id="b612a-117">Codage MIME ou uuencode pour les messages sortants: Boolean.</span><span class="sxs-lookup"><span data-stu-id="b612a-117">Whether to encode using MIME or uuencode for outbound messages: boolean.</span></span>
    
- <span data-ttu-id="b612a-118">Jeu de caractères à utiliser pour les messages sortants: chaîne (copié directement vers le paramètre charset) ou énumération (traduite en interne en chaîne charset).</span><span class="sxs-lookup"><span data-stu-id="b612a-118">Character set to use for outbound messages: string (copied directly to charset parameter) or enumeration (translated internally to charset string).</span></span>
    

