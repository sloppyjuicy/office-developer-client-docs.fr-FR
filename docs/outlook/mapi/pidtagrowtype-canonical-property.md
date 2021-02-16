---
title: Propriété canonique PidTagRowType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRowType
api_type:
- COM
ms.assetid: d57ce5c8-1f60-4709-b86a-4468c4208dfe
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 962e8c92ae61e8b60862a3ae26a7cdfbf5034e89
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359513"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="00c98-103">Propriété canonique PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="00c98-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="00c98-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00c98-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00c98-105">Contient une valeur qui indique le type d’une ligne dans un tableau.</span><span class="sxs-lookup"><span data-stu-id="00c98-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="00c98-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="00c98-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="00c98-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="00c98-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="00c98-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="00c98-108">Identifier:</span></span>  <br/> |<span data-ttu-id="00c98-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="00c98-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="00c98-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="00c98-110">Data type:</span></span>  <br/> |<span data-ttu-id="00c98-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="00c98-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="00c98-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="00c98-112">Area:</span></span>  <br/> |<span data-ttu-id="00c98-113">MAPI non transmetteable</span><span class="sxs-lookup"><span data-stu-id="00c98-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00c98-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="00c98-114">Remarks</span></span>

<span data-ttu-id="00c98-115">Cette propriété apparaît uniquement dans les tables des matières.</span><span class="sxs-lookup"><span data-stu-id="00c98-115">This property appears only on contents tables.</span></span> <span data-ttu-id="00c98-116">Une catégorie n’existe que lorsqu’elle possède des éléments.</span><span class="sxs-lookup"><span data-stu-id="00c98-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="00c98-117">Cette propriété peut avoir exactement l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="00c98-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="00c98-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="00c98-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="00c98-119">Représente les données réelles, plutôt qu’une ligne de catégorie.</span><span class="sxs-lookup"><span data-stu-id="00c98-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="00c98-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="00c98-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="00c98-121">Non utilisé actuellement.</span><span class="sxs-lookup"><span data-stu-id="00c98-121">Not currently used.</span></span>
    
<span data-ttu-id="00c98-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="00c98-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="00c98-123">La catégorie est étendue . L’interface utilisateur l’affiche généralement avec le signe moins ( - ) en face de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="00c98-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="00c98-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="00c98-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="00c98-125">La catégorie est réduire . L’interface utilisateur l’affiche généralement avec le signe plus (+) à côté de celle-ci.</span><span class="sxs-lookup"><span data-stu-id="00c98-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="00c98-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="00c98-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="00c98-127">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="00c98-127">Protocol specifications</span></span>

<span data-ttu-id="00c98-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00c98-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="00c98-129">Inclut les opérations autorisées pour les objets de table principale.</span><span class="sxs-lookup"><span data-stu-id="00c98-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="00c98-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="00c98-130">Header files</span></span>

<span data-ttu-id="00c98-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="00c98-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="00c98-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="00c98-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="00c98-133">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="00c98-133">Mapitags.h</span></span>
  
> <span data-ttu-id="00c98-134">Contient les définitions des propriétés répertoriées en tant que noms de remplacement.</span><span class="sxs-lookup"><span data-stu-id="00c98-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="00c98-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="00c98-135">See also</span></span>



[<span data-ttu-id="00c98-136">Propriété canonique PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="00c98-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="00c98-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="00c98-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="00c98-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="00c98-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="00c98-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="00c98-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="00c98-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="00c98-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

