---
title: Propriété canonique PidTagScheduleInfoFreeBusyAway
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyAway
api_type:
- COM
ms.assetid: 7b5d013a-15ac-469a-98c8-3ed1e80f6faf
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 717f934c0dadc46935b72c409469633e0779fb3d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576336"
---
# <a name="pidtagscheduleinfofreebusyaway-canonical-property"></a><span data-ttu-id="b9089-103">Propriété canonique PidTagScheduleInfoFreeBusyAway</span><span class="sxs-lookup"><span data-stu-id="b9089-103">PidTagScheduleInfoFreeBusyAway Canonical Property</span></span>

  
  
<span data-ttu-id="b9089-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9089-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9089-105">Contient les heures pour lequel l’état libre/occupé est défini à absent du bureau.</span><span class="sxs-lookup"><span data-stu-id="b9089-105">Contains the times for which the free/busy status is set to OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b9089-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="b9089-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="b9089-107">PR_SCHDINFO_FREEBUSY_OOF</span><span class="sxs-lookup"><span data-stu-id="b9089-107">PR_SCHDINFO_FREEBUSY_OOF</span></span>  <br/> |
|<span data-ttu-id="b9089-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="b9089-108">Identifier:</span></span>  <br/> |<span data-ttu-id="b9089-109">0x6856</span><span class="sxs-lookup"><span data-stu-id="b9089-109">0x6856</span></span>  <br/> |
|<span data-ttu-id="b9089-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="b9089-110">Data type:</span></span>  <br/> |<span data-ttu-id="b9089-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="b9089-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="b9089-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="b9089-112">Area:</span></span>  <br/> |<span data-ttu-id="b9089-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="b9089-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b9089-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="b9089-114">Remarks</span></span>

<span data-ttu-id="b9089-115">Format, calcul les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) mais faire référence à un rendez-vous qui sont marqués absent du bureau dans le calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="b9089-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="b9089-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="b9089-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="b9089-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="b9089-117">Protocol specifications</span></span>

<span data-ttu-id="b9089-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9089-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9089-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="b9089-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="b9089-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="b9089-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="b9089-121">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="b9089-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="b9089-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="b9089-122">Header files</span></span>

<span data-ttu-id="b9089-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="b9089-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="b9089-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="b9089-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="b9089-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="b9089-125">Mapitags.h</span></span>
  
> <span data-ttu-id="b9089-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="b9089-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9089-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b9089-127">See also</span></span>



[<span data-ttu-id="b9089-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="b9089-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="b9089-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="b9089-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="b9089-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="b9089-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="b9089-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="b9089-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

