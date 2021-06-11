---
title: Propriété canonique PidTagSelectable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSelectable
api_type:
- COM
ms.assetid: eeecd957-dd50-4849-9698-8bc7106301e9
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359016"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="da184-103">Propriété canonique PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="da184-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="da184-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="da184-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="da184-105">Contient TRUE si l’entrée de la table un-off peut être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="da184-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da184-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="da184-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="da184-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="da184-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="da184-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="da184-108">Identifier:</span></span>  <br/> |<span data-ttu-id="da184-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="da184-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="da184-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="da184-110">Data type:</span></span>  <br/> |<span data-ttu-id="da184-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="da184-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="da184-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="da184-112">Area:</span></span>  <br/> |<span data-ttu-id="da184-113">Conteneur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="da184-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="da184-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="da184-114">Remarks</span></span>

<span data-ttu-id="da184-115">Cette propriété est principalement utilisée pour la mise en forme visuelle d’un tableau one-off.</span><span class="sxs-lookup"><span data-stu-id="da184-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="da184-116">Les modèles peuvent être regroupés en créant une entrée qui indique le titre du groupe.</span><span class="sxs-lookup"><span data-stu-id="da184-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="da184-117">La définition de cette propriété sur FALSE pour le titre garantit que l’utilisateur peut sélectionner uniquement les modèles réels du groupe et non cette entrée de titre.</span><span class="sxs-lookup"><span data-stu-id="da184-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="da184-118">Cette propriété s’applique uniquement à une table unique, et non à une table de hiérarchie de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="da184-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="da184-119">MAPI permet à un fournisseur de carnet d’adresses de grouper visuellement les éléments par deux moyens.</span><span class="sxs-lookup"><span data-stu-id="da184-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="da184-120">Tout d’abord, certaines lignes peuvent fonctionner en tant qu’en-tête en étant désélectionnables.</span><span class="sxs-lookup"><span data-stu-id="da184-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="da184-121">Ensuite, les éléments sélectionnables peuvent être en retrait par rapport à leurs titres à l’aide de la **propriété PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="da184-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="da184-122">Cette propriété est utilisée dans ce regroupement pour indiquer si cet élément peut être sélectionné dans une liste pour créer une adresse unique.</span><span class="sxs-lookup"><span data-stu-id="da184-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="da184-123">Par exemple, si un client possède plusieurs modèles pour la création d’adresses de télécopie, il peut les afficher comme suit :</span><span class="sxs-lookup"><span data-stu-id="da184-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="da184-124">Modèles FAX (profondeur 0, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="da184-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="da184-125">Local (profondeur 1, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="da184-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="da184-126">Longue distance (profondeur 1, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="da184-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="da184-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="da184-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="da184-128">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="da184-128">Protocol specifications</span></span>

<span data-ttu-id="da184-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da184-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da184-130">Fournit des références aux spécifications Exchange Server protocole.</span><span class="sxs-lookup"><span data-stu-id="da184-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="da184-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="da184-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="da184-132">Spécifie les propriétés et opérations autorisées pour les modèles de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="da184-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="da184-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="da184-133">Header files</span></span>

<span data-ttu-id="da184-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="da184-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="da184-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="da184-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="da184-136">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="da184-136">Mapitags.h</span></span>
  
> <span data-ttu-id="da184-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="da184-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="da184-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="da184-138">See also</span></span>



[<span data-ttu-id="da184-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="da184-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="da184-140">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="da184-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="da184-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="da184-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="da184-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="da184-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="da184-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="da184-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="da184-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="da184-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

