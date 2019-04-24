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
ms.openlocfilehash: 7cca884eae2111a94d87cc24a6d30542148ab845
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316316"
---
# <a name="pidtagfoldertype-canonical-property"></a><span data-ttu-id="9d1ce-103">Propriété canonique PidTagFolderType</span><span class="sxs-lookup"><span data-stu-id="9d1ce-103">PidTagFolderType Canonical Property</span></span>

  
  
<span data-ttu-id="9d1ce-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d1ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d1ce-105">Contient une constante qui indique le type de dossier.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-105">Contains a constant that indicates the folder type.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9d1ce-106">Propriétés associées :</span><span class="sxs-lookup"><span data-stu-id="9d1ce-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="9d1ce-107">PR_FOLDER_TYPE</span><span class="sxs-lookup"><span data-stu-id="9d1ce-107">PR_FOLDER_TYPE</span></span>  <br/> |
|<span data-ttu-id="9d1ce-108">Identificateur :</span><span class="sxs-lookup"><span data-stu-id="9d1ce-108">Identifier:</span></span>  <br/> |<span data-ttu-id="9d1ce-109">0x3601</span><span class="sxs-lookup"><span data-stu-id="9d1ce-109">0x3601</span></span>  <br/> |
|<span data-ttu-id="9d1ce-110">Type de données :</span><span class="sxs-lookup"><span data-stu-id="9d1ce-110">Data type:</span></span>  <br/> |<span data-ttu-id="9d1ce-111">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="9d1ce-111">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="9d1ce-112">Domaine :</span><span class="sxs-lookup"><span data-stu-id="9d1ce-112">Area:</span></span>  <br/> |<span data-ttu-id="9d1ce-113">Conteneur MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1ce-113">MAPI container</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d1ce-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="9d1ce-114">Remarks</span></span>

<span data-ttu-id="9d1ce-115">Cette propriété peut avoir exactement l'une des valeurs suivantes:</span><span class="sxs-lookup"><span data-stu-id="9d1ce-115">This property can have exactly one of the following values:</span></span>
  
<span data-ttu-id="9d1ce-116">FOLDER_GENERIC</span><span class="sxs-lookup"><span data-stu-id="9d1ce-116">FOLDER_GENERIC</span></span> 
  
> <span data-ttu-id="9d1ce-117">Dossier générique contenant des messages et d'autres dossiers.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-117">A generic folder that contains messages and other folders.</span></span>
    
<span data-ttu-id="9d1ce-118">FOLDER_ROOT</span><span class="sxs-lookup"><span data-stu-id="9d1ce-118">FOLDER_ROOT</span></span> 
  
> <span data-ttu-id="9d1ce-119">Dossier racine de la table de hiérarchie des dossiers, c'est-à-dire un dossier qui n'a pas de dossier parent.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-119">The root folder of the folder hierarchy table, that is, a folder that has no parent folder.</span></span>
    
<span data-ttu-id="9d1ce-120">FOLDER_SEARCH</span><span class="sxs-lookup"><span data-stu-id="9d1ce-120">FOLDER_SEARCH</span></span> 
  
> <span data-ttu-id="9d1ce-121">Dossier contenant les résultats d'une recherche, sous la forme de liens vers des messages qui répondent aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-121">A folder that contains the results of a search, in the form of links to messages that meet search criteria.</span></span>
    
