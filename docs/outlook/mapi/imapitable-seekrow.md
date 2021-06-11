---
title: IMAPITableSeekRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRow
api_type:
- COM
ms.assetid: 93ac63ae-f254-45e1-a9b1-347d69d2ed9f
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413044"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="3d669-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="3d669-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="3d669-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d669-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d669-105">Déplace le curseur à une position spécifique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="3d669-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="3d669-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3d669-106">Parameters</span></span>

 <span data-ttu-id="3d669-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="3d669-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="3d669-108">[in] Signet identifiant la position de départ de l’opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="3d669-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="3d669-109">Un signet peut être créé à l’aide de la méthode [IMAPITable::CreateBookmark,](imapitable-createbookmark.md) ou l’une des valeurs prédéfinës suivantes peut être passée.</span><span class="sxs-lookup"><span data-stu-id="3d669-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="3d669-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="3d669-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="3d669-111">Démarre l’opération de recherche à partir du début du tableau.</span><span class="sxs-lookup"><span data-stu-id="3d669-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="3d669-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="3d669-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="3d669-113">Démarre l’opération de recherche à partir de la ligne du tableau où se trouve le curseur.</span><span class="sxs-lookup"><span data-stu-id="3d669-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="3d669-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="3d669-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="3d669-115">Démarre l’opération de recherche à partir de la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="3d669-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="3d669-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="3d669-116">_lRowCount_</span></span>
  
> <span data-ttu-id="3d669-117">[in] Nombre signé du nombre de lignes à déplacer, à partir du signet identifié par le _paramètre bkOrigin._</span><span class="sxs-lookup"><span data-stu-id="3d669-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="3d669-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="3d669-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="3d669-119">[out] Si  _lRowCount_ est un pointeur valide sur l’entrée,  _lplRowsSought_ pointe vers le nombre de lignes qui ont été traitées dans l’opération de recherche, dont le signe indique la direction de la recherche, vers l’avant ou vers l’arrière.</span><span class="sxs-lookup"><span data-stu-id="3d669-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="3d669-120">Si  _lRowCount est_ négatif,  _lplRowsSought_ est négatif.</span><span class="sxs-lookup"><span data-stu-id="3d669-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3d669-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d669-121">Return value</span></span>

<span data-ttu-id="3d669-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="3d669-122">S_OK</span></span> 
  
> <span data-ttu-id="3d669-123">L’opération de recherche a réussi.</span><span class="sxs-lookup"><span data-stu-id="3d669-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="3d669-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="3d669-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="3d669-125">Une autre opération est en cours qui empêche le démarrage de l’opération de recherche de lignes.</span><span class="sxs-lookup"><span data-stu-id="3d669-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="3d669-126">L’opération en cours doit être autorisée ou arrêtée.</span><span class="sxs-lookup"><span data-stu-id="3d669-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="3d669-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="3d669-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="3d669-128">Le signet spécifié dans le paramètre  _bkOrigin_ n’est pas valide car il a été supprimé ou parce qu’il se trouve au-delà de la dernière ligne demandée.</span><span class="sxs-lookup"><span data-stu-id="3d669-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="3d669-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="3d669-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="3d669-130">L’appel a réussi, mais le signet spécifié dans le paramètre  _bkOrigin_ n’est plus définie sur la même ligne que lors de sa dernière utilisation.</span><span class="sxs-lookup"><span data-stu-id="3d669-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="3d669-131">Si le signet n’a pas été utilisé, il n’est plus à la même position qu’au moment de sa création.</span><span class="sxs-lookup"><span data-stu-id="3d669-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="3d669-132">Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi.</span><span class="sxs-lookup"><span data-stu-id="3d669-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="3d669-133">Pour tester cet avertissement, utilisez la macro **HR_FAILED.**</span><span class="sxs-lookup"><span data-stu-id="3d669-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="3d669-134">Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="3d669-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3d669-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d669-135">Remarks</span></span>

