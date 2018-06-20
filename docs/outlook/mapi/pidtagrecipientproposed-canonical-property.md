---
title: Propriété canonique PidTagRecipientProposed
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposed
api_type:
- COM
ms.assetid: 8cb0e46c-0937-482f-be78-1f2e5261b210
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3b05f33328e9e0b90251a99defa9816f86971337
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786529"
---
# <a name="pidtagrecipientproposed-canonical-property"></a><span data-ttu-id="36a20-103">Propriété canonique PidTagRecipientProposed</span><span class="sxs-lookup"><span data-stu-id="36a20-103">PidTagRecipientProposed Canonical Property</span></span>

  
  
<span data-ttu-id="36a20-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="36a20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="36a20-105">Indique si un participant à la réunion a répondu.</span><span class="sxs-lookup"><span data-stu-id="36a20-105">Indicates whether a meeting attendee has responded.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36a20-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="36a20-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="36a20-107">PR_RECIPIENT_PROPOSED</span><span class="sxs-lookup"><span data-stu-id="36a20-107">PR_RECIPIENT_PROPOSED</span></span>  <br/> |
|<span data-ttu-id="36a20-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="36a20-108">Identifier:</span></span>  <br/> |<span data-ttu-id="36a20-109">0x5FE1</span><span class="sxs-lookup"><span data-stu-id="36a20-109">0x5FE1</span></span>  <br/> |
|<span data-ttu-id="36a20-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="36a20-110">Data type:</span></span>  <br/> |<span data-ttu-id="36a20-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="36a20-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="36a20-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="36a20-112">Area:</span></span>  <br/> |<span data-ttu-id="36a20-113">Destinataire de transport</span><span class="sxs-lookup"><span data-stu-id="36a20-113">Transport recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36a20-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="36a20-114">Remarks</span></span>

<span data-ttu-id="36a20-115">La valeur TRUE pour cette propriété indique que le participant proposé une nouvelle date et/ou heure.</span><span class="sxs-lookup"><span data-stu-id="36a20-115">A value of TRUE for this property indicates that the attendee proposed a new date and/or time.</span></span> <span data-ttu-id="36a20-116">La valeur FALSE, ou l’absence de cette propriété, signifie que le participant n’a pas encore répondu, soit la réponse la plus récente du participant ne pas inclure une nouvelle date / heure la proposition.</span><span class="sxs-lookup"><span data-stu-id="36a20-116">A value of FALSE, or the absence of this property, means either that the attendee has not yet responded, or the most recent response from the attendee did not include a new date/ time proposal.</span></span> <span data-ttu-id="36a20-117">Cette valeur ne doit pas avoir la valeur TRUE pour les participants d’une série périodique.</span><span class="sxs-lookup"><span data-stu-id="36a20-117">This value must not be TRUE for attendees in a recurring series.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="36a20-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="36a20-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="36a20-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="36a20-119">Protocol specifications</span></span>

<span data-ttu-id="36a20-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36a20-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36a20-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="36a20-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="36a20-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="36a20-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="36a20-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="36a20-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="36a20-124">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="36a20-124">Header files</span></span>

<span data-ttu-id="36a20-125">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="36a20-125">Mapidefs.h</span></span>
  
> <span data-ttu-id="36a20-126">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="36a20-126">Provides data type definitions.</span></span>
    
<span data-ttu-id="36a20-127">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="36a20-127">Mapitags.h</span></span>
  
> <span data-ttu-id="36a20-128">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="36a20-128">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="36a20-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36a20-129">See also</span></span>



[<span data-ttu-id="36a20-130">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="36a20-130">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="36a20-131">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="36a20-131">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="36a20-132">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="36a20-132">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="36a20-133">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="36a20-133">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