<span data-ttu-id="9d1ce-122">La racine d'un magasin de messages ne doit pas être confondue avec la racine de la sous-arborescence message interpersonne (IPM) dans cette banque.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-122">The root of a message store should not be confused with the root of the interpersonal message (IPM) subtree in that store.</span></span> <span data-ttu-id="9d1ce-123">Le dossier racine de la Banque, qui n'a pas de parent, est obtenu en appelant la méthode [IMsgStore:: OpenEntry](imsgstore-openentry.md) avec un identificateur d'entrée null.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-123">The store's root folder, which has no parent, is obtained by calling the [IMsgStore::OpenEntry](imsgstore-openentry.md) method with a null entry identifier.</span></span> <span data-ttu-id="9d1ce-124">Le dossier racine de la sous-arborescence IPM, qui a un parent, est obtenu à l'aide de la valeur de la propriété **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) pour l'appel **OpenEntry** .</span><span class="sxs-lookup"><span data-stu-id="9d1ce-124">The IPM subtree's root folder, which does have a parent, is obtained by using the value of the **PR_IPM_SUBTREE_ENTRYID** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md)) property for the **OpenEntry** call.</span></span> 
  
<span data-ttu-id="9d1ce-125">MAPI n'autorise qu'un seul dossier racine par Banque de messages.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-125">MAPI allows only one root folder per message store.</span></span> <span data-ttu-id="9d1ce-126">Ce dossier contient des messages et d'autres dossiers.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-126">This folder contains messages and other folders.</span></span> <span data-ttu-id="9d1ce-127">La propriété **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) du dossier racine contient l'identificateur d'entrée propre au dossier.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-127">The root folder's **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) property contains the folder's own entry identifier.</span></span>
  
<span data-ttu-id="9d1ce-128">Les informations contenues dans un dossier de résultats de recherche sont principalement stockées dans sa table des matières, qui contient les mêmes colonnes qu'une table de contenu classique, ainsi que deux colonnes supplémentaires identifiant le dossier dans lequel chaque message a été trouvé: **PR_PARENT_DISPLAY** ([ PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (nom complet, obligatoire) et cette propriété (identificateur d'entrée, facultatif).</span><span class="sxs-lookup"><span data-stu-id="9d1ce-128">The information in a search-results folder is mainly stored in its contents table, which contains the same columns as a typical contents table, as well as two extra columns identifying the folder in which each message was found: **PR_PARENT_DISPLAY** ([PidTagParentDisplay](pidtagparentdisplay-canonical-property.md)) (display name, required) and this property (entry identifier, optional).</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="9d1ce-129">Ressources associées</span><span class="sxs-lookup"><span data-stu-id="9d1ce-129">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="9d1ce-130">Spécifications de protocole</span><span class="sxs-lookup"><span data-stu-id="9d1ce-130">Protocol specifications</span></span>

<span data-ttu-id="9d1ce-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1ce-131">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1ce-132">Fournit des références à des spécifications de protocole Exchange Server connexes.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-132">Provides references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="9d1ce-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="9d1ce-133">[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="9d1ce-134">Gère les opérations de dossier.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-134">Handles folder operations.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="9d1ce-135">Fichiers d'en-tête</span><span class="sxs-lookup"><span data-stu-id="9d1ce-135">Header files</span></span>

<span data-ttu-id="9d1ce-136">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="9d1ce-136">Mapidefs.h</span></span>
  
> <span data-ttu-id="9d1ce-137">Fournit des définitions de type de données.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-137">Provides data type definitions.</span></span>
    
<span data-ttu-id="9d1ce-138">Mapitags. h</span><span class="sxs-lookup"><span data-stu-id="9d1ce-138">Mapitags.h</span></span>
  
> <span data-ttu-id="9d1ce-139">Contient les définitions des propriétés figurant en tant que noms de substitution.</span><span class="sxs-lookup"><span data-stu-id="9d1ce-139">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d1ce-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d1ce-140">See also</span></span>



[<span data-ttu-id="9d1ce-141">Propriétés MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1ce-141">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="9d1ce-142">Propriétés canoniques MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1ce-142">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="9d1ce-143">Mappage des noms de propriétés canoniques aux noms MAPI</span><span class="sxs-lookup"><span data-stu-id="9d1ce-143">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="9d1ce-144">Mappage des noms MAPI aux noms de propriétés canoniques</span><span class="sxs-lookup"><span data-stu-id="9d1ce-144">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

