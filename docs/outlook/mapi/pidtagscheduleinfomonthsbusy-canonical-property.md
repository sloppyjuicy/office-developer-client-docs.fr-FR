---
title: Propriété canonique PidTagScheduleInfoMonthsBusy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: b15447d6-89aa-40ad-93fc-21fbfa5e3d0e
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 08f8f6e016ff08211bc10e80588ab33e83d6441b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359791"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="d8849-103">Propriété canonique PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="d8849-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="d8849-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8849-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8849-105">Contient les mois pour lesquels les données de disponibilité de type occupé sont présentes dans le message de disponibilité.</span><span class="sxs-lookup"><span data-stu-id="d8849-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8849-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="d8849-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="d8849-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="d8849-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="d8849-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="d8849-108">Identifier:</span></span>  <br/> |<span data-ttu-id="d8849-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="d8849-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="d8849-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="d8849-110">Data type:</span></span>  <br/> |<span data-ttu-id="d8849-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="d8849-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="d8849-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="d8849-112">Area:</span></span>  <br/> |<span data-ttu-id="d8849-113">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="d8849-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8849-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8849-114">Remarks</span></span>

<span data-ttu-id="d8849-115">Le format, le calcul et les contraintes de cette propriété sont les mêmes que ceux de **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)), mais font référence à des rendez-vous marqués comme occupés sur l'objet de calendrier associé.</span><span class="sxs-lookup"><span data-stu-id="d8849-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="d8849-116">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="d8849-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="d8849-117">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="d8849-117">Protocol specifications</span></span>

<span data-ttu-id="d8849-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8849-118">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8849-119">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="d8849-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="d8849-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="d8849-120">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="d8849-121">Publie la disponibilité d'un utilisateur ou d'une ressource.</span><span class="sxs-lookup"><span data-stu-id="d8849-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="d8849-122">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="d8849-122">Header files</span></span>

<span data-ttu-id="d8849-123">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="d8849-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="d8849-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="d8849-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="d8849-125">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="d8849-125">Mapitags.h</span></span>
  
> <span data-ttu-id="d8849-126">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="d8849-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="d8849-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d8849-127">See also</span></span>



[<span data-ttu-id="d8849-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="d8849-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="d8849-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="d8849-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="d8849-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="d8849-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="d8849-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="d8849-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

