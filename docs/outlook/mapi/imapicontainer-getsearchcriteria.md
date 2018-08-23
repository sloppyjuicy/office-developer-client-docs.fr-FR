---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: Dernière modification le 09 mars 2015
ms.openlocfilehash: 4ca565f97851a2efe2f3279f062f6ea89a4c6326
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579962"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="af140-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="af140-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="af140-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af140-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af140-105">Obtient les critères de recherche pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="af140-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="af140-106">Param�tres</span><span class="sxs-lookup"><span data-stu-id="af140-106">Parameters</span></span>

 <span data-ttu-id="af140-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="af140-107">_ulFlags_</span></span>
  
> <span data-ttu-id="af140-108">[in] Masque de bits d’indicateurs qui contrôle le type des chaînes dans le passé.</span><span class="sxs-lookup"><span data-stu-id="af140-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="af140-109">Vous pouvez définir l’indicateur suivant :</span><span class="sxs-lookup"><span data-stu-id="af140-109">The following flag can be set:</span></span>
    
<span data-ttu-id="af140-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="af140-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="af140-111">Les chaînes passée sont au format Unicode.</span><span class="sxs-lookup"><span data-stu-id="af140-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="af140-112">Si l’indicateur MAPI_UNICODE n’est pas définie, les chaînes sont au format ANSI.</span><span class="sxs-lookup"><span data-stu-id="af140-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="af140-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="af140-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="af140-114">[out] Pointeur vers un pointeur vers une structure [SRestriction](srestriction.md) qui définit les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="af140-115">Si une application cliente passe NULL dans le paramètre _lppRestriction_ , **GetSearchCriteria** ne renvoie pas une structure **SRestriction** .</span><span class="sxs-lookup"><span data-stu-id="af140-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="af140-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="af140-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="af140-117">[out] Pointeur vers un pointeur vers un tableau d’identificateurs d’entrée qui représentent les conteneurs à inclure dans la recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="af140-118">Si un client passe NULL dans le paramètre _lppContainerList_ , **GetSearchCriteria** ne renvoie pas un tableau d’identificateurs d’entrée.</span><span class="sxs-lookup"><span data-stu-id="af140-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="af140-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="af140-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="af140-120">[out] Pointeur vers un masque binaire composé des indicateurs utilisés pour indiquer l’état actuel de la recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="af140-121">Si un client passe NULL dans le paramètre _lpulSearchState_ , **GetSearchCriteria** ne renvoie aucun indicateur.</span><span class="sxs-lookup"><span data-stu-id="af140-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="af140-122">Les indicateurs suivants peuvent être définis :</span><span class="sxs-lookup"><span data-stu-id="af140-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="af140-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="af140-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="af140-124">La recherche doit être exécutée à priorité élevée par rapport à d’autres critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="af140-125">Si cet indicateur n’est pas défini, la recherche s’exécute à une priorité normale par rapport à d’autres critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="af140-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="af140-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="af140-127">La recherche est en mode intensive du processeur de son fonctionnement, essayez de rechercher des messages qui correspondent aux critères.</span><span class="sxs-lookup"><span data-stu-id="af140-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="af140-128">Si cet indicateur n’est pas défini, le composant intensive du processeur de l’opération de la recherche est.</span><span class="sxs-lookup"><span data-stu-id="af140-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="af140-129">Cet indicateur n’a une signification uniquement si la recherche est active (c'est-à-dire, si l’indicateur SEARCH_RUNNING est défini).</span><span class="sxs-lookup"><span data-stu-id="af140-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="af140-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="af140-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="af140-131">Recherche dans les conteneurs spécifiés et tous les conteneurs de leurs enfants pour la correspondance des entrées de la recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="af140-132">Si cet indicateur n’est pas défini, que les conteneurs explicitement incluses dans le dernier appel à la méthode [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) sont recherchés.</span><span class="sxs-lookup"><span data-stu-id="af140-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="af140-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="af140-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="af140-134">La recherche est active et la table des matières du conteneur est mis à jour pour refléter les modifications de la banque de messages ou le carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="af140-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="af140-135">Si cet indicateur n’est pas défini, la recherche est inactive et la table des matières est statique.</span><span class="sxs-lookup"><span data-stu-id="af140-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af140-136">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="af140-136">Return value</span></span>

<span data-ttu-id="af140-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="af140-137">S_OK</span></span> 
  
> <span data-ttu-id="af140-138">Les critères de recherche a été obtenue avec succès.</span><span class="sxs-lookup"><span data-stu-id="af140-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="af140-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="af140-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="af140-140">Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été défini et l’implémentation prend en charge Unicode uniquement.</span><span class="sxs-lookup"><span data-stu-id="af140-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="af140-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="af140-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="af140-142">Critères de recherche ont été établies jamais pour le conteneur.</span><span class="sxs-lookup"><span data-stu-id="af140-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="af140-143">Remarques</span><span class="sxs-lookup"><span data-stu-id="af140-143">Remarks</span></span>

<span data-ttu-id="af140-144">La méthode **IMAPIContainer::GetSearchCriteria** Obtient les critères de recherche pour un conteneur qui prend en charge les recherches, généralement un dossier de résultats de recherche.</span><span class="sxs-lookup"><span data-stu-id="af140-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="af140-145">Vous créez des critères de recherche en appelant la méthode de **IMAPIContainer::SetSearchCriteria** d’un conteneur.</span><span class="sxs-lookup"><span data-stu-id="af140-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="af140-146">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="af140-146">Notes to implementers</span></span>

<span data-ttu-id="af140-147">Conteneurs de carnet d’adresses peuvent prendre en charge **GetSearchCriteria** uniquement s’ils fournissent les fonctionnalités de recherche avancée associées à la propriété **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="af140-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="af140-148">Pour plus d’informations sur la façon d’implémenter la fonctionnalité de recherche avancée pour les conteneurs de carnet d’adresses, voir [Implémentation de la recherche avancée](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="af140-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="af140-149">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="af140-149">Notes to callers</span></span>

<span data-ttu-id="af140-150">Lorsque vous avez terminé avec les structures de données indiqués par les paramètres _lppRestriction_ et _lppContainerList_ , appelez [MAPIFreeBuffer](mapifreebuffer.md) qu’une seule fois pour chaque structure doit être publié.</span><span class="sxs-lookup"><span data-stu-id="af140-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="af140-151">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="af140-151">MFCMAPI reference</span></span>

<span data-ttu-id="af140-152">Pour des exemples de code MFCMAPI, voir le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="af140-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="af140-153">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="af140-153">**File**</span></span>|<span data-ttu-id="af140-154">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="af140-154">**Function**</span></span>|<span data-ttu-id="af140-155">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="af140-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="af140-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="af140-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="af140-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="af140-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="af140-158">MFCMAPI utilise la méthode **IMAPIContainer::GetSearchCriteria** pour obtenir des critères de recherche à partir d’un dossier à afficher.</span><span class="sxs-lookup"><span data-stu-id="af140-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="af140-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="af140-159">See also</span></span>



[<span data-ttu-id="af140-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="af140-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="af140-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="af140-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="af140-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="af140-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="af140-163">Propriété canonique PidTagSearch</span><span class="sxs-lookup"><span data-stu-id="af140-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="af140-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="af140-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="af140-165">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="af140-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

