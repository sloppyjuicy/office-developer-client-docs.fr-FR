---
title: Propriété canonique PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4f2cab31d6eed19a262bd0e667166bc79f428877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786694"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="0c641-103">Propriété canonique PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="0c641-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="0c641-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c641-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c641-105">Contient la valeur TRUE si un client ou serveur doit répondre automatiquement à toutes les demandes de réunion pour la ressource ou un participant.</span><span class="sxs-lookup"><span data-stu-id="0c641-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0c641-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="0c641-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0c641-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="0c641-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="0c641-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="0c641-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0c641-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="0c641-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="0c641-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="0c641-110">Data type:</span></span>  <br/> |<span data-ttu-id="0c641-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0c641-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0c641-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="0c641-112">Area:</span></span>  <br/> |<span data-ttu-id="0c641-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="0c641-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c641-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="0c641-114">Remarks</span></span>

<span data-ttu-id="0c641-115">Lors de la réponse, la réponse doit être acceptation, sauf si pour une contrainte supplémentaire qui est spécifiée par la **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) ou **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** propriétés ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) est remplie.</span><span class="sxs-lookup"><span data-stu-id="0c641-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="0c641-116">La valeur FALSE ou l’absence de cette propriété indique qu’un client ou serveur ne doit pas accepter automatiquement les demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="0c641-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="0c641-117">Il n’est pas une propriété requise.</span><span class="sxs-lookup"><span data-stu-id="0c641-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="0c641-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="0c641-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="0c641-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="0c641-119">Protocol specifications</span></span>

<span data-ttu-id="0c641-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c641-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c641-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="0c641-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="0c641-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c641-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c641-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="0c641-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="0c641-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="0c641-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="0c641-125">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="0c641-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="0c641-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="0c641-126">Header files</span></span>

<span data-ttu-id="0c641-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0c641-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="0c641-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="0c641-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="0c641-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="0c641-129">Mapitags.h</span></span>
  
> <span data-ttu-id="0c641-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="0c641-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0c641-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0c641-131">See also</span></span>



[<span data-ttu-id="0c641-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="0c641-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0c641-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="0c641-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0c641-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="0c641-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0c641-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="0c641-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

