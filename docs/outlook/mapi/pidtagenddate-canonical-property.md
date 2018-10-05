---
title: Propriété canonique PidTagEndDate
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEndDate
api_type:
- HeaderDef
ms.assetid: d7ec5c79-1287-4364-b5e5-5d1d6f0ea0f1
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2688e1764b6e4e31a47aeee306987caa66c709a6
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382714"
---
# <a name="pidtagenddate-canonical-property"></a><span data-ttu-id="fa11d-103">Propriété canonique PidTagEndDate</span><span class="sxs-lookup"><span data-stu-id="fa11d-103">PidTagEndDate Canonical Property</span></span>

  
  
<span data-ttu-id="fa11d-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa11d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa11d-105">Contient la date et l’heure d’un rendez-vous comme gérés par une application de planification.</span><span class="sxs-lookup"><span data-stu-id="fa11d-105">Contains the ending date and time of an appointment as managed by a scheduling application.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fa11d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="fa11d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="fa11d-107">PR_END_DATE</span><span class="sxs-lookup"><span data-stu-id="fa11d-107">PR_END_DATE</span></span>  <br/> |
|<span data-ttu-id="fa11d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="fa11d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="fa11d-109">0x0061</span><span class="sxs-lookup"><span data-stu-id="fa11d-109">0x0061</span></span>  <br/> |
|<span data-ttu-id="fa11d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="fa11d-110">Data type:</span></span>  <br/> |<span data-ttu-id="fa11d-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="fa11d-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="fa11d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="fa11d-112">Area:</span></span>  <br/> |<span data-ttu-id="fa11d-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="fa11d-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa11d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fa11d-114">Remarks</span></span>

<span data-ttu-id="fa11d-115">Applications de planification doivent définir la **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) et cette propriété lors de l’envoi de demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="fa11d-115">Scheduling applications should set both the **PR_START_DATE** ([PidTagStartDate](pidtagstartdate-canonical-property.md)) and this property when sending meeting requests.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="fa11d-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="fa11d-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="fa11d-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="fa11d-117">Protocol specifications</span></span>

<span data-ttu-id="fa11d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa11d-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa11d-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="fa11d-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="fa11d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="fa11d-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="fa11d-121">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="fa11d-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="fa11d-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="fa11d-122">Header files</span></span>

<span data-ttu-id="fa11d-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="fa11d-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="fa11d-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="fa11d-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="fa11d-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="fa11d-125">Mapitags.h</span></span>
  
> <span data-ttu-id="fa11d-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="fa11d-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fa11d-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fa11d-127">See also</span></span>



[<span data-ttu-id="fa11d-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="fa11d-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="fa11d-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="fa11d-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="fa11d-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="fa11d-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="fa11d-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="fa11d-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

