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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 678fd982505cc2bc910af9ef131f852a7f0c919a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330099"
---
# <a name="pidtagscheduleinfodisallowrecurringappts-canonical-property"></a><span data-ttu-id="457d4-103">Propriété canonique PidTagScheduleInfoDisallowRecurringAppts</span><span class="sxs-lookup"><span data-stu-id="457d4-103">PidTagScheduleInfoDisallowRecurringAppts Canonical Property</span></span>

  
  
<span data-ttu-id="457d4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="457d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="457d4-105">Contient TRUE lorsque la réponse automatique aux rendez-vous périodiques est refuser.</span><span class="sxs-lookup"><span data-stu-id="457d4-105">Contains TRUE when the automatic response to recurring appointments is decline.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="457d4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="457d4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="457d4-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span><span class="sxs-lookup"><span data-stu-id="457d4-107">PR_SCHDINFO_DISALLOW_RECURRING_APPTS</span></span>  <br/> |
|<span data-ttu-id="457d4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="457d4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="457d4-109">0x686E</span><span class="sxs-lookup"><span data-stu-id="457d4-109">0x686E</span></span>  <br/> |
|<span data-ttu-id="457d4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="457d4-110">Data type:</span></span>  <br/> |<span data-ttu-id="457d4-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="457d4-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="457d4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="457d4-112">Area:</span></span>  <br/> |<span data-ttu-id="457d4-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="457d4-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="457d4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="457d4-114">Remarks</span></span>

<span data-ttu-id="457d4-115">Cette propriété n’est significative que si la valeur de la **propriété PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) est TRUE.</span><span class="sxs-lookup"><span data-stu-id="457d4-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="457d4-116">L’absence de cette propriété indique que les réunions périodiques doivent être acceptées.</span><span class="sxs-lookup"><span data-stu-id="457d4-116">The absence of this property indicates that recurring meetings must be accepted.</span></span> <span data-ttu-id="457d4-117">Il ne s’agit pas d’une propriété obligatoire.</span><span class="sxs-lookup"><span data-stu-id="457d4-117">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="457d4-118">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="457d4-118">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="457d4-119">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="457d4-119">Protocol specifications</span></span>

<span data-ttu-id="457d4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="457d4-120">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="457d4-121">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="457d4-121">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="457d4-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="457d4-122">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="457d4-123">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="457d4-123">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="457d4-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="457d4-124">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="457d4-125">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="457d4-125">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="457d4-126">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="457d4-126">Header files</span></span>

<span data-ttu-id="457d4-127">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="457d4-127">Mapidefs.h</span></span>
  
> <span data-ttu-id="457d4-128">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="457d4-128">Provides data type definitions.</span></span>
    
<span data-ttu-id="457d4-129">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="457d4-129">Mapitags.h</span></span>
  
> <span data-ttu-id="457d4-130">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="457d4-130">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="457d4-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="457d4-131">See also</span></span>



[<span data-ttu-id="457d4-132">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="457d4-132">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="457d4-133">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="457d4-133">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="457d4-134">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="457d4-134">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="457d4-135">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="457d4-135">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

