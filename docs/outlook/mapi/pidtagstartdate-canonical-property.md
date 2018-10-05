---
title: Propriété canonique PidTagStartDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStartDate
api_type:
- COM
ms.assetid: 908c2d9f-53f4-4aa8-b309-2f3ac2dca5b5
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fd799a3dc5ba91d388285f649cccfeec188b6143
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395517"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="42a6c-103">Propriété canonique PidTagStartDate</span><span class="sxs-lookup"><span data-stu-id="42a6c-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="42a6c-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="42a6c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="42a6c-105">Contient la date et l’heure d’un rendez-vous comme gérés par une application de planification départ.</span><span class="sxs-lookup"><span data-stu-id="42a6c-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="42a6c-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="42a6c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="42a6c-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="42a6c-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="42a6c-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="42a6c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="42a6c-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="42a6c-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="42a6c-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="42a6c-110">Data type:</span></span>  <br/> |<span data-ttu-id="42a6c-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="42a6c-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="42a6c-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="42a6c-112">Area:</span></span>  <br/> |<span data-ttu-id="42a6c-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="42a6c-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42a6c-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="42a6c-114">Remarks</span></span>

<span data-ttu-id="42a6c-115">Applications de planification doivent définir cette propriété et les propriétés **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) lors de l’envoi de demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="42a6c-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="42a6c-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="42a6c-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="42a6c-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="42a6c-117">Protocol specifications</span></span>

<span data-ttu-id="42a6c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42a6c-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42a6c-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="42a6c-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="42a6c-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="42a6c-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="42a6c-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="42a6c-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="42a6c-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="42a6c-122">Header files</span></span>

<span data-ttu-id="42a6c-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="42a6c-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="42a6c-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="42a6c-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="42a6c-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="42a6c-125">Mapitags.h</span></span>
  
> <span data-ttu-id="42a6c-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="42a6c-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="42a6c-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="42a6c-127">See also</span></span>



[<span data-ttu-id="42a6c-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="42a6c-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="42a6c-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="42a6c-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="42a6c-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="42a6c-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="42a6c-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="42a6c-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

