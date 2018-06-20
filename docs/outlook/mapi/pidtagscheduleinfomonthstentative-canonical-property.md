---
title: Propriété canonique PidTagScheduleInfoMonthsTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoMonthsTentative
api_type:
- COM
ms.assetid: 3179442c-6499-464a-93af-eb0a7a5b0d30
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 20620a5835e627eb7543a03037f9be75db6739ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786723"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="c7358-103">Propriété canonique PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="c7358-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="c7358-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c7358-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c7358-105">Contient les mois marqués provisoires dans le message et de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="c7358-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c7358-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c7358-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c7358-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="c7358-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="c7358-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c7358-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c7358-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="c7358-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="c7358-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c7358-110">Data type:</span></span>  <br/> |<span data-ttu-id="c7358-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c7358-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c7358-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="c7358-112">Area:</span></span>  <br/> |<span data-ttu-id="c7358-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="c7358-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7358-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c7358-114">Remarks</span></span>

<span data-ttu-id="c7358-115">Le nombre de valeurs dans cette propriété doit être comprise entre 0 et le nombre de mois couverts par la plage de publication, qui est la période entre la **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) et **PR_FREEBUSY_PUBLISH_END **Propriétés ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="c7358-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="c7358-116">Chaque valeur de cette propriété, a un mois et l’année codé de celui-ci.</span><span class="sxs-lookup"><span data-stu-id="c7358-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="c7358-117">Il est calculé à l’aide de l’expression « an x 16 + mois » où les mois et année sont basées sur le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="c7358-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="c7358-118">Les valeurs sont triées par ordre croissant et sont encodés au format little-endian.</span><span class="sxs-lookup"><span data-stu-id="c7358-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="c7358-119">Si un événement s’étend sur plusieurs mois ou plusieurs années, il doit être une valeur pour chacun des mois qui figurent dans la plage de publication.</span><span class="sxs-lookup"><span data-stu-id="c7358-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="c7358-120">S’il n’y a aucun événement provisoire dans la plage de publication, cette propriété et la **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) ne doivent pas être définie, ou doivent être supprimés s’ils existent déjà.</span><span class="sxs-lookup"><span data-stu-id="c7358-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="c7358-121">Dans le cas contraire, cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="c7358-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c7358-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c7358-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c7358-123">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c7358-123">Protocol specifications</span></span>

<span data-ttu-id="c7358-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7358-124">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7358-125">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c7358-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c7358-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c7358-126">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c7358-127">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="c7358-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c7358-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c7358-128">Header files</span></span>

<span data-ttu-id="c7358-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c7358-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="c7358-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c7358-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="c7358-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c7358-131">Mapitags.h</span></span>
  
> <span data-ttu-id="c7358-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c7358-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7358-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7358-133">See also</span></span>



[<span data-ttu-id="c7358-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c7358-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c7358-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c7358-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c7358-136">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c7358-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c7358-137">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="c7358-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

