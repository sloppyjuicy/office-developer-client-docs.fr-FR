---
title: IMAPIContainerGetHierarchyTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetHierarchyTable
api_type:
- COM
ms.assetid: d0c54092-86a3-47e0-8133-72e119e74b65
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 88b6f220f812f419b3f881aaa7f70a22186b589e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563799"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="3fb2b-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="3fb2b-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="3fb2b-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fb2b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fb2b-105">Retourne un pointeur vers la table de hiérarchie du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="3fb2b-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="3fb2b-106">Parameters</span></span>

 <span data-ttu-id="3fb2b-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3fb2b-107">_ulFlags_</span></span>
  
> <span data-ttu-id="3fb2b-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont les informations sont retournées dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="3fb2b-109">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="3fb2b-109">The following flags can be set:</span></span>
    
<span data-ttu-id="3fb2b-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="3fb2b-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="3fb2b-111">Remplit la table de hiérarchie avec des conteneurs de plusieurs niveaux.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="3fb2b-112">Si CONVENIENT_DEPTH n’est pas définie, la table de hiérarchie contient uniquement les conteneurs enfant immédiat du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="3fb2b-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="3fb2b-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="3fb2b-114">**GetHierarchyTable** peut renvoyer avec succès, probablement que le tableau soit disponible à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="3fb2b-115">Si le tableau n’est pas disponible, l’émission d’un appel de la table suivante peut déclencher une erreur.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="3fb2b-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="3fb2b-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="3fb2b-117">Demandes de renvoyer les colonnes qui contiennent des données de type chaîne au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="3fb2b-118">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes doivent être retournées au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="3fb2b-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="3fb2b-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="3fb2b-120">Affiche les éléments qui sont actuellement marqués comme logicielles supprimés — autrement dit, ils sont dans la rétention des éléments supprimés phase de temps.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="3fb2b-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="3fb2b-121">_lppTable_</span></span>
  
> <span data-ttu-id="3fb2b-122">[out] Pointeur vers un pointeur vers la table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3fb2b-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3fb2b-123">Return value</span></span>

<span data-ttu-id="3fb2b-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fb2b-124">S_OK</span></span> 
  
> <span data-ttu-id="3fb2b-125">La table de hiérarchie a été récupérée correctement.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="3fb2b-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="3fb2b-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="3fb2b-127">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="3fb2b-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="3fb2b-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="3fb2b-129">Le conteneur a les conteneurs enfants et ne peuvent pas fournir une table de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fb2b-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="3fb2b-130">Remarks</span></span>

<span data-ttu-id="3fb2b-131">La méthode **IMAPIContainer::GetHierarchyTable** renvoie un pointeur vers la table de hiérarchie d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="3fb2b-132">Une table de hiérarchie conserve des informations récapitulatives concernant les conteneurs enfants dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="3fb2b-133">Tables de hiérarchie de dossier contiennent des informations sur les sous-dossiers ; tables de hiérarchie adresse livre contiennent des informations sur les enfants conteneurs de carnet d’adresses et listes de distribution.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="3fb2b-134">Il est possible pour certains conteneurs pour que les conteneurs enfants.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="3fb2b-135">Ces conteneurs renvoient MAPI_E_NO_SUPPORT à partir de leurs implémentations de **GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="3fb2b-136">Lorsque l’indicateur CONVENIENT_DEPTH est défini, chaque ligne dans la table de hiérarchie inclut également la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en tant que colonne.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="3fb2b-137">**PR_DEPTH** indique le niveau de chaque conteneur par rapport à du conteneur qui implémente le tableau.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="3fb2b-138">Enfant immédiat du conteneur d’application sont des conteneurs au niveau de profondeur de zéro, les conteneurs enfants dans les conteneurs de profondeur zéro sont en profondeur un et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="3fb2b-139">Les valeurs de **PR_DEPTH** augmentent en séquence comme approfondit la hiérarchie de niveaux.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="3fb2b-140">Pour une liste complète des colonnes obligatoires et facultatifs dans les tables de hiérarchie, voir les [Tables de hiérarchie](hierarchy-tables.md).</span><span class="sxs-lookup"><span data-stu-id="3fb2b-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3fb2b-141">Remarques à l’attention des responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3fb2b-141">Notes to implementers</span></span>

<span data-ttu-id="3fb2b-142">Si vous prenez en charge une table de hiérarchie de votre conteneur, vous devez également procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="3fb2b-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="3fb2b-143">Prend en charge un appel à la méthode de [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="3fb2b-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="3fb2b-144">Retourner **PR_CONTAINER_HIERARCHY** à partir d’un appel aux méthodes de [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) du conteneur.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="3fb2b-145">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="3fb2b-145">Notes to callers</span></span>

<span data-ttu-id="3fb2b-146">Colonnes de tableau contenu chaîne et binaires peuvent être tronqués.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="3fb2b-147">En règle générale, les fournisseurs retournent 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="3fb2b-148">Car vous ne pouvez pas savoir au préalable si une table inclut des colonnes tronqués, supposons qu’une colonne est tronquée si la longueur de la colonne est 255 ou 510 octets.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="3fb2b-149">Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet à l’aide de son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .</span><span class="sxs-lookup"><span data-stu-id="3fb2b-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="3fb2b-150">Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent appliquer à la chaîne entière ou à la version tronquée de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="3fb2b-151">En outre, les fournisseurs de magasins ne sont pas nécessairement de respecter l’ensemble d’ordre de tri [que ssortorderset](ssortorderset.md) spécifiée pour les tables de hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3fb2b-152">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3fb2b-152">MFCMAPI reference</span></span>

<span data-ttu-id="3fb2b-153">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3fb2b-154">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3fb2b-154">**File**</span></span>|<span data-ttu-id="3fb2b-155">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3fb2b-155">**Function**</span></span>|<span data-ttu-id="3fb2b-156">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3fb2b-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3fb2b-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="3fb2b-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="3fb2b-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="3fb2b-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="3fb2b-159">La classe CHierarchyTableTreeCtrl utilise **GetHierarchyTable** pour obtenir des tables de hiérarchie à afficher dans un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="3fb2b-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3fb2b-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fb2b-160">See also</span></span>



[<span data-ttu-id="3fb2b-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="3fb2b-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="3fb2b-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="3fb2b-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="3fb2b-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fb2b-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="3fb2b-164">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="3fb2b-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="3fb2b-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="3fb2b-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="3fb2b-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3fb2b-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

