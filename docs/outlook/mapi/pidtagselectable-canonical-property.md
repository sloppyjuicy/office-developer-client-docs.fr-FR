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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 225c435107ba79183c737ddb8e09cda1ffbd83f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786742"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="6b910-103">Propriété canonique PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="6b910-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="6b910-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b910-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b910-105">Contient la valeur TRUE si l’entrée dans la table unique peut être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="6b910-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b910-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="6b910-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6b910-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="6b910-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="6b910-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="6b910-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6b910-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="6b910-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="6b910-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="6b910-110">Data type:</span></span>  <br/> |<span data-ttu-id="6b910-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="6b910-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="6b910-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="6b910-112">Area:</span></span>  <br/> |<span data-ttu-id="6b910-113">Conteneur de carnet d’adresses</span><span class="sxs-lookup"><span data-stu-id="6b910-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b910-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b910-114">Remarks</span></span>

<span data-ttu-id="6b910-115">Cette propriété est utilisée principalement pour la mise en forme visuelle d’une table unique.</span><span class="sxs-lookup"><span data-stu-id="6b910-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="6b910-116">Les modèles peuvent être regroupés en créant une entrée qui indique le titre pour le groupe.</span><span class="sxs-lookup"><span data-stu-id="6b910-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="6b910-117">Définir cette propriété sur FALSE pour l’en-tête garantit que l’utilisateur peut sélectionner uniquement les modèles réelles dans le groupe et pas cette entrée de titre.</span><span class="sxs-lookup"><span data-stu-id="6b910-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="6b910-118">Cette propriété s’applique uniquement à une table unique, pas à une table de hiérarchie de livre adresse.</span><span class="sxs-lookup"><span data-stu-id="6b910-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="6b910-119">MAPI permet à un fournisseur de carnet d’adresses pour regrouper les éléments visuellement de deux manières.</span><span class="sxs-lookup"><span data-stu-id="6b910-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="6b910-120">Tout d’abord, certaines lignes peuvent fonctionner comme en-têtes en étant non sélectionnable.</span><span class="sxs-lookup"><span data-stu-id="6b910-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="6b910-121">Deuxièmement, les éléments sélectionnables peuvent être mis en retrait par rapport à leurs en-têtes à l’aide de la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6b910-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="6b910-122">Cette propriété est utilisée dans ce regroupement pour indiquer si cet élément peut être sélectionné dans une liste pour créer une adresse unique.</span><span class="sxs-lookup"><span data-stu-id="6b910-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="6b910-123">Par exemple, si un client a plusieurs modèles pour la création des adresses de télécopie, il peut afficher les comme suit :</span><span class="sxs-lookup"><span data-stu-id="6b910-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="6b910-124">Modèles de télécopies (profondeur 0, pas sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="6b910-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="6b910-125">Local (profondeur 1, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="6b910-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="6b910-126">Appel longue distance (profondeur 1, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="6b910-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="6b910-127">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="6b910-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="6b910-128">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="6b910-128">Protocol specifications</span></span>

<span data-ttu-id="6b910-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b910-129">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b910-130">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="6b910-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="6b910-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="6b910-131">[[MS-OXOABKT]](http://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="6b910-132">Spécifie les propriétés et les opérations qui sont autorisées pour les modèles de carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="6b910-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="6b910-133">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="6b910-133">Header files</span></span>

<span data-ttu-id="6b910-134">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6b910-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="6b910-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="6b910-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="6b910-136">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="6b910-136">Mapitags.h</span></span>
  
> <span data-ttu-id="6b910-137">Contient les définitions des propriétés répertoriées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="6b910-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6b910-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b910-138">See also</span></span>



[<span data-ttu-id="6b910-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="6b910-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="6b910-140">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="6b910-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="6b910-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="6b910-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6b910-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="6b910-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6b910-143">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="6b910-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6b910-144">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="6b910-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

