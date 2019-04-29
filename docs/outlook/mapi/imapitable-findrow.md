---
title: IMAPITableFindRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.FindRow
api_type:
- COM
ms.assetid: 6511368c-9777-497e-9eea-cf390c04b92e
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a5364af229721d101f38d2f054f528169b48c09e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429571"
---
# <a name="imapitablefindrow"></a><span data-ttu-id="dd6de-103">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="dd6de-103">IMAPITable::FindRow</span></span>

  
  
<span data-ttu-id="dd6de-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="dd6de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="dd6de-105">Recherche la ligne suivante d'une table qui correspond aux critères de recherche spécifiques et place le curseur sur cette ligne.</span><span class="sxs-lookup"><span data-stu-id="dd6de-105">Finds the next row in a table that matches specific search criteria and moves the cursor to that row.</span></span>
  
```cpp
HRESULT FindRow(
LPSRestriction lpRestriction,
BOOKMARK BkOrigin,
ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="dd6de-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd6de-106">Parameters</span></span>

 <span data-ttu-id="dd6de-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="dd6de-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="dd6de-108">dans Pointeur vers une structure [SRestriction](srestriction.md) qui décrit les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="dd6de-108">[in] A pointer to an [SRestriction](srestriction.md) structure that describes the search criteria.</span></span> 
    
 <span data-ttu-id="dd6de-109">_BkOrigin_</span><span class="sxs-lookup"><span data-stu-id="dd6de-109">_BkOrigin_</span></span>
  
> <span data-ttu-id="dd6de-110">dans Signet identifiant la ligne où **FindRow** doit commencer sa recherche.</span><span class="sxs-lookup"><span data-stu-id="dd6de-110">[in] A bookmark identifying the row where **FindRow** should begin its search.</span></span> <span data-ttu-id="dd6de-111">Un signet peut être créé à l'aide de la méthode [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) ou l'une des valeurs prédéfinies suivantes peut être passée.</span><span class="sxs-lookup"><span data-stu-id="dd6de-111">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="dd6de-112">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="dd6de-112">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="dd6de-113">Recherche à partir du début de la table.</span><span class="sxs-lookup"><span data-stu-id="dd6de-113">Searches from the beginning of the table.</span></span> 
    
<span data-ttu-id="dd6de-114">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="dd6de-114">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="dd6de-115">Recherche à partir de la ligne dans la table où se trouve le curseur.</span><span class="sxs-lookup"><span data-stu-id="dd6de-115">Searches from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="dd6de-116">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="dd6de-116">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="dd6de-117">Recherches à partir de la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="dd6de-117">Searches from the end of the table.</span></span> 
    
 <span data-ttu-id="dd6de-118">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="dd6de-118">_ulFlags_</span></span>
  
> <span data-ttu-id="dd6de-119">dans Masque de des indicateurs qui contrôle la direction de la recherche.</span><span class="sxs-lookup"><span data-stu-id="dd6de-119">[in] A bitmask of flags that controls the direction of the search.</span></span> <span data-ttu-id="dd6de-120">L'indicateur suivant peut être défini:</span><span class="sxs-lookup"><span data-stu-id="dd6de-120">The following flag can be set:</span></span>
    
<span data-ttu-id="dd6de-121">DIR_BACKWARD</span><span class="sxs-lookup"><span data-stu-id="dd6de-121">DIR_BACKWARD</span></span> 
  
> <span data-ttu-id="dd6de-122">Effectue une recherche vers l'arrière à partir de la ligne identifiée par le signet.</span><span class="sxs-lookup"><span data-stu-id="dd6de-122">Searches backward from the row identified by the bookmark.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="dd6de-123">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="dd6de-123">Return value</span></span>

<span data-ttu-id="dd6de-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="dd6de-124">S_OK</span></span> 
  
> <span data-ttu-id="dd6de-125">L'opération de recherche a réussi.</span><span class="sxs-lookup"><span data-stu-id="dd6de-125">The find operation was successful.</span></span>
    
<span data-ttu-id="dd6de-126">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="dd6de-126">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="dd6de-127">Le signet dans le paramètre _BkOrigin_ n'est pas valide, car il a été supprimé ou il se trouve au-delà de la dernière ligne demandée.</span><span class="sxs-lookup"><span data-stu-id="dd6de-127">The bookmark in the  _BkOrigin_ parameter is invalid because it has been removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="dd6de-128">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="dd6de-128">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="dd6de-129">Aucune ligne correspondant à la restriction n'a été trouvée.</span><span class="sxs-lookup"><span data-stu-id="dd6de-129">No rows were found that matched the restriction.</span></span>
    
<span data-ttu-id="dd6de-130">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="dd6de-130">MAPI_W_POSITION_CHANGED</span></span>
  
> <span data-ttu-id="dd6de-131">L'appel a réussi, mais le signet utilisé dans l'opération n'est plus défini sur la même ligne que lors de sa dernière utilisation; Si le signet n'a pas été utilisé, il n'est plus dans la même position que lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="dd6de-131">The call succeeded, but the bookmark used in the operation is no longer set at the same row as when it was last used; if the bookmark has not been used, it is no longer in the same position as when it was created.</span></span> <span data-ttu-id="dd6de-132">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="dd6de-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="dd6de-133">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="dd6de-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="dd6de-134">Consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="dd6de-134">See [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dd6de-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd6de-135">Remarks</span></span>

<span data-ttu-id="dd6de-136">La méthode **IMAPITable:: FindRow** localise la première ligne de la table pour qu'elle corresponde à un ensemble de critères de recherche décrits dans la structure **SRestriction** vers laquelle pointe le paramètre _lpRestriction_ .</span><span class="sxs-lookup"><span data-stu-id="dd6de-136">The **IMAPITable::FindRow** method locates the first row in the table to match a set of search criteria described in the **SRestriction** structure pointed to by the  _lpRestriction_ parameter.</span></span> 
  
<span data-ttu-id="dd6de-137">En règle générale, **FindRow** effectue une recherche vers l'avant à partir du signet spécifié.</span><span class="sxs-lookup"><span data-stu-id="dd6de-137">Usually, **FindRow** searches forward from the specified bookmark.</span></span> <span data-ttu-id="dd6de-138">L'appelant peut définir la recherche pour reculer à partir du signet en définissant l'indicateur DIR_BACKWARD dans le paramètre _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="dd6de-138">The caller can set the search to move backward from the bookmark by setting the DIR_BACKWARD flag in the  _ulFlags_ parameter.</span></span> <span data-ttu-id="dd6de-139">La recherche vers le bas commence à partir du signet actif; la recherche vers l'arrière commence à partir de la ligne précédant le signet.</span><span class="sxs-lookup"><span data-stu-id="dd6de-139">Searching forward starts from the current bookmark; searching backward starts from the row prior to the bookmark.</span></span> <span data-ttu-id="dd6de-140">La position de fin de la recherche est juste avant la première ligne ayant satisfait à la restriction.</span><span class="sxs-lookup"><span data-stu-id="dd6de-140">The end position of the search is just before the first row found that satisfied the restriction.</span></span> 
  
<span data-ttu-id="dd6de-141">Si la ligne désignée par le signet dans le paramètre _BkOrigin_ n'existe plus dans le tableau et que la table ne peut pas établir de nouvelle position pour le signet, **FindRow** renvoie MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="dd6de-141">If the row pointed to by the bookmark in the  _BkOrigin_ parameter no longer exists in the table and the table cannot establish a new position for the bookmark, **FindRow** returns MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="dd6de-142">Si la ligne sur laquelle pointe _BkOrigin_ n'existe plus et que la table est en mesure d'établir une nouvelle position pour le signet, **FindRow** renvoie MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="dd6de-142">If the row pointed to by  _BkOrigin_ no longer exists and the table is able to establish a new position for the bookmark, **FindRow** returns MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="dd6de-143">Si le signet transmis dans _BkOrigin_ est BOOKMARK_BEGINNING ou BOOKMARK_END, **FindRow** renvoie MAPI_E_NOT_FOUND si aucune ligne correspondante n'est trouvée.</span><span class="sxs-lookup"><span data-stu-id="dd6de-143">If the bookmark passed in  _BkOrigin_ is either BOOKMARK_BEGINNING or BOOKMARK_END, **FindRow** returns MAPI_E_NOT_FOUND if no matching row is found.</span></span> <span data-ttu-id="dd6de-144">Si le signet utilisé dans _BkOrigin_ est BOOKMARK_CURRENT, **FINDROW** peut renvoyer MAPI_W_POSITION_CHANGED mais pas MAPI_E_INVALID_BOOKMARK, car il y a toujours une position de curseur actuelle.</span><span class="sxs-lookup"><span data-stu-id="dd6de-144">If the bookmark used in  _BkOrigin_ is BOOKMARK_CURRENT, **FindRow** can return MAPI_W_POSITION_CHANGED but not MAPI_E_INVALID_BOOKMARK because there is always a current cursor position.</span></span> 
  
<span data-ttu-id="dd6de-145">La colonne de propriété **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) est requise pour toutes les tables et toutes les implémentations de **FindRow** doivent prendre en charge les appels qui recherchent une ligne en fonction de PR_INSTANCE_KEY.</span><span class="sxs-lookup"><span data-stu-id="dd6de-145">The **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property column is required for all tables, and all implementations of **FindRow** are required to support calls seeking a row based on PR_INSTANCE_KEY.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="dd6de-146">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="dd6de-146">Notes to implementers</span></span>

<span data-ttu-id="dd6de-147">Le type de recherche de préfixe effectué par **FindRow** n'est utile que si la recherche respecte la même direction que l'organisation de la table.</span><span class="sxs-lookup"><span data-stu-id="dd6de-147">The type of prefix searching performed by **FindRow** is only useful when the search follows the same direction as the table organization.</span></span> <span data-ttu-id="dd6de-148">Pour obtenir le comportement requis, la fonction de comparaison impliquée par le **RELOP_GE** passé dans la structure de restriction de propriété doit être la même fonction de comparaison que l'ordre de tri de la table.</span><span class="sxs-lookup"><span data-stu-id="dd6de-148">In order to achieve the required behavior, the comparison function implied by the **RELOP_GE** passed in the property restriction structure should be the same comparison function on which the table sort order is based.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="dd6de-149">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="dd6de-149">Notes to callers</span></span>

<span data-ttu-id="dd6de-150">Vous pouvez utiliser **FindRow** pour prendre en charge le défilement basé sur les chaînes tapées par l'utilisateur, en particulier dans les zones de liste dans les boîtes de dialogue d'adresses.</span><span class="sxs-lookup"><span data-stu-id="dd6de-150">You can use **FindRow** to support scrolling based on strings typed in by the user, especially in list boxes within address dialog boxes.</span></span> <span data-ttu-id="dd6de-151">Dans ce type de défilement, les utilisateurs entrent des préfixes progressivement plus longs d'une valeur de chaîne souhaitée et vous pouvez périodiquement émettre un appel **FindRow** pour accéder à la première ligne correspondant au préfixe.</span><span class="sxs-lookup"><span data-stu-id="dd6de-151">In this type of scrolling, users enter progressively longer prefixes of a desired string value, and you can periodically issue a **FindRow** call to jump to the first row that matches the prefix.</span></span> <span data-ttu-id="dd6de-152">La direction du curseur dépend de la direction dans laquelle la recherche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="dd6de-152">Which direction the cursor jumps depends on which direction the search is set to run.</span></span> 
  
<span data-ttu-id="dd6de-153">Pour utiliser **FindRow**, un signet doit être défini.</span><span class="sxs-lookup"><span data-stu-id="dd6de-153">To use **FindRow**, a bookmark must be set.</span></span> <span data-ttu-id="dd6de-154">La recherche de chaîne peut provenir de n'importe quel signet, y compris des signets prédéfinis indiquant la position actuelle et le début et la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="dd6de-154">The string search can originate from any bookmark, including from the preset bookmarks indicating the current position and the beginning and end of the table.</span></span> <span data-ttu-id="dd6de-155">S'il existe un grand nombre de lignes dans la table, l'opération de recherche peut être lente.</span><span class="sxs-lookup"><span data-stu-id="dd6de-155">If there are a large number of rows in the table, the search operation can be slow.</span></span>
  
<span data-ttu-id="dd6de-156">Utilisez une restriction pour rechercher un préfixe de chaîne pour le défilement, comme suit.</span><span class="sxs-lookup"><span data-stu-id="dd6de-156">Use a restriction to find a string prefix for scrolling as follows.</span></span> <span data-ttu-id="dd6de-157">Pour effectuer une recherche vers l'avant sur une colonne triée par ordre croissant et pour effectuer une recherche vers l'arrière sur une colonne triée dans l'ordre décroissant, transmettez une structure de restriction de propriété dans le paramètre _lpRestriction_ avec la relation **RELOP_GE** et l'objet balise et préfixe de propriété à l'aide du préfixe de _balise_ **GE** __.</span><span class="sxs-lookup"><span data-stu-id="dd6de-157">For forward searching on a column sorted in ascending order and for backward searching on a column sorted in descending order, pass a property restriction structure in the  _lpRestriction_ parameter with the relation **RELOP_GE** and the appropriate property tag and prefix, using the format  _tag_ **GE** _prefix_.</span></span> 
  
<span data-ttu-id="dd6de-158">Pour plus d'informations sur l'utilisation des structures de restriction pour spécifier un filtre, consultez la rubrique [à propos des restrictions](about-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="dd6de-158">For more information about using restriction structures to specify a filter, see [About Restrictions](about-restrictions.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="dd6de-159">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="dd6de-159">MFCMAPI reference</span></span>

<span data-ttu-id="dd6de-160">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="dd6de-160">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="dd6de-161">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="dd6de-161">**File**</span></span>|<span data-ttu-id="dd6de-162">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="dd6de-162">**Function**</span></span>|<span data-ttu-id="dd6de-163">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="dd6de-163">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="dd6de-164">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="dd6de-164">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="dd6de-165">DwThreadFuncLoadTable</span><span class="sxs-lookup"><span data-stu-id="dd6de-165">DwThreadFuncLoadTable</span></span>  <br/> |<span data-ttu-id="dd6de-166">MFCMAPI utilise la méthode **IMAPITable:: FindRow** pour rechercher les lignes correspondant à une restriction.</span><span class="sxs-lookup"><span data-stu-id="dd6de-166">MFCMAPI uses the **IMAPITable::FindRow** method to find rows which match a restriction.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dd6de-167">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd6de-167">See also</span></span>



[<span data-ttu-id="dd6de-168">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="dd6de-168">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="dd6de-169">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="dd6de-169">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="dd6de-170">SRestriction</span><span class="sxs-lookup"><span data-stu-id="dd6de-170">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="dd6de-171">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="dd6de-171">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="dd6de-172">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="dd6de-172">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

