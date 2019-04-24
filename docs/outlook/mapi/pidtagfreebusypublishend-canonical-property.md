---
title: Propriété canonique PidTagFreeBusyPublishEnd
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFreeBusyPublishEnd
api_type:
- HeaderDef
ms.assetid: df239741-6a63-4cd4-9bbb-42c0f5c668a5
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 3b4a8cb7136eee914dc697d24e0374ccb4b6f8b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316183"
---
# <a name="pidtagfreebusypublishend-canonical-property"></a><span data-ttu-id="907a2-103">Propriété canonique PidTagFreeBusyPublishEnd</span><span class="sxs-lookup"><span data-stu-id="907a2-103">PidTagFreeBusyPublishEnd Canonical Property</span></span>

  
  
<span data-ttu-id="907a2-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="907a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="907a2-105">Contient l'heure de fin de la plage de publication.</span><span class="sxs-lookup"><span data-stu-id="907a2-105">Contains the end time of the publishing range.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="907a2-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="907a2-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="907a2-107">PR_FREEBUSY_PUBLISH_END</span><span class="sxs-lookup"><span data-stu-id="907a2-107">PR_FREEBUSY_PUBLISH_END</span></span>  <br/> |
|<span data-ttu-id="907a2-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="907a2-108">Identifier:</span></span>  <br/> |<span data-ttu-id="907a2-109">0x6848</span><span class="sxs-lookup"><span data-stu-id="907a2-109">0x6848</span></span>  <br/> |
|<span data-ttu-id="907a2-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="907a2-110">Data type:</span></span>  <br/> |<span data-ttu-id="907a2-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="907a2-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="907a2-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="907a2-112">Area:</span></span>  <br/> |<span data-ttu-id="907a2-113">Disponibilité</span><span class="sxs-lookup"><span data-stu-id="907a2-113">Free/Busy</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="907a2-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="907a2-114">Remarks</span></span>

<span data-ttu-id="907a2-115">La valeur de cette propriété est calculée en ajoutant la valeur de **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) à la date de début de la plage de publication.</span><span class="sxs-lookup"><span data-stu-id="907a2-115">The value for this property is computed by adding the value of **PR_FREEBUSY_COUNT_MONTHS** ([PidTagFreeBusyCountMonths](pidtagfreebusycountmonths-canonical-property.md)) to the start date of the publishing range.</span></span> <span data-ttu-id="907a2-116">Cette valeur est exprimée en nombre de minutes écoulées depuis minuit, le 1er janvier 1601 en temps universel coordonné (UTC).</span><span class="sxs-lookup"><span data-stu-id="907a2-116">This value is expressed as the number of minutes since midnight, January 1, 1601 in Coordinated Universal Time (UTC).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="907a2-117">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="907a2-117">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="907a2-118">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="907a2-118">Protocol specifications</span></span>

<span data-ttu-id="907a2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="907a2-119">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="907a2-120">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="907a2-120">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="907a2-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="907a2-121">[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="907a2-122">Publie la disponibilité d'un utilisateur ou d'une ressource.</span><span class="sxs-lookup"><span data-stu-id="907a2-122">Publishes the availability of a user or resource.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="907a2-123">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="907a2-123">Header files</span></span>

<span data-ttu-id="907a2-124">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="907a2-124">Mapidefs.h</span></span>
  
> <span data-ttu-id="907a2-125">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="907a2-125">Provides data type definitions.</span></span>
    
<span data-ttu-id="907a2-126">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="907a2-126">Mapitags.h</span></span>
  
> <span data-ttu-id="907a2-127">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="907a2-127">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="907a2-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="907a2-128">See also</span></span>



[<span data-ttu-id="907a2-129">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="907a2-129">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="907a2-130">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="907a2-130">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="907a2-131">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="907a2-131">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="907a2-132">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="907a2-132">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

