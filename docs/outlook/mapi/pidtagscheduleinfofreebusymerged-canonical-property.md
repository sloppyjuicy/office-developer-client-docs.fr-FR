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
ms.openlocfilehash: 8d15c6cb256fb1e80e3c94bdfe7e71bd8625aa35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338716"
---
# <a name="pidtagscheduleinfofreebusymerged-canonical-property"></a><span data-ttu-id="70c63-103">Propriété canonique PidTagScheduleInfoFreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="70c63-103">PidTagScheduleInfoFreeBusyMerged Canonical Property</span></span>

  
  
<span data-ttu-id="70c63-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70c63-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70c63-105">Contient les heures pour lesquelles l'état de disponibilité est défini sur occupé ou OOF.</span><span class="sxs-lookup"><span data-stu-id="70c63-105">Contains the times for which the free/busy status is set to busy or OOF.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="70c63-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="70c63-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="70c63-107">PR_SCHDINFO_FREEBUSY_MERGED</span><span class="sxs-lookup"><span data-stu-id="70c63-107">PR_SCHDINFO_FREEBUSY_MERGED</span></span>  <br/> |
|<span data-ttu-id="70c63-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="70c63-108">Identifier:</span></span>  <br/> |<span data-ttu-id="70c63-109">0x6850</span><span class="sxs-lookup"><span data-stu-id="70c63-109">0x6850</span></span>  <br/> |
|<span data-ttu-id="70c63-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="70c63-110">Data type:</span></span>  <br/> |<span data-ttu-id="70c63-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="70c63-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="70c63-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="70c63-112">Area:</span></span>  <br/> |<span data-ttu-id="70c63-113">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="70c63-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70c63-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="70c63-114">Remarks</span></span>

<span data-ttu-id="70c63-115">Les événements de type de disponibilité provisoire ne sont pas inclus dans cette propriété.</span><span class="sxs-lookup"><span data-stu-id="70c63-115">Events of free/busy type tentative are not included in this property.</span></span> <span data-ttu-id="70c63-116">Le format, le calcul et les restrictions de cette propriété sont les mêmes que ceux de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mais font référence à des rendez-vous marqués comme absent (e) ou occupé (e) sur le calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="70c63-116">The format, computation and the restrictions of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked OOF or busy on the associated calendar.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="70c63-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="70c63-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="70c63-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="70c63-118">Protocol specifications</span></span>

<span data-ttu-id="70c63-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70c63-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70c63-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="70c63-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="70c63-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="70c63-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="70c63-122">Publie la disponibilité d'un utilisateur ou d'une ressource.</span><span class="sxs-lookup"><span data-stu-id="70c63-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="70c63-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="70c63-123">Header files</span></span>

<span data-ttu-id="70c63-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="70c63-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="70c63-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="70c63-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="70c63-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="70c63-126">Mapitags.h</span></span>
  
> <span data-ttu-id="70c63-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="70c63-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="70c63-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="70c63-128">See also</span></span>



[<span data-ttu-id="70c63-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="70c63-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="70c63-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="70c63-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="70c63-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="70c63-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="70c63-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="70c63-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

