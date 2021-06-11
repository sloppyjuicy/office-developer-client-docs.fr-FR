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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338716"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="60522-103">Propriété canonique PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="60522-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="60522-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60522-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60522-105">Contient les heures pendant lesquelles l’état de la période de libre/occupé est occupé ou d’absence du travail.</span><span class="sxs-lookup"><span data-stu-id="60522-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60522-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="60522-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="60522-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="60522-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="60522-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="60522-108">Identifier:</span></span>  <br/> |<span data-ttu-id="60522-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="60522-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="60522-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="60522-110">Data type:</span></span>  <br/> |<span data-ttu-id="60522-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="60522-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="60522-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="60522-112">Area:</span></span>  <br/> |<span data-ttu-id="60522-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="60522-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60522-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="60522-114">Remarks</span></span>

<span data-ttu-id="60522-115">Les événements de type de libre/occupé provisoire ne sont pas inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="60522-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="60522-116">Le format, le calcul et les restrictions de cette propriété sont identiques à ceux de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mais font référence aux rendez-vous marqués comme étant des absences du calendrier ou occupés sur le calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="60522-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="60522-117">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="60522-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="60522-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="60522-118">Protocol specifications</span></span>

<span data-ttu-id="60522-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60522-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60522-120">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="60522-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="60522-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="60522-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="60522-122">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="60522-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="60522-123">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="60522-123">Header files</span></span>

<span data-ttu-id="60522-124">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60522-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="60522-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="60522-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="60522-126">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="60522-126">Mapitags.h</span></span>
  
> <span data-ttu-id="60522-127">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="60522-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60522-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="60522-128">See also</span></span>



[<span data-ttu-id="60522-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="60522-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60522-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="60522-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60522-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="60522-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60522-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="60522-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

