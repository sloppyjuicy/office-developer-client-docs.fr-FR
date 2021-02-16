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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278819"
---
# <a name="pidtagstartdate-canonical-property"></a><span data-ttu-id="ecfac-103">Propriété canonique PidTagStartDate</span><span class="sxs-lookup"><span data-stu-id="ecfac-103">PidTagStartDate Canonical Property</span></span>

  
  
<span data-ttu-id="ecfac-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecfac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecfac-105">Contient la date et l’heure de début d’un rendez-vous géré par une application de planification.</span><span class="sxs-lookup"><span data-stu-id="ecfac-105">Contains the starting date and time of an appointment as managed by a scheduling application.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ecfac-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="ecfac-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ecfac-107">PR_START_DATE</span><span class="sxs-lookup"><span data-stu-id="ecfac-107">PR_START_DATE</span></span>  <br/> |
|<span data-ttu-id="ecfac-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="ecfac-108">Identifier:</span></span>  <br/> |<span data-ttu-id="ecfac-109">0x0060</span><span class="sxs-lookup"><span data-stu-id="ecfac-109">0x0060</span></span>  <br/> |
|<span data-ttu-id="ecfac-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="ecfac-110">Data type:</span></span>  <br/> |<span data-ttu-id="ecfac-111">PT_SYSTIME</span><span class="sxs-lookup"><span data-stu-id="ecfac-111">PT_SYSTIME</span></span>  <br/> |
|<span data-ttu-id="ecfac-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="ecfac-112">Area:</span></span>  <br/> |<span data-ttu-id="ecfac-113">Enveloppe MAPI</span><span class="sxs-lookup"><span data-stu-id="ecfac-113">MAPI envelope</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecfac-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="ecfac-114">Remarks</span></span>

<span data-ttu-id="ecfac-115">Les applications de planification doivent définir cette propriété et **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) lors de l’envoi de demandes de réunion.</span><span class="sxs-lookup"><span data-stu-id="ecfac-115">Scheduling applications should set both this property and **PR_END_DATE** ([PidTagEndDate](pidtagenddate-canonical-property.md)) properties when sending meeting requests.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="ecfac-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="ecfac-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ecfac-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="ecfac-117">Protocol specifications</span></span>

<span data-ttu-id="ecfac-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecfac-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecfac-119">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="ecfac-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ecfac-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ecfac-120">[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ecfac-121">Spécifie les propriétés et les opérations pour les messages de rendez-vous, de demande de réunion et de réponse.</span><span class="sxs-lookup"><span data-stu-id="ecfac-121">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ecfac-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="ecfac-122">Header files</span></span>

<span data-ttu-id="ecfac-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ecfac-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="ecfac-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="ecfac-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="ecfac-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="ecfac-125">Mapitags.h</span></span>
  
> <span data-ttu-id="ecfac-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="ecfac-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ecfac-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ecfac-127">See also</span></span>



[<span data-ttu-id="ecfac-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="ecfac-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ecfac-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="ecfac-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ecfac-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="ecfac-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ecfac-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="ecfac-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

