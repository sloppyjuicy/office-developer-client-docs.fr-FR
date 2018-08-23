---
title: Propriété canonique PidTagScheduleInfoDisallowOverlappingAppts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoDisallowOverlappingAppts
api_type:
- COM
ms.assetid: 27978a09-daf7-4a50-927a-96d9c4a97d02
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: c563284eb261d9b1fe4823f5d3ae90629144e1f8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565626"
---
# <a name="pidtagscheduleinfodisallowoverlappingappts-canonical-property"></a><span data-ttu-id="cf299-103">Propriété canonique PidTagScheduleInfoDisallowOverlappingAppts</span><span class="sxs-lookup"><span data-stu-id="cf299-103">PidTagScheduleInfoDisallowOverlappingAppts Canonical Property</span></span>

  
  
<span data-ttu-id="cf299-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf299-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf299-105">Contient la valeur TRUE si le rendez-vous qui se chevauchent ne sont pas autorisés.</span><span class="sxs-lookup"><span data-stu-id="cf299-105">Contains TRUE if overlapping appointments are disallowed.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cf299-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="cf299-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="cf299-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span><span class="sxs-lookup"><span data-stu-id="cf299-107">PR_SCHDINFO_DISALLOW_OVERLAPPING_APPTS</span></span>  <br/> |
|<span data-ttu-id="cf299-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="cf299-108">Identifier:</span></span>  <br/> |<span data-ttu-id="cf299-109">0x686F</span><span class="sxs-lookup"><span data-stu-id="cf299-109">0x686F</span></span>  <br/> |
|<span data-ttu-id="cf299-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="cf299-110">Data type:</span></span>  <br/> |<span data-ttu-id="cf299-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="cf299-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="cf299-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="cf299-112">Area:</span></span>  <br/> |<span data-ttu-id="cf299-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="cf299-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf299-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf299-114">Remarks</span></span>

<span data-ttu-id="cf299-115">Cette propriété est explicite uniquement lorsque la valeur de la propriété **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) a la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="cf299-115">This property is only meaningful when the value of the **PR_SCHDINFO_AUTO_ACCEPT_APPTS** ([PidTagScheduleInfoAutoAcceptAppointments](pidtagscheduleinfoautoacceptappointments-canonical-property.md)) property is TRUE.</span></span> <span data-ttu-id="cf299-116">La valeur TRUE indique que lorsque vous répondez automatiquement aux demandes de réunion, un client ou serveur doit refuser instances qui se chevauchent événements planifiées auparavant.</span><span class="sxs-lookup"><span data-stu-id="cf299-116">A value of TRUE indicates that when automatically responding to meeting requests, a client or server must decline instances that overlap previously scheduled events.</span></span> <span data-ttu-id="cf299-117">La valeur FALSE ou l’absence de cette propriété indique que le chevauchement des instances doit être accepté.</span><span class="sxs-lookup"><span data-stu-id="cf299-117">A value of FALSE or the absence of this property indicates that overlapping instances must be accepted.</span></span> <span data-ttu-id="cf299-118">Il n’est pas une propriété requise.</span><span class="sxs-lookup"><span data-stu-id="cf299-118">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="cf299-119">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="cf299-119">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="cf299-120">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="cf299-120">Protocol specifications</span></span>

<span data-ttu-id="cf299-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf299-121">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf299-122">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="cf299-122">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="cf299-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf299-123">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf299-124">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="cf299-124">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
<span data-ttu-id="cf299-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="cf299-125">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="cf299-126">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="cf299-126">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="cf299-127">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="cf299-127">Header files</span></span>

<span data-ttu-id="cf299-128">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="cf299-128">Mapidefs.h</span></span>
  
> <span data-ttu-id="cf299-129">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="cf299-129">Provides data type definitions.</span></span>
    
<span data-ttu-id="cf299-130">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="cf299-130">Mapitags.h</span></span>
  
> <span data-ttu-id="cf299-131">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="cf299-131">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf299-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cf299-132">See also</span></span>



[<span data-ttu-id="cf299-133">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="cf299-133">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="cf299-134">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="cf299-134">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="cf299-135">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="cf299-135">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="cf299-136">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="cf299-136">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

