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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 000132f052abb666ae844ec7d21b59c85ab43613
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355054"
---
# <a name="pidtagreplyrecipiententries-canonical-property"></a><span data-ttu-id="5e9d2-103">Propriété canonique PidTagReplyRecipientEntries</span><span class="sxs-lookup"><span data-stu-id="5e9d2-103">PidTagReplyRecipientEntries Canonical Property</span></span>

  
  
<span data-ttu-id="5e9d2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5e9d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5e9d2-105">Contient un tableau dimensionné d'identificateurs d'entrée pour les destinataires qui doivent recevoir une réponse.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-105">Contains a sized array of entry identifiers for recipients that are to get a reply.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5e9d2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="5e9d2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="5e9d2-107">PR_REPLY_RECIPIENT_ENTRIES</span><span class="sxs-lookup"><span data-stu-id="5e9d2-107">PR_REPLY_RECIPIENT_ENTRIES</span></span>  <br/> |
|<span data-ttu-id="5e9d2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="5e9d2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="5e9d2-109">0x004F</span><span class="sxs-lookup"><span data-stu-id="5e9d2-109">0x004F</span></span>  <br/> |
|<span data-ttu-id="5e9d2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="5e9d2-110">Data type:</span></span>  <br/> |<span data-ttu-id="5e9d2-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="5e9d2-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="5e9d2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="5e9d2-112">Area:</span></span>  <br/> |<span data-ttu-id="5e9d2-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="5e9d2-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5e9d2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5e9d2-114">Remarks</span></span>

<span data-ttu-id="5e9d2-115">Cette propriété contient une structure [FLATENTRYLIST](flatentrylist.md) et n'est pas une propriété à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-115">This property contains a [FLATENTRYLIST](flatentrylist.md) structure and is not a multivalued property.</span></span> 
  
<span data-ttu-id="5e9d2-116">Lorsque cette propriété n'est pas présente, une réponse est envoyée uniquement à l'utilisateur identifié par la propriété **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5e9d2-116">When this property is not present, a reply is sent only to the user identified by the **PR_SENDER_ENTRYID** ([PidTagSenderEntryId](pidtagsenderentryid-canonical-property.md)) property.</span></span> <span data-ttu-id="5e9d2-117">Lorsque les propriétés this et **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) sont définies, la réponse est envoyée à tous les destinataires identifiés par ces deux propriétés.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-117">When this and the **PR_REPLY_RECIPIENT_NAMES** ([PidTagReplyRecipientNames](pidtagreplyrecipientnames-canonical-property.md)) properties are defined, the reply is sent to all of the recipients identified by these two properties.</span></span> <span data-ttu-id="5e9d2-118">Un fournisseur de transport utilise ces propriétés pour remplacer la logique de réponse habituelle.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-118">A transport provider uses these properties to override the usual reply logic.</span></span>
  
<span data-ttu-id="5e9d2-119">Si cette propriété ou la propriété **PR_REPLY_RECIPIENT_NAMES** est définie, l'autre propriété doit être définie également.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-119">If either this property or the **PR_REPLY_RECIPIENT_NAMES** property is set, the other property must be set also.</span></span> <span data-ttu-id="5e9d2-120">Ces propriétés doivent contenir le même nombre de destinataires, et elles doivent les contenir dans le même ordre.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-120">These properties must contain the same number of recipients, and they must contain them in the same order.</span></span> <span data-ttu-id="5e9d2-121">Si vous ne respectez pas ces exigences, les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-121">Failure to observe these requirements can cause unpredictable results.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="5e9d2-122">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="5e9d2-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="5e9d2-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="5e9d2-123">Protocol specifications</span></span>

<span data-ttu-id="5e9d2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e9d2-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e9d2-125">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="5e9d2-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e9d2-126">[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e9d2-127">Spécifie les propriétés et les opérations qui sont autorisées pour les messages électroniques.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-127">Specifies the properties and operations that are permissible on email messages.</span></span>
    
<span data-ttu-id="5e9d2-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5e9d2-128">[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="5e9d2-129">ConVertit des conventions de messagerie standard Internet en objets message.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-129">Converts from Internet standard email conventions to message objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="5e9d2-130">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="5e9d2-130">Header files</span></span>

<span data-ttu-id="5e9d2-131">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="5e9d2-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="5e9d2-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="5e9d2-133">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="5e9d2-133">Mapitags.h</span></span>
  
> <span data-ttu-id="5e9d2-134">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="5e9d2-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5e9d2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5e9d2-135">See also</span></span>



[<span data-ttu-id="5e9d2-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="5e9d2-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="5e9d2-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="5e9d2-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="5e9d2-138">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="5e9d2-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="5e9d2-139">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="5e9d2-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

