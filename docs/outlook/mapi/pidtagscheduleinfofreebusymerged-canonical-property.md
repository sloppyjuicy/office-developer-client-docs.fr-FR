---
title: Propriété canonique PidTagScheduleInfoFreeBusyMerged
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyMerged
api_type:
- COM
ms.assetid: 3ebfccb6-967a-4f8e-9d94-94c50ba65438
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 0e1fbab53589a4ebf8681d5fe738ad625d31c18f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786714"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="4271b-103">Propriété canonique PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="4271b-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="4271b-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4271b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4271b-105">Contient les heures pour lesquelles l’état libre/occupé est défini sur occupé (e) ou absent du bureau.</span><span class="sxs-lookup"><span data-stu-id="4271b-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4271b-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="4271b-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="4271b-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="4271b-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="4271b-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="4271b-108">Identifier:</span></span>  <br/> |<span data-ttu-id="4271b-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="4271b-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="4271b-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="4271b-110">Data type:</span></span>  <br/> |<span data-ttu-id="4271b-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="4271b-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="4271b-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="4271b-112">Area:</span></span>  <br/> |<span data-ttu-id="4271b-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="4271b-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4271b-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="4271b-114">Remarks</span></span>

<span data-ttu-id="4271b-115">Événements de type disponible/occupé provisoire ne sont pas inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4271b-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="4271b-116">Le format, calcul et les restrictions de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) mais faire référence à un rendez-vous qui sont marquées comme absent du bureau ou occupé dans le calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="4271b-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="4271b-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="4271b-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="4271b-118">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="4271b-118">Protocol specifications</span></span>

<span data-ttu-id="4271b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4271b-119">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4271b-120">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="4271b-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="4271b-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="4271b-121">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="4271b-122">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="4271b-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="4271b-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="4271b-123">Header files</span></span>

<span data-ttu-id="4271b-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="4271b-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="4271b-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="4271b-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="4271b-126">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="4271b-126">Mapitags.h</span></span>
  
> <span data-ttu-id="4271b-127">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="4271b-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4271b-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4271b-128">See also</span></span>



[<span data-ttu-id="4271b-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="4271b-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="4271b-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="4271b-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="4271b-131">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="4271b-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="4271b-132">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="4271b-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

