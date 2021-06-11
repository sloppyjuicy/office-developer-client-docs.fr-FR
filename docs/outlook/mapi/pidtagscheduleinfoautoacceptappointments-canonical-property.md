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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330092"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a><span data-ttu-id="f58b5-103">Propriété canonique PidTagScheduleInfoAutoAcceptAppointments</span><span class="sxs-lookup"><span data-stu-id="f58b5-103">PidTagScheduleInfoAutoAcceptAppointments Canonical Property</span></span>

  
  
<span data-ttu-id="f58b5-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f58b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f58b5-105">Contient TRUE si un client ou un serveur doit répondre automatiquement à toutes les demandes de réunion pour le participant ou la ressource.</span><span class="sxs-lookup"><span data-stu-id="f58b5-105">Contains TRUE if a client or server should automatically respond to all meeting requests for the attendee or resource.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f58b5-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f58b5-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f58b5-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span><span class="sxs-lookup"><span data-stu-id="f58b5-107">PR_SCHDINFO_AUTO_ACCEPT_APPTS</span></span>  <br/> |
|<span data-ttu-id="f58b5-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f58b5-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f58b5-109">0x686D</span><span class="sxs-lookup"><span data-stu-id="f58b5-109">0x686D</span></span>  <br/> |
|<span data-ttu-id="f58b5-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f58b5-110">Data type:</span></span>  <br/> |<span data-ttu-id="f58b5-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="f58b5-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="f58b5-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f58b5-112">Area:</span></span>  <br/> |<span data-ttu-id="f58b5-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="f58b5-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f58b5-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f58b5-114">Remarks</span></span>

<span data-ttu-id="f58b5-115">Lorsque vous répondez, la réponse doit être acceptée, sauf si une contrainte supplémentaire spécifiée par les propriétés **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) ou **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) est remplie.</span><span class="sxs-lookup"><span data-stu-id="f58b5-115">When responding, the response must be acceptance, unless for an additional constraint that is specified by the **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) or **PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) properties is met.</span></span> <span data-ttu-id="f58b5-116">La valeur FALSE ou l’absence de cette propriété indique qu’un client ou un serveur ne doit pas accepter automatiquement les demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="f58b5-116">A value of FALSE or the absence of this property indicates that a client or server must not automatically accept meeting requests.</span></span> <span data-ttu-id="f58b5-117">Il ne s’agit pas d’une propriété obligatoire.</span><span class="sxs-lookup"><span data-stu-id="f58b5-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="f58b5-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f58b5-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f58b5-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="f58b5-119">Protocol specifications</span></span>

<span data-ttu-id="f58b5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f58b5-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f58b5-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="f58b5-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="f58b5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f58b5-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f58b5-123">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="f58b5-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="f58b5-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f58b5-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f58b5-125">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="f58b5-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f58b5-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f58b5-126">Header files</span></span>

<span data-ttu-id="f58b5-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f58b5-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="f58b5-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f58b5-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="f58b5-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="f58b5-129">Mapitags.h</span></span>
  
> <span data-ttu-id="f58b5-130">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="f58b5-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f58b5-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f58b5-131">See also</span></span>



[<span data-ttu-id="f58b5-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f58b5-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f58b5-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f58b5-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f58b5-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f58b5-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f58b5-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f58b5-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

