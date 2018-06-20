---
title: Propriété canonique PidTagFolderType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderType
api_type:
- HeaderDef
ms.assetid: 2ab4681e-0013-4ba0-ba26-50517bbf3f5b
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 2520a7544eb4ba39cd83a7a0aa65b98bd8a67deb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19786004"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="e45a3-103">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="e45a3-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="e45a3-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e45a3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e45a3-105">Contient une constante qui indique le type de dossier.</span><span class="sxs-lookup"><span data-stu-id="e45a3-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e45a3-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="e45a3-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e45a3-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="e45a3-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="e45a3-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="e45a3-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e45a3-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="e45a3-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="e45a3-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="e45a3-110">Data type:</span></span>  <br/> |<span data-ttu-id="e45a3-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="e45a3-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="e45a3-112">Zone :</span><span class="sxs-lookup"><span data-stu-id="e45a3-112">Area:</span></span>  <br/> |<span data-ttu-id="e45a3-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="e45a3-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e45a3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="e45a3-114">Remarks</span></span>

<span data-ttu-id="e45a3-115">Cette propriété peut avoir exactement une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="e45a3-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="e45a3-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="e45a3-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="e45a3-117">Un dossier générique qui contient des messages et autres dossiers.</span><span class="sxs-lookup"><span data-stu-id="e45a3-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="e45a3-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="e45a3-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="e45a3-119">Le dossier racine de la table de hiérarchie de dossier, autrement dit, un dossier qui n’a aucun dossier parent.</span><span class="sxs-lookup"><span data-stu-id="e45a3-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="e45a3-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="e45a3-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="e45a3-121">Un dossier qui contient les résultats d’une recherche, sous la forme de liens vers les messages qui répondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="e45a3-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="e45a3-122">La racine d’une banque de messages ne doit pas être confondue avec la racine de la sous-arborescence message interpersonnel (IPM) de cette banque.</span><span class="sxs-lookup"><span data-stu-id="e45a3-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="e45a3-123">Dossier racine de la banque, qui n’a pas de parent, est obtenu en appelant la méthode [IMsgStore::OpenEntry](imsgstore-openentry.md) avec un identificateur d’entrée null.</span><span class="sxs-lookup"><span data-stu-id="e45a3-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="e45a3-124">Dossier racine de la sous-arborescence IPM, qui a un parent, est obtenue à l’aide de la valeur de la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) pour l’appel de **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="e45a3-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="e45a3-125">MAPI ne permet qu’un seul dossier racine par banque de messages.</span><span class="sxs-lookup"><span data-stu-id="e45a3-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="e45a3-126">Ce dossier contient des messages et autres dossiers.</span><span class="sxs-lookup"><span data-stu-id="e45a3-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="e45a3-127">Propriété de **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) du dossier racine contient l’identificateur d’entrée du dossier.</span><span class="sxs-lookup"><span data-stu-id="e45a3-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="e45a3-128">Les informations contenues dans un dossier de résultats de recherche sont principalement stockés dans sa table des matières, qui contient les mêmes colonnes sous forme de tableau de type de contenu, ainsi que deux colonnes supplémentaires qui identifie le dossier dans lequel chaque message a été trouvé : **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (affiche le nom, requis) et que cette propriété (identificateur d’entrée, facultatif).</span><span class="sxs-lookup"><span data-stu-id="e45a3-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="e45a3-129">Ressources connexes</span><span class="sxs-lookup"><span data-stu-id="e45a3-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="e45a3-130">Spécifications du protocole</span><span class="sxs-lookup"><span data-stu-id="e45a3-130">Protocol specifications</span></span>

<span data-ttu-id="e45a3-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e45a3-131">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e45a3-132">Fournit des références aux spécifications du protocole Exchange Server associées.</span><span class="sxs-lookup"><span data-stu-id="e45a3-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="e45a3-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="e45a3-133">[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="e45a3-134">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="e45a3-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="e45a3-135">Fichiers d’en-tête</span><span class="sxs-lookup"><span data-stu-id="e45a3-135">Header files</span></span>

<span data-ttu-id="e45a3-136">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e45a3-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="e45a3-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="e45a3-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="e45a3-138">MAPITAGS.h</span><span class="sxs-lookup"><span data-stu-id="e45a3-138">Mapitags.h</span></span>
  
> <span data-ttu-id="e45a3-139">Contient les définitions des propriétés répertoriées en tant que d’autres noms.</span><span class="sxs-lookup"><span data-stu-id="e45a3-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e45a3-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e45a3-140">See also</span></span>



[<span data-ttu-id="e45a3-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="e45a3-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e45a3-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="e45a3-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e45a3-143">Mappage de noms de propriété canonique aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="e45a3-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e45a3-144">Mappage de noms MAPI pour les noms de propriété canonique</span><span class="sxs-lookup"><span data-stu-id="e45a3-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

