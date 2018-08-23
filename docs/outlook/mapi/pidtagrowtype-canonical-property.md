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
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 6e856cc8dc131c1b6266181a954a8da9cfb1d1ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566102"
---
# <a name="pidtagrowtype-canonical-property"></a><span data-ttu-id="f7ece-103">Propriété canonique PidTagRowType</span><span class="sxs-lookup"><span data-stu-id="f7ece-103">PidTagRowType Canonical Property</span></span>

  
  
<span data-ttu-id="f7ece-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f7ece-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f7ece-105">Contient une valeur qui indique le type d’une ligne dans une table.</span><span class="sxs-lookup"><span data-stu-id="f7ece-105">Contains a value that indicates the type of a row in a table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f7ece-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="f7ece-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="f7ece-107">PR_ROW_TYPE</span><span class="sxs-lookup"><span data-stu-id="f7ece-107">PR_ROW_TYPE</span></span>  <br/> |
|<span data-ttu-id="f7ece-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="f7ece-108">Identifier:</span></span>  <br/> |<span data-ttu-id="f7ece-109">0x0FF5</span><span class="sxs-lookup"><span data-stu-id="f7ece-109">0x0FF5</span></span>  <br/> |
|<span data-ttu-id="f7ece-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="f7ece-110">Data type:</span></span>  <br/> |<span data-ttu-id="f7ece-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="f7ece-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="f7ece-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="f7ece-112">Area:</span></span>  <br/> |<span data-ttu-id="f7ece-113">MAPI non transmissible</span><span class="sxs-lookup"><span data-stu-id="f7ece-113">MAPI non-transmittable</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f7ece-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="f7ece-114">Remarks</span></span>

<span data-ttu-id="f7ece-115">Cette propriété s’affiche uniquement sur des tables des matières.</span><span class="sxs-lookup"><span data-stu-id="f7ece-115">This property appears only on contents tables.</span></span> <span data-ttu-id="f7ece-116">Une catégorie existe uniquement lorsqu’il a des éléments.</span><span class="sxs-lookup"><span data-stu-id="f7ece-116">A category only exists when it has items.</span></span>
  
<span data-ttu-id="f7ece-117">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="f7ece-117">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="f7ece-118">TBL_LEAF_ROW</span><span class="sxs-lookup"><span data-stu-id="f7ece-118">TBL_LEAF_ROW</span></span> 
  
> <span data-ttu-id="f7ece-119">Représente les données réelles, plutôt qu’une ligne de la catégorie.</span><span class="sxs-lookup"><span data-stu-id="f7ece-119">Represents actual data, rather than a category row.</span></span>
    
<span data-ttu-id="f7ece-120">TBL_EMPTY_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f7ece-120">TBL_EMPTY_CATEGORY</span></span> 
  
> <span data-ttu-id="f7ece-121">N’est actuellement pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="f7ece-121">Not currently used.</span></span>
    
<span data-ttu-id="f7ece-122">TBL_EXPANDED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f7ece-122">TBL_EXPANDED_CATEGORY</span></span> 
  
> <span data-ttu-id="f7ece-123">La catégorie est développée ; l’interface utilisateur affiche généralement avec le signe moins (-) à côté d’elle.</span><span class="sxs-lookup"><span data-stu-id="f7ece-123">The category is expanded; the user interface usually displays this with the minus sign ( - ) next to it.</span></span>
    
<span data-ttu-id="f7ece-124">TBL_COLLAPSED_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="f7ece-124">TBL_COLLAPSED_CATEGORY</span></span> 
  
> <span data-ttu-id="f7ece-125">La catégorie est réduite ; l’interface utilisateur affiche généralement avec le signe plus (+) en regard de son.</span><span class="sxs-lookup"><span data-stu-id="f7ece-125">The category is collapsed; the user interface usually displays this with the plus sign (+) next to it.</span></span>
    
## <a name="related-resources"></a><span data-ttu-id="f7ece-126">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="f7ece-126">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="f7ece-127">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="f7ece-127">Protocol specifications</span></span>

<span data-ttu-id="f7ece-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="f7ece-128">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="f7ece-129">Inclut les opérations autorisées pour les objets de la table principale.</span><span class="sxs-lookup"><span data-stu-id="f7ece-129">Includes permissible operations for the core table objects.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="f7ece-130">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="f7ece-130">Header files</span></span>

<span data-ttu-id="f7ece-131">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="f7ece-131">Mapidefs.h</span></span>
  
> <span data-ttu-id="f7ece-132">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="f7ece-132">Provides data type definitions.</span></span>
    
<span data-ttu-id="f7ece-133">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="f7ece-133">Mapitags.h</span></span>
  
> <span data-ttu-id="f7ece-134">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="f7ece-134">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="f7ece-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f7ece-135">See also</span></span>



[<span data-ttu-id="f7ece-136">Propriété canonique PidTagRowid</span><span class="sxs-lookup"><span data-stu-id="f7ece-136">PidTagRowid Canonical Property</span></span>](pidtagrowid-canonical-property.md)


[<span data-ttu-id="f7ece-137">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ece-137">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="f7ece-138">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ece-138">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="f7ece-139">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="f7ece-139">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="f7ece-140">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="f7ece-140">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

