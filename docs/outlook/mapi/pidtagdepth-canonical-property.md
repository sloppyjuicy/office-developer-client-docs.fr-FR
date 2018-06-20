---
title: Propriété canonique PidTagDepth
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDepth
api_type:
- HeaderDef
ms.assetid: 04d444a5-e97f-48e6-89a5-8a6cb2136408
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 25af87004ef5616a6c6fc575c647fdd1794d710f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19785923"
---
# <a name="pidtagdepth-canonical-property"></a><span data-ttu-id="a87dc-103">Propriété canonique PidTagDepth</span><span class="sxs-lookup"><span data-stu-id="a87dc-103">PidTagDepth Canonical Property</span></span>

  
  
<span data-ttu-id="a87dc-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a87dc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a87dc-105">Contient un entier qui représente le niveau de retrait, ou la profondeur, d’un objet dans une table de hiérarchie relatif.</span><span class="sxs-lookup"><span data-stu-id="a87dc-105">Contains an integer that represents the relative level of indentation, or depth, of an object in a hierarchy table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a87dc-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="a87dc-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="a87dc-107">PR_DEPTH</span><span class="sxs-lookup"><span data-stu-id="a87dc-107">PR_DEPTH</span></span>  <br/> |
|<span data-ttu-id="a87dc-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="a87dc-108">Identifier:</span></span>  <br/> |<span data-ttu-id="a87dc-109">0x3005</span><span class="sxs-lookup"><span data-stu-id="a87dc-109">0x3005</span></span>  <br/> |
|<span data-ttu-id="a87dc-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="a87dc-110">Data type:</span></span>  <br/> |<span data-ttu-id="a87dc-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a87dc-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a87dc-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="a87dc-112">Area:</span></span>  <br/> |<span data-ttu-id="a87dc-113">MAPI courantes</span><span class="sxs-lookup"><span data-stu-id="a87dc-113">MAPI common</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a87dc-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a87dc-114">Remarks</span></span>

<span data-ttu-id="a87dc-115">Cette propriété peut également spécifier le niveau de la catégorisation d’une ligne dans une table des matières ou la profondeur de hiérarchie dans une table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="a87dc-115">This property can also specify the categorization level of a row in a contents table or the hierarchy depth in a hierarchy table.</span></span> <span data-ttu-id="a87dc-116">La profondeur est zéro, où zéro représente la catégorie plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="a87dc-116">The depth is zero-based, where zero represents the leftmost category.</span></span> <span data-ttu-id="a87dc-117">Dans tous les cas, la valeur de propriété représente une valeur relative plutôt qu’une valeur absolue.</span><span class="sxs-lookup"><span data-stu-id="a87dc-117">In all cases, the property value represents a relative value rather than an absolute value.</span></span> <span data-ttu-id="a87dc-118">Dans la table de hiérarchie, par exemple, la valeur de profondeur est par rapport au conteneur à partir de laquelle la table de hiérarchie a été récupérée.</span><span class="sxs-lookup"><span data-stu-id="a87dc-118">In the hierarchy table, for example, the depth value is relative to the container from which the hierarchy table was retrieved.</span></span> <span data-ttu-id="a87dc-119">La profondeur ne représente pas une profondeur absolue du conteneur racine.</span><span class="sxs-lookup"><span data-stu-id="a87dc-119">The depth does not represent an absolute depth from the root container.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="a87dc-120">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="a87dc-120">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a87dc-121">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="a87dc-121">Protocol specifications</span></span>

<span data-ttu-id="a87dc-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a87dc-122">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a87dc-123">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="a87dc-123">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="a87dc-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a87dc-124">[[MS-OXCTABL]](http://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a87dc-125">Inclut les opérations autorisées pour les objets de la table principale.</span><span class="sxs-lookup"><span data-stu-id="a87dc-125">Includes permissible operations for the core table objects.</span></span>
    
<span data-ttu-id="a87dc-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="a87dc-126">[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="a87dc-127">Spécifie les propriétés et opérations pour les listes des utilisateurs, des contacts, des groupes et des ressources.</span><span class="sxs-lookup"><span data-stu-id="a87dc-127">Specifies the properties and operations for lists of users, contacts, groups, and resources.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a87dc-128">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="a87dc-128">Header files</span></span>

<span data-ttu-id="a87dc-129">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a87dc-129">Mapidefs.h</span></span>
  
> <span data-ttu-id="a87dc-130">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="a87dc-130">Provides data type definitions.</span></span>
    
<span data-ttu-id="a87dc-131">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="a87dc-131">Mapitags.h</span></span>
  
> <span data-ttu-id="a87dc-132">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="a87dc-132">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a87dc-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a87dc-133">See also</span></span>



[<span data-ttu-id="a87dc-134">Propriété canonique PidTagObjectType</span><span class="sxs-lookup"><span data-stu-id="a87dc-134">PidTagObjectType Canonical Property</span></span>](pidtagobjecttype-canonical-property.md)
  
[<span data-ttu-id="a87dc-135">Propriété canonique PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="a87dc-135">PidTagSelectable Canonical Property</span></span>](pidtagselectable-canonical-property.md)


[<span data-ttu-id="a87dc-136">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="a87dc-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a87dc-137">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="a87dc-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a87dc-138">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="a87dc-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a87dc-139">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="a87dc-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

