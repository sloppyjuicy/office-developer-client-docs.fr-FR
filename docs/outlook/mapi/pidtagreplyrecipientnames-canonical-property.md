---
title: Propriété canonique PidTagReplyRecipientNames
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientNames
api_type:
- COM
ms.assetid: f5ae6124-3e44-400f-95c2-24b19f3085b5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 02dcbcccd003fb0b53356da11a3b90b38e632c2a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401635"
---
# <a name="pidtagreplyrecipientnames-canonical-property"></a><span data-ttu-id="25553-103">Propriété canonique PidTagReplyRecipientNames</span><span class="sxs-lookup"><span data-stu-id="25553-103">PidTagReplyRecipientNames Canonical Property</span></span>

  
  
<span data-ttu-id="25553-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="25553-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="25553-105">Contient une liste des noms complets des destinataires qui doivent recevoir une réponse.</span><span class="sxs-lookup"><span data-stu-id="25553-105">Contains a list of display names for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="25553-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="25553-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="25553-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span><span class="sxs-lookup"><span data-stu-id="25553-107">PR_REPLY_RECIPIENT_NAMES, PR_REPLY_RECIPIENT_NAMES_A, PR_REPLY_RECIPIENT_NAMES_W</span></span>  <br/> |
|<span data-ttu-id="25553-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="25553-108">Identifier:</span></span>  <br/> |<span data-ttu-id="25553-109">0x0050</span><span class="sxs-lookup"><span data-stu-id="25553-109">0x0050</span></span>  <br/> |
|<span data-ttu-id="25553-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="25553-110">Data type:</span></span>  <br/> |<span data-ttu-id="25553-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="25553-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="25553-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="25553-112">Area:</span></span>  <br/> |<span data-ttu-id="25553-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="25553-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25553-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="25553-114">Remarks</span></span>

<span data-ttu-id="25553-115">Ces propriétés contiennent les noms complets, séparés par des points-virgules.</span><span class="sxs-lookup"><span data-stu-id="25553-115">These properties contain the display names separated by semicolons.</span></span>
  
<span data-ttu-id="25553-116">Lorsque cette propriété n’est pas présente, une réponse est envoyée uniquement à l’utilisateur identifié par la propriété **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="25553-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) property.</span></span> <span data-ttu-id="25553-117">Lorsque **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) et ces propriétés sont définies, la réponse est envoyée à tous les destinataires identifiés par ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="25553-117">When **PR_REPLY_RECIPIENT_ENTRIES** ([PidTagReplyRecipientEntries](pidtagreplyrecipiententries-canonical-property.md)) and these properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="25553-118">Un fournisseur de transport utilise ces propriétés pour remplacer la logique de réponse habituelle.</span><span class="sxs-lookup"><span data-stu-id="25553-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="25553-119">Si **PR_REPLY_RECIPIENT_ENTRIES** ou ces propriétés sont définies, la propriété doit être définie également.</span><span class="sxs-lookup"><span data-stu-id="25553-119">If either **PR_REPLY_RECIPIENT_ENTRIES** or these properties are set, the other property must be set also.</span></span> <span data-ttu-id="25553-120">Ces propriétés doivent contenir le même nombre de destinataires, et ils doivent contenir les dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="25553-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="25553-121">Vous devez respecter ces conditions peut provoquer des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="25553-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="25553-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="25553-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="25553-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="25553-123">Protocol specifications</span></span>

<span data-ttu-id="25553-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25553-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25553-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="25553-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="25553-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25553-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25553-127">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="25553-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="25553-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="25553-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="25553-129">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="25553-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="25553-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="25553-130">Header files</span></span>

<span data-ttu-id="25553-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="25553-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="25553-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="25553-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="25553-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="25553-133">Mapitags.h</span></span>
  
> <span data-ttu-id="25553-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="25553-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="25553-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="25553-135">See also</span></span>



[<span data-ttu-id="25553-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="25553-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="25553-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="25553-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="25553-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="25553-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="25553-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="25553-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

