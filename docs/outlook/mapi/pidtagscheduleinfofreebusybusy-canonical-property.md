---
title: Propriété canonique PidTagScheduleInfoFreeBusyBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoFreeBusyBusy
api_type:
- COM
ms.assetid: 84d9c5b5-e734-4c07-b4cc-1d7b13c1ed19
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 4fbf0d8b80fdb48e44480b2739a71aec43b88a05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338653"
---
# <a name="pidtagscheduleinfofreebusybusy-canonical-property"></a><span data-ttu-id="a7dea-103">Propriété canonique PidTagScheduleInfoFreeBusyBusy</span><span class="sxs-lookup"><span data-stu-id="a7dea-103">PidTagScheduleInfoFreeBusyBusy Canonical Property</span></span>

  
  
<span data-ttu-id="a7dea-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a7dea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a7dea-105">Contient les blocs de temps pour lesquels l’état est occupé.</span><span class="sxs-lookup"><span data-stu-id="a7dea-105">Contains the blocks of time for which the status is busy.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a7dea-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a7dea-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a7dea-107">PR_SCHDINFO_FREEBUSY_BUSY</span><span class="sxs-lookup"><span data-stu-id="a7dea-107">PR_SCHDINFO_FREEBUSY_BUSY</span></span>  <br/> |
|<span data-ttu-id="a7dea-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a7dea-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a7dea-109">0x6854</span><span class="sxs-lookup"><span data-stu-id="a7dea-109">0x6854</span></span>  <br/> |
|<span data-ttu-id="a7dea-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a7dea-110">Data type:</span></span>  <br/> |<span data-ttu-id="a7dea-111">PT_MV_BINARY</span><span class="sxs-lookup"><span data-stu-id="a7dea-111">PT_MV_BINARY</span></span>  <br/> |
|<span data-ttu-id="a7dea-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="a7dea-112">Area:</span></span>  <br/> |<span data-ttu-id="a7dea-113">Libre/Occupé</span><span class="sxs-lookup"><span data-stu-id="a7dea-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7dea-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a7dea-114">Remarks</span></span>

<span data-ttu-id="a7dea-115">Le format, le calcul et les contraintes de cette propriété sont identiques à ceux de **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)), mais font référence aux rendez-vous qui sont marqués comme occupés sur l’objet calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="a7dea-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_FREEBUSY_TENTATIVE** ([PidTagScheduleInfoFreeBusyTentative](pidtagscheduleinfofreebusytentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a7dea-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a7dea-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a7dea-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="a7dea-117">Protocol specifications</span></span>

<span data-ttu-id="a7dea-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7dea-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7dea-119">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="a7dea-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a7dea-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a7dea-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a7dea-121">Publie la disponibilité d’un utilisateur ou d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="a7dea-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a7dea-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a7dea-122">Header files</span></span>

<span data-ttu-id="a7dea-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a7dea-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="a7dea-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a7dea-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="a7dea-125">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="a7dea-125">Mapitags.h</span></span>
  
> <span data-ttu-id="a7dea-126">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="a7dea-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a7dea-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7dea-127">See also</span></span>



[<span data-ttu-id="a7dea-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a7dea-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a7dea-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a7dea-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a7dea-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a7dea-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a7dea-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="a7dea-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

