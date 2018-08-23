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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 7723897c6d249bbb53a0de5aa68ad8d1bc79830f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563724"
---
# <a name="pidtagscheduleinfomonthsbusy-canonical-property"></a><span data-ttu-id="c10eb-103">Propriété canonique PidTagScheduleInfoMonthsBusy</span><span class="sxs-lookup"><span data-stu-id="c10eb-103">PidTagScheduleInfoMonthsBusy Canonical Property</span></span>

  
  
<span data-ttu-id="c10eb-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c10eb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c10eb-105">Contient les mois dont sont présentes dans le message et de disponibilité et de disponibilité des données de type occupé (e).</span><span class="sxs-lookup"><span data-stu-id="c10eb-105">Contains the months for which free/busy data of type busy is present in the free/busy message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c10eb-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="c10eb-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="c10eb-107">PR_SCHDINFO_MONTHS_BUSY</span><span class="sxs-lookup"><span data-stu-id="c10eb-107">PR_SCHDINFO_MONTHS_BUSY</span></span>  <br/> |
|<span data-ttu-id="c10eb-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="c10eb-108">Identifier:</span></span>  <br/> |<span data-ttu-id="c10eb-109">0x6853</span><span class="sxs-lookup"><span data-stu-id="c10eb-109">0x6853</span></span>  <br/> |
|<span data-ttu-id="c10eb-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="c10eb-110">Data type:</span></span>  <br/> |<span data-ttu-id="c10eb-111">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="c10eb-111">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="c10eb-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="c10eb-112">Area:</span></span>  <br/> |<span data-ttu-id="c10eb-113">Informations de disponibilité</span><span class="sxs-lookup"><span data-stu-id="c10eb-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c10eb-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c10eb-114">Remarks</span></span>

<span data-ttu-id="c10eb-115">Format, calcul les contraintes de cette propriété sont les mêmes que ceux du **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) mais faire référence à des rendez-vous sont marquées comme occupé (e) sur l’objet calendar associé.</span><span class="sxs-lookup"><span data-stu-id="c10eb-115">The format, computation and constraints of this property are the same as those of **PR_SCHDINFO_MONTHS_TENTATIVE** ([PidTagScheduleInfoMonthsTentative](pidtagscheduleinfomonthstentative-canonical-property.md)) but refer to appointments that are marked busy on the associated calendar object.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c10eb-116">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="c10eb-116">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c10eb-117">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="c10eb-117">Protocol specifications</span></span>

<span data-ttu-id="c10eb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c10eb-118">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c10eb-119">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="c10eb-119">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="c10eb-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="c10eb-120">[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="c10eb-121">Publie la disponibilité d’un utilisateur ou une ressource.</span><span class="sxs-lookup"><span data-stu-id="c10eb-121">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c10eb-122">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="c10eb-122">Header files</span></span>

<span data-ttu-id="c10eb-123">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c10eb-123">Mapidefs.h</span></span>
  
> <span data-ttu-id="c10eb-124">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="c10eb-124">Provides data type definitions.</span></span>
    
<span data-ttu-id="c10eb-125">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="c10eb-125">Mapitags.h</span></span>
  
> <span data-ttu-id="c10eb-126">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="c10eb-126">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c10eb-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c10eb-127">See also</span></span>



[<span data-ttu-id="c10eb-128">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="c10eb-128">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c10eb-129">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="c10eb-129">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c10eb-130">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="c10eb-130">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c10eb-131">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="c10eb-131">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

