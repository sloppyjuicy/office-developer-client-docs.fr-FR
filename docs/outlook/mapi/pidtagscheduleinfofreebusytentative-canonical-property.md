---
title: Propriété canonique PidTagScheduleInfoFreeBusyTentative
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyTentative
api_type:
- COM
ms.assetid: 28453d29-30c5-405b-84d2-5bb5f281756c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a00505b765abdcb7b8fe9d68052774b30bbdf692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786726"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="aef4f-103">Propriété canonique PidTagScheduleInfoFreeBusyTentative</span><span class="sxs-lookup"><span data-stu-id="aef4f-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="aef4f-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aef4f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aef4f-105">Contient les blocs de temps pour lequel l’état de disponibilité est provisoire.</span><span class="sxs-lookup"><span data-stu-id="aef4f-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="aef4f-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="aef4f-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="aef4f-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="aef4f-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="aef4f-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="aef4f-108">Identifier:</span></span>  <br/> |<span data-ttu-id="aef4f-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="aef4f-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="aef4f-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="aef4f-110">Data type:</span></span>  <br/> |<span data-ttu-id="aef4f-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="aef4f-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="aef4f-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="aef4f-112">Area:</span></span>  <br/> |<span data-ttu-id="aef4f-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="aef4f-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aef4f-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="aef4f-114">Remarks</span></span>

<span data-ttu-id="aef4f-115">Cette propriété a les valeurs autant que le nombre de valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="aef4f-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="aef4f-116">Chaque valeur binaire représente un mois et correspond à la valeur dans le même index dans **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="aef4f-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="aef4f-117">Les valeurs binaires sont triés dans le même ordre que les valeurs de **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="aef4f-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="aef4f-118">Chaque valeur binaire a un ou plusieurs blocs de 4 octets et chacune d'entre elles contient l’heure de début dans les deux premiers octets et l’heure de fin dans les deux octets au format little-endian.</span><span class="sxs-lookup"><span data-stu-id="aef4f-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="aef4f-119">L’heure de début est le nombre de minutes entre minuit temps universel coordonné (UTC) du premier jour du mois et l’heure de début de l’événement au format UTC.</span><span class="sxs-lookup"><span data-stu-id="aef4f-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="aef4f-120">L’heure de fin est le nombre de minutes entre minuit UTC du premier jour du mois et l’heure de fin de l’événement au format UTC.</span><span class="sxs-lookup"><span data-stu-id="aef4f-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="aef4f-121">Les blocs de 4 octets sont triés par ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="aef4f-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="aef4f-122">Blocs consécutifs ou qui se chevauchent de temps sont fusionnés dans un bloc avec l’heure de début comme heure de début du premier bloc et heure de fin comme heure de fin du dernier bloc.</span><span class="sxs-lookup"><span data-stu-id="aef4f-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="aef4f-123">Si un événement s’étend sur plusieurs mois ou années, l’événement est divisée en plusieurs blocs, une pour chaque mois.</span><span class="sxs-lookup"><span data-stu-id="aef4f-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="aef4f-124">S’il n’y a aucun événement provisoire dans la plage de publication, cette propriété et la **PR_SCHDINFO_MONTHS_TENTATIVE** ne doivent pas être définie, ou doivent être supprimés s’ils existent déjà.</span><span class="sxs-lookup"><span data-stu-id="aef4f-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="aef4f-125">Dans le cas contraire, cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="aef4f-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="aef4f-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="aef4f-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="aef4f-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="aef4f-127">Protocol specifications</span></span>

<span data-ttu-id="aef4f-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aef4f-128">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aef4f-129">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="aef4f-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="aef4f-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="aef4f-130">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="aef4f-131">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="aef4f-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="aef4f-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="aef4f-132">Header files</span></span>

<span data-ttu-id="aef4f-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="aef4f-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="aef4f-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="aef4f-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="aef4f-135">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="aef4f-135">Mapitags.h</span></span>
  
> <span data-ttu-id="aef4f-136">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="aef4f-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="aef4f-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="aef4f-137">See also</span></span>



[<span data-ttu-id="aef4f-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="aef4f-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="aef4f-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="aef4f-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="aef4f-140">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="aef4f-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="aef4f-141">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="aef4f-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

