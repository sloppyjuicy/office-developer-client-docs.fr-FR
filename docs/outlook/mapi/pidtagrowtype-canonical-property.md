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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383064"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="21ff4-103">Propriété canonique PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="21ff4-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="21ff4-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="21ff4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="21ff4-105">Contient une valeur qui indique le type d’une ligne dans une table.</span><span class="sxs-lookup"><span data-stu-id="21ff4-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="21ff4-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="21ff4-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="21ff4-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="21ff4-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="21ff4-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="21ff4-108">Identifier:</span></span>  <br/> |<span data-ttu-id="21ff4-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="21ff4-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="21ff4-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="21ff4-110">Data type:</span></span>  <br/> |<span data-ttu-id="21ff4-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="21ff4-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="21ff4-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="21ff4-112">Area:</span></span>  <br/> |<span data-ttu-id="21ff4-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="21ff4-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21ff4-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="21ff4-114">Remarks</span></span>

<span data-ttu-id="21ff4-115">Cette propriété s’affiche uniquement sur des tables des matières.</span><span class="sxs-lookup"><span data-stu-id="21ff4-115">This property appears only on contents tables.</span></span> <span data-ttu-id="21ff4-116">Une catégorie existe uniquement lorsqu’il a des éléments.</span><span class="sxs-lookup"><span data-stu-id="21ff4-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="21ff4-117">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="21ff4-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="21ff4-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="21ff4-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="21ff4-119">Représente les données réelles, plutôt qu’une ligne de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="21ff4-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="21ff4-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="21ff4-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="21ff4-121">N’est actuellement pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="21ff4-121">Not currently used.</span></span>
    
<span data-ttu-id="21ff4-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="21ff4-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="21ff4-123">La catégorie est développée ; l’interface utilisateur affiche généralement avec le signe moins (-) à côté d’elle.</span><span class="sxs-lookup"><span data-stu-id="21ff4-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="21ff4-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="21ff4-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="21ff4-125">La catégorie est réduite ; l’interface utilisateur affiche généralement avec le signe plus (+) en regard de son.</span><span class="sxs-lookup"><span data-stu-id="21ff4-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="21ff4-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="21ff4-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="21ff4-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="21ff4-127">Protocol specifications</span></span>

<span data-ttu-id="21ff4-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="21ff4-128">[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="21ff4-129">Inclut les opérations autorisées pour les objets de la table principale.</span><span class="sxs-lookup"><span data-stu-id="21ff4-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="21ff4-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="21ff4-130">Header files</span></span>

<span data-ttu-id="21ff4-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="21ff4-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="21ff4-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="21ff4-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="21ff4-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="21ff4-133">Mapitags.h</span></span>
  
> <span data-ttu-id="21ff4-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="21ff4-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="21ff4-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21ff4-135">See also</span></span>



[<span data-ttu-id="21ff4-136">Propriété canonique PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="21ff4-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="21ff4-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="21ff4-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="21ff4-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="21ff4-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="21ff4-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="21ff4-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="21ff4-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="21ff4-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

