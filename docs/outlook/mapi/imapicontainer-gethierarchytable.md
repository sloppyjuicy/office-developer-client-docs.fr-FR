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
ms.openlocfilehash: efc7f7a2fa703004afe361d766e0209ba40ffe46
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426197"
---
# <a name="imapicontainergethierarchytable"></a><span data-ttu-id="5bfe7-103">IMAPIContainer::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="5bfe7-103">IMAPIContainer::GetHierarchyTable</span></span>

  
  
<span data-ttu-id="5bfe7-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bfe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bfe7-105">Renvoie un pointeur vers le tableau hiérarchique du conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-105">Returns a pointer to the container's hierarchy table.</span></span>
  
```cpp
HRESULT GetHierarchyTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="5bfe7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5bfe7-106">Parameters</span></span>

 <span data-ttu-id="5bfe7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5bfe7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5bfe7-108">[in] Masque de bits d’indicateurs qui contrôle la façon dont les informations sont renvoyées dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-108">[in] A bitmask of flags that controls how information is returned in the table.</span></span> <span data-ttu-id="5bfe7-109">Les indicateurs suivants peuvent être définies :</span><span class="sxs-lookup"><span data-stu-id="5bfe7-109">The following flags can be set:</span></span>
    
<span data-ttu-id="5bfe7-110">CONVENIENT_DEPTH</span><span class="sxs-lookup"><span data-stu-id="5bfe7-110">CONVENIENT_DEPTH</span></span> 
  
> <span data-ttu-id="5bfe7-111">Remplit la table de hiérarchie avec des conteneurs de plusieurs niveaux.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-111">Fills the hierarchy table with containers from multiple levels.</span></span> <span data-ttu-id="5bfe7-112">Si CONVENIENT_DEPTH n’est pas définie, la table de hiérarchie contient uniquement les conteneurs enfants immédiats du conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-112">If CONVENIENT_DEPTH is not set, the hierarchy table contains only the container's immediate child containers.</span></span>
    
<span data-ttu-id="5bfe7-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="5bfe7-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="5bfe7-114">**GetHierarchyTable** peut renvoyer correctement, éventuellement avant que la table soit disponible pour l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-114">**GetHierarchyTable** can return successfully, possibly before the table is made available to the caller.</span></span> <span data-ttu-id="5bfe7-115">Si la table n’est pas disponible, effectuer un appel de table ultérieur peut occasioner une erreur.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-115">If the table is not available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="5bfe7-116">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5bfe7-116">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5bfe7-117">Demande que les colonnes qui contiennent des données de chaîne soient renvoyées au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-117">Requests that the columns that contain string data be returned in Unicode format.</span></span> <span data-ttu-id="5bfe7-118">Si l MAPI_UNICODE n’est pas définie, les chaînes doivent être renvoyées au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-118">If the MAPI_UNICODE flag is not set, the strings should be returned in ANSI format.</span></span> 
    
<span data-ttu-id="5bfe7-119">SHOW_SOFT_DELETES</span><span class="sxs-lookup"><span data-stu-id="5bfe7-119">SHOW_SOFT_DELETES</span></span>
  
> <span data-ttu-id="5bfe7-120">Affiche les éléments actuellement marqués comme supprimés (supprimés (supprimés( en d’autres cas), ils sont dans la phase de rétention des éléments supprimés.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-120">Shows items that are currently marked as soft deleted—that is, they are in the deleted item retention time phase.</span></span>
    
 <span data-ttu-id="5bfe7-121">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="5bfe7-121">_lppTable_</span></span>
  
> <span data-ttu-id="5bfe7-122">[out] Pointeur vers un pointeur vers le tableau hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-122">[out] A pointer to a pointer to the hierarchy table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bfe7-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5bfe7-123">Return value</span></span>

<span data-ttu-id="5bfe7-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bfe7-124">S_OK</span></span> 
  
> <span data-ttu-id="5bfe7-125">La table de hiérarchie a été récupérée avec succès.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-125">The hierarchy table was successfully retrieved.</span></span>
    
<span data-ttu-id="5bfe7-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="5bfe7-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="5bfe7-127">L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="5bfe7-128">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="5bfe7-128">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="5bfe7-129">Le conteneur n’a pas de conteneurs enfants et ne peut pas fournir de table hiérarchique.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-129">The container has no child containers and cannot provide a hierarchy table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bfe7-130">Remarques</span><span class="sxs-lookup"><span data-stu-id="5bfe7-130">Remarks</span></span>

<span data-ttu-id="5bfe7-131">La **méthode IMAPIContainer::GetHierarchyTable** renvoie un pointeur vers la table hiérarchique d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-131">The **IMAPIContainer::GetHierarchyTable** method returns a pointer to the hierarchy table of a container.</span></span> <span data-ttu-id="5bfe7-132">Une table de hiérarchie contient des informations récapitulatifs sur les conteneurs enfants dans le conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-132">A hierarchy table holds summary information about the child containers in the container.</span></span> <span data-ttu-id="5bfe7-133">Les tables de hiérarchie de dossiers contient des informations sur les sous-dossiers . Les tables de hiérarchie de carnet d’adresses contenint des informations sur les conteneurs de carnet d’adresses et les listes de distribution enfants.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-133">Folder hierarchy tables hold information about subfolders; address book hierarchy tables hold information about child address book containers and distribution lists.</span></span> 
  
<span data-ttu-id="5bfe7-134">Certains conteneurs peuvent ne pas avoir de conteneurs enfants.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-134">It is possible for some containers to have no child containers.</span></span> <span data-ttu-id="5bfe7-135">Ces conteneurs retournent MAPI_E_NO_SUPPORT à partir de leurs implémentations **de GetHierarchyTable**.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-135">These containers return MAPI_E_NO_SUPPORT from their implementations of **GetHierarchyTable**.</span></span>
  
<span data-ttu-id="5bfe7-136">Lorsque l CONVENIENT_DEPTH est définie, chaque ligne de la table hiérarchique inclut également la propriété **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) en tant que colonne.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-136">When the CONVENIENT_DEPTH flag is set, each row in the hierarchy table also includes the **PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) property as a column.</span></span> <span data-ttu-id="5bfe7-137">**PR_DEPTH** indique le niveau de chaque conteneur par rapport au conteneur qui implémente la table.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-137">**PR_DEPTH** indicates the level of each container relative to the container that implements the table.</span></span> <span data-ttu-id="5bfe7-138">Les conteneurs enfants immédiats du conteneur d’implémentation sont à la profondeur zéro, les conteneurs enfants dans les conteneurs de profondeur zéro sont à la profondeur 1, etc.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-138">The implementing container's immediate child containers are at depth zero, child containers in the zero depth containers are at depth one, and so on.</span></span> <span data-ttu-id="5bfe7-139">Les valeurs des **PR_DEPTH** augmentent de manière séquentielle à mesure que la hiérarchie des niveaux s’accroît.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-139">The values of **PR_DEPTH** increase sequentially as the hierarchy of levels deepens.</span></span> 
  
<span data-ttu-id="5bfe7-140">Pour obtenir la liste complète des colonnes obligatoires et facultatives dans les tableaux hiérarchiques, voir [Tables de hiérarchie.](hierarchy-tables.md)</span><span class="sxs-lookup"><span data-stu-id="5bfe7-140">For a complete list of required and optional columns in hierarchy tables, see [Hierarchy Tables](hierarchy-tables.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5bfe7-141">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="5bfe7-141">Notes to implementers</span></span>

<span data-ttu-id="5bfe7-142">Si vous prendre en charge une table hiérarchique pour votre conteneur, vous devez également :</span><span class="sxs-lookup"><span data-stu-id="5bfe7-142">If you support a hierarchy table for your container, you must also do the following:</span></span>
  
- <span data-ttu-id="5bfe7-143">Prendre en charge un appel à la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) du conteneur pour ouvrir la propriété **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="5bfe7-143">Support a call to the container's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to open the **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) property.</span></span>
    
- <span data-ttu-id="5bfe7-144">Renvoyer **PR_CONTAINER_HIERARCHY** d’un appel aux méthodes [IMAPIProp::GetPropList](imapiprop-getproplist.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md) du conteneur.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-144">Return **PR_CONTAINER_HIERARCHY** from a call to the container's [IMAPIProp::GetPropList](imapiprop-getproplist.md) or [IMAPIProp::GetProps](imapiprop-getprops.md) methods.</span></span> 
    
## <a name="notes-to-callers"></a><span data-ttu-id="5bfe7-145">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="5bfe7-145">Notes to callers</span></span>

<span data-ttu-id="5bfe7-146">Les colonnes de table de contenu binaire et de chaîne peuvent être tronquées.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-146">String and binary contents table columns can be truncated.</span></span> <span data-ttu-id="5bfe7-147">En règle générale, les fournisseurs retournent 255 caractères.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-147">Typically, providers return 255 characters.</span></span> <span data-ttu-id="5bfe7-148">Comme vous ne pouvez pas savoir au préalable si un tableau inclut des colonnes tronquées, supposons qu’une colonne est tronquée si la longueur de la colonne est de 255 ou 510 octets.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-148">Because you cannot know beforehand whether a table includes truncated columns, assume that a column is truncated if the length of the column is either 255 or 510 bytes.</span></span> <span data-ttu-id="5bfe7-149">Vous pouvez toujours récupérer la valeur complète d’une colonne tronquée, si nécessaire, directement à partir de l’objet en utilisant son identificateur d’entrée pour l’ouvrir, puis en appelant la méthode [IMAPIProp::GetProps.](imapiprop-getprops.md)</span><span class="sxs-lookup"><span data-stu-id="5bfe7-149">You can always retrieve the full value of a truncated column, if necessary, directly from the object by using its entry identifier to open it and then calling the [IMAPIProp::GetProps](imapiprop-getprops.md) method.</span></span> 
  
<span data-ttu-id="5bfe7-150">Selon l’implémentation du fournisseur, les restrictions et les opérations de tri peuvent s’appliquer à la chaîne entière ou à la version tronquée de cette chaîne.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-150">Depending on the provider's implementation, restrictions and sorting operations can apply to the whole string or to the truncated version of that string.</span></span> <span data-ttu-id="5bfe7-151">En outre, il n’est pas garanti que les fournisseurs de magasins respectent le jeu d’ordre de tri [SSortOrderSet](ssortorderset.md) spécifié pour les tables hiérarchiques.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-151">Moreover, store providers are not guaranteed to honor the sort order set [SSortOrderSet](ssortorderset.md) specified for hierarchy tables.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5bfe7-152">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5bfe7-152">MFCMAPI reference</span></span>

<span data-ttu-id="5bfe7-153">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-153">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5bfe7-154">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="5bfe7-154">**File**</span></span>|<span data-ttu-id="5bfe7-155">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="5bfe7-155">**Function**</span></span>|<span data-ttu-id="5bfe7-156">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="5bfe7-156">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5bfe7-157">HierarchyTableTreeCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="5bfe7-157">HierarchyTableTreeCtrl.cpp</span></span>  <br/> |<span data-ttu-id="5bfe7-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span><span class="sxs-lookup"><span data-stu-id="5bfe7-158">CHierarchyTableTreeCtrl::GetHierarchyTable</span></span>  <br/> |<span data-ttu-id="5bfe7-159">La classe CHierarchyTableTreeCtrl utilise **GetHierarchyTable** pour obtenir des tables hiérarchiques à afficher dans un contrôle d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="5bfe7-159">The CHierarchyTableTreeCtrl class uses **GetHierarchyTable** to obtain hierarchy tables to display in a tree view control.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bfe7-160">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5bfe7-160">See also</span></span>



[<span data-ttu-id="5bfe7-161">IMAPIProp::GetPropList</span><span class="sxs-lookup"><span data-stu-id="5bfe7-161">IMAPIProp::GetPropList</span></span>](imapiprop-getproplist.md)
  
[<span data-ttu-id="5bfe7-162">IMAPIProp::GetProps</span><span class="sxs-lookup"><span data-stu-id="5bfe7-162">IMAPIProp::GetProps</span></span>](imapiprop-getprops.md)
  
[<span data-ttu-id="5bfe7-163">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bfe7-163">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="5bfe7-164">Propriété canonique PidTagContainerHierarchy</span><span class="sxs-lookup"><span data-stu-id="5bfe7-164">PidTagContainerHierarchy Canonical Property</span></span>](pidtagcontainerhierarchy-canonical-property.md)
  
[<span data-ttu-id="5bfe7-165">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="5bfe7-165">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="5bfe7-166">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="5bfe7-166">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

