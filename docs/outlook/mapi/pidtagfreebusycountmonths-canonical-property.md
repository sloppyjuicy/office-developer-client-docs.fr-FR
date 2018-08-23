---
title: Propriété canonique PidTagFreeBusyCountMonths
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyCountMonths
api_type:
- HeaderDef
ms.assetid: 278a77f2-65ec-4281-b406-942cc416a476
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: e7dc8c06fca48c5f7c124a1fdf2228ebeb9da450
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569980"
---
# <a name="pidtagfreebusycountmonths-canonical-property"></a><span data-ttu-id="90f3d-103">Propriété canonique PidTagFreeBusyCountMonths</span><span class="sxs-lookup"><span data-stu-id="90f3d-103">PidTagFreeBusyCountMonths Canonical Property</span></span>

  
  
<span data-ttu-id="90f3d-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90f3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90f3d-105">Contient la valeur pour calculer les dates de début et de fin de la plage de données et de disponibilité pour être publiés dans les dossiers publics.</span><span class="sxs-lookup"><span data-stu-id="90f3d-105">Contains the value for calculating the start and end dates of the range of free/busy data to be published to public folders.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="90f3d-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="90f3d-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="90f3d-107">PR_FREEBUSY_COUNT_MONTHS</span><span class="sxs-lookup"><span data-stu-id="90f3d-107">PR_FREEBUSY_COUNT_MONTHS</span></span>  <br/> |
|<span data-ttu-id="90f3d-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="90f3d-108">Identifier:</span></span>  <br/> |<span data-ttu-id="90f3d-109">0x6869</span><span class="sxs-lookup"><span data-stu-id="90f3d-109">0x6869</span></span>  <br/> |
|<span data-ttu-id="90f3d-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="90f3d-110">Data type:</span></span>  <br/> |<span data-ttu-id="90f3d-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="90f3d-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="90f3d-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="90f3d-112">Area:</span></span>  <br/> |<span data-ttu-id="90f3d-113">Message défini par la classe transmissible</span><span class="sxs-lookup"><span data-stu-id="90f3d-113">Message class-defined transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="90f3d-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="90f3d-114">Remarks</span></span>

<span data-ttu-id="90f3d-115">Valeur de cette propriété doit être supérieure ou égale à 0 et inférieure ou égale à 36.</span><span class="sxs-lookup"><span data-stu-id="90f3d-115">This property's value must be greater than or equal to 0 and less than or equal to 36.</span></span> <span data-ttu-id="90f3d-116">Il n’est pas une propriété requise.</span><span class="sxs-lookup"><span data-stu-id="90f3d-116">This is not a required property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="90f3d-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="90f3d-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="90f3d-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="90f3d-118">Protocol specifications</span></span>

<span data-ttu-id="90f3d-119">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90f3d-119">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90f3d-120">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="90f3d-120">Publishes the availability of a user or resource.</span></span>
    
<span data-ttu-id="90f3d-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="90f3d-121">[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="90f3d-122">Spécifie les propriétés et opérations pour un rendez-vous, une demande de réunion et les messages de réponse.</span><span class="sxs-lookup"><span data-stu-id="90f3d-122">Specifies the properties and operations for appointment, meeting request, and response messages.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="90f3d-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="90f3d-123">Header files</span></span>

<span data-ttu-id="90f3d-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="90f3d-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="90f3d-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="90f3d-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="90f3d-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="90f3d-126">Mapitags.h</span></span>
  
> <span data-ttu-id="90f3d-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="90f3d-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="90f3d-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="90f3d-128">See also</span></span>



[<span data-ttu-id="90f3d-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="90f3d-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="90f3d-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="90f3d-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="90f3d-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="90f3d-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="90f3d-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="90f3d-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

