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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 18bc41d9038113b5b813f1cfd02d90b8e982703c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359773"
---
# <a name="pidtagscheduleinfofreebusytentative-canonical-property"></a><span data-ttu-id="e1141-103">Propriété canonique PidTagScheduleInfoFreeBusyTentative</span><span class="sxs-lookup"><span data-stu-id="e1141-103">PidTagScheduleInfoFreeBusyTentative Canonical Property</span></span>

  
  
<span data-ttu-id="e1141-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1141-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e1141-105">Contient les blocs de heures pour lesquels l’état de libre/occupé est provisoire.</span><span class="sxs-lookup"><span data-stu-id="e1141-105">Contains the blocks of times for which the free/busy status is tentative.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e1141-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e1141-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e1141-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span><span class="sxs-lookup"><span data-stu-id="e1141-107">PR_SCHDINFO_FREEBUSY_TENTATIVE</span></span>  <br/> |
|<span data-ttu-id="e1141-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e1141-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e1141-109">0x6852</span><span class="sxs-lookup"><span data-stu-id="e1141-109">0x6852</span></span>  <br/> |
|<span data-ttu-id="e1141-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e1141-110">Data type:</span></span>  <br/> |<span data-ttu-id="e1141-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="e1141-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="e1141-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="e1141-112">Area:</span></span>  <br/> |<span data-ttu-id="e1141-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="e1141-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1141-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1141-114">Remarks</span></span>

<span data-ttu-id="e1141-115">Cette propriété a autant de valeurs que le nombre de valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="e1141-115">This property has as many values as the number of values in **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)).</span></span> <span data-ttu-id="e1141-116">Chaque valeur binaire représente un mois et correspond à la valeur au même index dans **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="e1141-116">Each binary value represents a month and corresponds to the value at the same index in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span> <span data-ttu-id="e1141-117">Les valeurs binaires sont triées dans le même ordre que les valeurs dans **PR_SCHDINFO_MONTHS_TENTATIVE**.</span><span class="sxs-lookup"><span data-stu-id="e1141-117">The binary values are sorted in the same order as the values in **PR_SCHDINFO_MONTHS_TENTATIVE**.</span></span>
  
<span data-ttu-id="e1141-118">Chaque valeur binaire comporte un ou plusieurs blocs de 4 octets et chacun d’eux contient l’heure de début dans les deux premiers octets et l’heure de fin dans les deux deuxièmes octets au format little-endian.</span><span class="sxs-lookup"><span data-stu-id="e1141-118">Each binary value has one or more 4-BYTE blocks and each of them contains the start time in the first two bytes and end time in the second two bytes in little-endian format.</span></span> <span data-ttu-id="e1141-119">L’heure de début est le nombre de minutes entre l’heure UTC (Temps universel coordonné) de minuit du premier jour du mois et l’heure de début de l’événement en UTC.</span><span class="sxs-lookup"><span data-stu-id="e1141-119">The start time is the number of minutes between midnight Coordinated Universal Time (UTC) of the first day of the month and the start time of the event in UTC.</span></span> <span data-ttu-id="e1141-120">L’heure de fin est le nombre de minutes entre minuit UTC du premier jour du mois et l’heure de fin de l’événement en UTC.</span><span class="sxs-lookup"><span data-stu-id="e1141-120">The end time is the number of minutes between midnight UTC of the first day of the month and the end time of the event in UTC.</span></span> <span data-ttu-id="e1141-121">Les blocs 4-BYTE sont triés dans l’ordre croissant.</span><span class="sxs-lookup"><span data-stu-id="e1141-121">The 4-BYTE blocks are sorted in ascending order.</span></span>
  
<span data-ttu-id="e1141-122">Les blocs de temps consécutifs ou qui se chevauchent sont fusionnés en un seul bloc avec l’heure de début comme heure de début du premier bloc et l’heure de fin comme heure de fin du dernier bloc.</span><span class="sxs-lookup"><span data-stu-id="e1141-122">Consecutive or overlapping blocks of time are merged into one block with start time as the start time of the first block and end time as the end time of the last block.</span></span> <span data-ttu-id="e1141-123">Si un événement est réparti sur plusieurs mois ou années, l’événement est divisé en plusieurs blocs, un par mois.</span><span class="sxs-lookup"><span data-stu-id="e1141-123">If an event is spread across multiple months or years, the event is split into multiple blocks, one for each month.</span></span> <span data-ttu-id="e1141-124">S’il n’existe aucun événement provisoire dans  la plage de publication, cette propriété et cette PR_SCHDINFO_MONTHS_TENTATIVE ne doivent pas être définies ou supprimées s’ils existent déjà.</span><span class="sxs-lookup"><span data-stu-id="e1141-124">If there are no tentative events in the publishing range, then this property and **PR_SCHDINFO_MONTHS_TENTATIVE** must not be set or must be deleted if they already exist.</span></span> <span data-ttu-id="e1141-125">Sinon, cette propriété doit être définie.</span><span class="sxs-lookup"><span data-stu-id="e1141-125">Otherwise, this property must be set.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e1141-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e1141-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e1141-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="e1141-127">Protocol specifications</span></span>

<span data-ttu-id="e1141-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1141-128">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1141-129">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="e1141-129">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e1141-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e1141-130">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e1141-131">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="e1141-131">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e1141-132">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e1141-132">Header files</span></span>

<span data-ttu-id="e1141-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e1141-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="e1141-134">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e1141-134">Provides data type definitions.</span></span>
    
<span data-ttu-id="e1141-135">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e1141-135">Mapitags.h</span></span>
  
> <span data-ttu-id="e1141-136">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="e1141-136">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e1141-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e1141-137">See also</span></span>



[<span data-ttu-id="e1141-138">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e1141-138">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e1141-139">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e1141-139">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e1141-140">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e1141-140">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e1141-141">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="e1141-141">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

