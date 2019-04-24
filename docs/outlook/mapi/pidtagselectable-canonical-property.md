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
ms.openlocfilehash: 17343a721cbcc642c8cffe95112f25710c0c130c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359016"
---
# <a name="pidtagselectable-canonical-property"></a><span data-ttu-id="08920-103">Propriété canonique PidTagSelectable</span><span class="sxs-lookup"><span data-stu-id="08920-103">PidTagSelectable Canonical Property</span></span>

  
  
<span data-ttu-id="08920-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="08920-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="08920-105">Contient la valeur TRUE si l'entrée dans la table ponctuelle peut être sélectionnée.</span><span class="sxs-lookup"><span data-stu-id="08920-105">Contains TRUE if the entry in the one-off table can be selected.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="08920-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="08920-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="08920-107">PR_SELECTABLE</span><span class="sxs-lookup"><span data-stu-id="08920-107">PR_SELECTABLE</span></span>  <br/> |
|<span data-ttu-id="08920-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="08920-108">Identifier:</span></span>  <br/> |<span data-ttu-id="08920-109">0x3609</span><span class="sxs-lookup"><span data-stu-id="08920-109">0x3609</span></span>  <br/> |
|<span data-ttu-id="08920-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="08920-110">Data type:</span></span>  <br/> |<span data-ttu-id="08920-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="08920-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="08920-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="08920-112">Area:</span></span>  <br/> |<span data-ttu-id="08920-113">Conteneur de carnet d'adresses</span><span class="sxs-lookup"><span data-stu-id="08920-113">Address book container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="08920-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="08920-114">Remarks</span></span>

<span data-ttu-id="08920-115">Cette propriété est principalement utilisée pour la mise en forme visuelle d'une table ponctuelle.</span><span class="sxs-lookup"><span data-stu-id="08920-115">This property is used primarily for visual formatting of a one-off table.</span></span> <span data-ttu-id="08920-116">Les modèles peuvent être regroupés en créant une entrée qui indique l'en-tête du groupe.</span><span class="sxs-lookup"><span data-stu-id="08920-116">Templates can be grouped by creating an entry that indicates the heading for the group.</span></span> <span data-ttu-id="08920-117">La définition de cette propriété sur FALSe pour l'en-tête garantit que l'utilisateur peut sélectionner uniquement les modèles réels dans le groupe et non cette entrée d'en-tête.</span><span class="sxs-lookup"><span data-stu-id="08920-117">Setting this property to FALSE for the heading ensures that the user can select only the actual templates in the group and not this heading entry.</span></span> 
  
<span data-ttu-id="08920-118">Cette propriété s'applique uniquement à une table ponctuelle, et non à une table de hiérarchie de carnets d'adresses.</span><span class="sxs-lookup"><span data-stu-id="08920-118">This property applies only to a one-off table, not to an address book hierarchy table.</span></span> 
  
<span data-ttu-id="08920-119">MAPI permet à un fournisseur de carnets d'adresses de regrouper les éléments visuellement de deux manières.</span><span class="sxs-lookup"><span data-stu-id="08920-119">MAPI allows an address book provider to group items visually by two means.</span></span> <span data-ttu-id="08920-120">Tout d'abord, certaines lignes peuvent fonctionner comme des en-têtes en étant désélectionnées.</span><span class="sxs-lookup"><span data-stu-id="08920-120">First, certain rows can function as headings by being unselectable.</span></span> <span data-ttu-id="08920-121">Deuxièmement, les éléments sélectionnables peuvent être mis en retrait par rapport à leurs en-têtes à l'aide de la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="08920-121">Second, the selectable items can be indented relative to their headings by using the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property.</span></span> <span data-ttu-id="08920-122">Cette propriété est utilisée dans ce regroupement pour indiquer si cet élément peut être sélectionné ou non dans une liste pour créer une adresse ponctuelle.</span><span class="sxs-lookup"><span data-stu-id="08920-122">This property is used in such grouping to indicate whether or not this item can be selected from a list to create a one-off address.</span></span> <span data-ttu-id="08920-123">Par exemple, si un client dispose de plusieurs modèles pour créer des adresses de télécopie, il peut les afficher comme suit:</span><span class="sxs-lookup"><span data-stu-id="08920-123">For example, if a client has several templates for building fax addresses, it can display them as follows:</span></span> 
  
<span data-ttu-id="08920-124">Modèles de télécopie (profondeur 0, non sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="08920-124">FAX templates (depth 0, not selectable)</span></span>
  
 <span data-ttu-id="08920-125">Local (profondeur 1, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="08920-125">Local (depth 1, selectable)</span></span> 
  
 <span data-ttu-id="08920-126">Longue distance (profondeur 1, sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="08920-126">Long-distance (depth 1, selectable)</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="08920-127">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="08920-127">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="08920-128">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="08920-128">Protocol specifications</span></span>

<span data-ttu-id="08920-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08920-129">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08920-130">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="08920-130">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="08920-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="08920-131">[[MS-OXOABKT]](https://msdn.microsoft.com/library/cd5a3e78-1eeb-4a75-88eb-e82c8c96ff31%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="08920-132">Spécifie les propriétés et les opérations autorisées pour les modèles de carnet d'adresses.</span><span class="sxs-lookup"><span data-stu-id="08920-132">Specifies the properties and operations that are permissible for address book templates.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="08920-133">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="08920-133">Header files</span></span>

<span data-ttu-id="08920-134">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="08920-134">Mapidefs.h</span></span>
  
> <span data-ttu-id="08920-135">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="08920-135">Provides data type definitions.</span></span>
    
<span data-ttu-id="08920-136">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="08920-136">Mapitags.h</span></span>
  
> <span data-ttu-id="08920-137">Contient les définitions des propriétés indiquées en tant que propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="08920-137">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="08920-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08920-138">See also</span></span>



[<span data-ttu-id="08920-139">IABLogon::GetOneOffTable</span><span class="sxs-lookup"><span data-stu-id="08920-139">IABLogon::GetOneOffTable</span></span>](iablogon-getoneofftable.md)
  
[<span data-ttu-id="08920-140">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="08920-140">PidTagFolderType Canonical Property</span></span>](pidtagfoldertype-canonical-property.md)


[<span data-ttu-id="08920-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="08920-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="08920-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="08920-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="08920-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="08920-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="08920-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="08920-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