<span data-ttu-id="3d669-136">La **méthode IMAPITable::SeekRow** établit une nouvelle position BOOKMARK_CURRENT position du curseur.</span><span class="sxs-lookup"><span data-stu-id="3d669-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="3d669-137">Le  _paramètre lRowCount_ indique le nombre de lignes que le curseur déplace et la direction du mouvement.</span><span class="sxs-lookup"><span data-stu-id="3d669-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="3d669-138">Si la position résultante se trouve au-delà de la dernière ligne du tableau, le curseur est placé après la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="3d669-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="3d669-139">Si la position résultante se trouve avant la première ligne du tableau, le curseur est placé au début de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="3d669-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="3d669-140">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="3d669-140">Notes to implementers</span></span>

<span data-ttu-id="3d669-141">Si la ligne pointée par  _bkOrigin_ n’existe plus dans le tableau et que vous ne pouvez pas établir une nouvelle position pour le signet, renvoyez MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="3d669-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="3d669-142">Si la ligne pointée par  _bkOrigin_ n’existe plus et que vous pouvez établir une nouvelle position pour le signet, renvoyez MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="3d669-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="3d669-143">Un signet pointant vers une ligne qui est réduire en dehors de l’affichage Tableau peut toujours être utilisé.</span><span class="sxs-lookup"><span data-stu-id="3d669-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="3d669-144">Si l’appelant tente de déplacer le curseur vers un signet de ce type, déplacez le curseur vers la ligne visible suivante et renvoyez-MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="3d669-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="3d669-145">Vous pouvez déplacer des signets pour les positions qui sont en dehors de l’affichage, soit au moment de l’utilisation, soit au moment où la ligne est réduire.</span><span class="sxs-lookup"><span data-stu-id="3d669-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="3d669-146">Si un signet est déplacé au moment où la ligne est réduire, conservez un peu dans le signet qui indique si le signet a été déplacé depuis sa dernière utilisation ou, s’il n’a jamais été utilisé, depuis sa création.</span><span class="sxs-lookup"><span data-stu-id="3d669-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="3d669-147">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="3d669-147">Notes to callers</span></span>

<span data-ttu-id="3d669-148">Pour indiquer un déplacement vers l’arrière **pour SeekRow**, passez une valeur négative dans  _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="3d669-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="3d669-149">Pour rechercher au début du tableau, passez zéro dans  _lRowCount_ et la valeur BOOKMARK_BEGINNING dans  _bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="3d669-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="3d669-150">S’il y a beaucoup de lignes dans le tableau, **l’opération SeekRow** peut être lente.</span><span class="sxs-lookup"><span data-stu-id="3d669-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="3d669-151">Les performances peuvent également être affectées si vous avez besoin de retourner un nombre de lignes dans le contenu du _paramètre lplRowsSought._</span><span class="sxs-lookup"><span data-stu-id="3d669-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="3d669-152">**SeekRow** renvoie le nombre de lignes réellement recherchés dans, positif ou négatif, dans la variable pointée par  _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="3d669-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="3d669-153">En opération ordinaire, elle doit renvoyer la même valeur pour  _lplRowsSought_ que pour  _lRowCount_, sauf si la recherche a atteint le début ou la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="3d669-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="3d669-154">Ne définissez  _pas lRowCount_ sur un nombre supérieur à 50.</span><span class="sxs-lookup"><span data-stu-id="3d669-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="3d669-155">Pour rechercher un plus grand nombre de lignes, utilisez la méthode [IMAPITable::SeekRowApprox.](imapitable-seekrowapprox.md)</span><span class="sxs-lookup"><span data-stu-id="3d669-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="3d669-156">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="3d669-156">MFCMAPI reference</span></span>

<span data-ttu-id="3d669-157">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="3d669-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="3d669-158">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="3d669-158">**File**</span></span>|<span data-ttu-id="3d669-159">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="3d669-159">**Function**</span></span>|<span data-ttu-id="3d669-160">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="3d669-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3d669-161">MAPIProcessor.cpp</span><span class="sxs-lookup"><span data-stu-id="3d669-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="3d669-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="3d669-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="3d669-163">MFCMAPI utilise la **méthode IMAPITable::SeekRow** pour localiser le début de la table avant le traitement.</span><span class="sxs-lookup"><span data-stu-id="3d669-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3d669-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3d669-164">See also</span></span>



[<span data-ttu-id="3d669-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="3d669-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="3d669-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="3d669-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="3d669-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="3d669-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="3d669-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="3d669-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="3d669-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3d669-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="3d669-170">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="3d669-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

