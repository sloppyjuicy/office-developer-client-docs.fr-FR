---
title: Propriété canonique PidTagReplyRecipientEntries
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReplyRecipientEntries
api_type:
- COM
ms.assetid: a903fd22-a3f2-464f-99b0-c087e211b124
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: ce433dda7357bdce964f897ce985286d193ec0b1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576469"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="0dd59-103">Propriété canonique PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="0dd59-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="0dd59-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0dd59-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0dd59-105">Contient un tableau d’identificateurs d’entrée de taille pour les destinataires sont pour obtenir une réponse.</span><span class="sxs-lookup"><span data-stu-id="0dd59-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0dd59-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0dd59-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0dd59-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="0dd59-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="0dd59-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0dd59-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0dd59-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="0dd59-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="0dd59-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0dd59-110">Data type:</span></span>  <br/> |<span data-ttu-id="0dd59-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="0dd59-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="0dd59-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="0dd59-112">Area:</span></span>  <br/> |<span data-ttu-id="0dd59-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="0dd59-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dd59-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0dd59-114">Remarks</span></span>

<span data-ttu-id="0dd59-115">Cette propriété contient une structure [FLATENTRYLIST](flatentrylist.md) et n’est pas une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="0dd59-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="0dd59-116">Lorsque cette propriété n’est pas présente, une réponse est envoyée uniquement à l’utilisateur identifié par la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="0dd59-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="0dd59-117">Lorsque ce et les propriétés **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) sont définies, la réponse est envoyée à tous les destinataires identifiés par ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="0dd59-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="0dd59-118">Un fournisseur de transport utilise ces propriétés pour remplacer la logique de réponse habituelle.</span><span class="sxs-lookup"><span data-stu-id="0dd59-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="0dd59-119">Si cette propriété ou la propriété **PR_REPLY_RECIPIENT_NAMES** est définie, l’autre propriété doit être définie également.</span><span class="sxs-lookup"><span data-stu-id="0dd59-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="0dd59-120">Ces propriétés doivent contenir le même nombre de destinataires, et ils doivent contenir les dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="0dd59-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="0dd59-121">Vous devez respecter ces conditions peut provoquer des résultats imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="0dd59-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0dd59-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0dd59-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0dd59-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0dd59-123">Protocol specifications</span></span>

<span data-ttu-id="0dd59-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd59-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd59-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0dd59-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0dd59-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd59-126">[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd59-127">Spécifie les propriétés et les opérations qui sont autorisées sur les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="0dd59-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="0dd59-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0dd59-128">[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0dd59-129">Convertit des conventions de messagerie standard Internet aux objets de message.</span><span class="sxs-lookup"><span data-stu-id="0dd59-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0dd59-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0dd59-130">Header files</span></span>

<span data-ttu-id="0dd59-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0dd59-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="0dd59-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0dd59-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="0dd59-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0dd59-133">Mapitags.h</span></span>
  
> <span data-ttu-id="0dd59-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0dd59-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0dd59-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dd59-135">See also</span></span>



[<span data-ttu-id="0dd59-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0dd59-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0dd59-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0dd59-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0dd59-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0dd59-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0dd59-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="0dd59-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

