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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 6fa0579dcd98a0d819e58e62d8a42cb2972a9d1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359758"
---
# <a name="pidtagscheduleinfomonthstentative-canonical-property"></a><span data-ttu-id="7ceec-103">Propriété canonique PidTagScheduleInfoMonthsTentative</span><span class="sxs-lookup"><span data-stu-id="7ceec-103">PidTagScheduleInfoMonthsTentative Canonical Property</span></span>

  
  
<span data-ttu-id="7ceec-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7ceec-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7ceec-105">Contient les mois marqués comme provisoires dans le message de libre/occupé.</span><span class="sxs-lookup"><span data-stu-id="7ceec-105">Contains the months marked tentative in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7ceec-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="7ceec-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="7ceec-107">PR_SCHDINFO_MONTHS_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="7ceec-107">PR_SCHDINFO_MONTHS_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="7ceec-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="7ceec-108">Identifier:</span></span>  <br/> |<span data-ttu-id="7ceec-109">0x6851</span><span class="sxs-lookup"><span data-stu-id="7ceec-109">0x6851</span></span>  <br/> |
|<span data-ttu-id="7ceec-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="7ceec-110">Data type:</span></span>  <br/> |<span data-ttu-id="7ceec-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="7ceec-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="7ceec-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="7ceec-112">Area:</span></span>  <br/> |<span data-ttu-id="7ceec-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="7ceec-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7ceec-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="7ceec-114">Remarks</span></span>

<span data-ttu-id="7ceec-115">Le nombre de valeurs de cette propriété doit être entre zéro et le nombre de mois couverts par la plage de publication, qui est la période entre les propriétés **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) et **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7ceec-115">The number of values in this property must be between zero and the number of months covered by the publishing range, which is the period between the **PR_FREEBUSY_PUBLISH_START** ([PidTagFreeBusyPublishStart](pidtagfreebusypublishstart-canonical-property.md)) and **PR_FREEBUSY_PUBLISH_END** ([PidTagFreeBusyPublishEnd](pidtagfreebusypublishend-canonical-property.md)) properties.</span></span>
  
<span data-ttu-id="7ceec-116">Chaque valeur de cette propriété est codée mois et année.</span><span class="sxs-lookup"><span data-stu-id="7ceec-116">Each value in this property, has a month and year encoded in it.</span></span> <span data-ttu-id="7ceec-117">Cette valeur est calculée à l’aide de l’expression « year × 16 + month », où l’année et le mois sont basés sur le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="7ceec-117">This is calculated by using the expression "year × 16 + month" where year and month are based on the Gregorian calendar.</span></span> <span data-ttu-id="7ceec-118">Les valeurs sont triées dans l’ordre croissant et sont codées au format little endian.</span><span class="sxs-lookup"><span data-stu-id="7ceec-118">The values are sorted in ascending order and are encoded in little-endian format.</span></span> <span data-ttu-id="7ceec-119">Si un événement est réparti sur plusieurs mois ou plusieurs années, il doit y avoir une valeur pour chacun des mois qui se trouve dans la plage de publication.</span><span class="sxs-lookup"><span data-stu-id="7ceec-119">If an event is spread across multiple months, or multiple years, there must be one value for each of the months that fall in the publishing range.</span></span> <span data-ttu-id="7ceec-120">S’il n’existe aucun événement provisoire dans la plage de publication, cette propriété et **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) ne doivent pas être définies ou supprimées s’ils existent déjà.</span><span class="sxs-lookup"><span data-stu-id="7ceec-120">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="7ceec-121">Sinon, cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="7ceec-121">Otherwise, this property must be set.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="7ceec-122">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="7ceec-122">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="7ceec-123">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="7ceec-123">Protocol specifications</span></span>

<span data-ttu-id="7ceec-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ceec-124">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ceec-125">Fournit des références aux spécifications Exchange Server de protocole associées.</span><span class="sxs-lookup"><span data-stu-id="7ceec-125">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="7ceec-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="7ceec-126">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="7ceec-127">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="7ceec-127">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="7ceec-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="7ceec-128">Header files</span></span>

<span data-ttu-id="7ceec-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="7ceec-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="7ceec-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="7ceec-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="7ceec-131">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="7ceec-131">Mapitags.h</span></span>
  
> <span data-ttu-id="7ceec-132">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="7ceec-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ceec-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7ceec-133">See also</span></span>



[<span data-ttu-id="7ceec-134">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="7ceec-134">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="7ceec-135">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="7ceec-135">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="7ceec-136">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="7ceec-136">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="7ceec-137">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="7ceec-137">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

