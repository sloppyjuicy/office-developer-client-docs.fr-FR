---
title: Propriété canonique PidTagScheduleInfoDisallowRecurringAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowRecurringAppts
api_type:
- COM
ms.assetid: 61e082dd-f5bc-479b-990a-c9c0360f883e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: f5f3feb5b3186f8d0239558aa410c7f71bdf54f8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786707"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="8359f-103">Propriété canonique PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="8359f-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="8359f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8359f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8359f-105">Contient la valeur TRUE lorsque la réponse automatique pour les rendez-vous périodiques est Refuser.</span><span class="sxs-lookup"><span data-stu-id="8359f-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="8359f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="8359f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="8359f-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="8359f-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="8359f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="8359f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="8359f-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="8359f-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="8359f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="8359f-110">Data type:</span></span>  <br/> |<span data-ttu-id="8359f-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="8359f-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="8359f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="8359f-112">Area:</span></span>  <br/> |<span data-ttu-id="8359f-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="8359f-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8359f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="8359f-114">Remarks</span></span>

<span data-ttu-id="8359f-115">Cette propriété est explicite uniquement lorsque la valeur de la propriété **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) a la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="8359f-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="8359f-116">L’absence de cette propriété indique que les réunions périodiques doivent être acceptées.</span><span class="sxs-lookup"><span data-stu-id="8359f-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="8359f-117">Il n’est pas une propriété requise.</span><span class="sxs-lookup"><span data-stu-id="8359f-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="8359f-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="8359f-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="8359f-119">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="8359f-119">Protocol specifications</span></span>

<span data-ttu-id="8359f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8359f-120">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8359f-121">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="8359f-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="8359f-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8359f-122">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8359f-123">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="8359f-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="8359f-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="8359f-124">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="8359f-125">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="8359f-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="8359f-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="8359f-126">Header files</span></span>

<span data-ttu-id="8359f-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8359f-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="8359f-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="8359f-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="8359f-129">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="8359f-129">Mapitags.h</span></span>
  
> <span data-ttu-id="8359f-130">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="8359f-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="8359f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8359f-131">See also</span></span>



[<span data-ttu-id="8359f-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="8359f-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="8359f-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="8359f-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="8359f-134">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="8359f-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="8359f-135">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="8359f-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

