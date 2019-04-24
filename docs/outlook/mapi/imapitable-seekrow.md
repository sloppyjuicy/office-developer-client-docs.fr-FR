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
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: fbc990a8c962883aa07987b200d1d2fd55434f93
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328825"
---
# <a name="imapitableseekrow"></a><span data-ttu-id="31e5e-103">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="31e5e-103">IMAPITable::SeekRow</span></span>

  
  
<span data-ttu-id="31e5e-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="31e5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="31e5e-105">Déplace le curseur à une position spécifique dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="31e5e-105">Moves the cursor to a specific position in the table.</span></span>
  
```cpp
HRESULT SeekRow(
BOOKMARK bkOrigin,
LONG lRowCount,
LONG FAR * lplRowsSought
);
```

## <a name="parameters"></a><span data-ttu-id="31e5e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="31e5e-106">Parameters</span></span>

 <span data-ttu-id="31e5e-107">_bkOrigin_</span><span class="sxs-lookup"><span data-stu-id="31e5e-107">_bkOrigin_</span></span>
  
> <span data-ttu-id="31e5e-108">dans Signet identifiant la position de départ de l'opération de recherche.</span><span class="sxs-lookup"><span data-stu-id="31e5e-108">[in] The bookmark identifying the starting position for the seek operation.</span></span> <span data-ttu-id="31e5e-109">Un signet peut être créé à l'aide de la méthode [IMAPITable:: CreateBookmark](imapitable-createbookmark.md) ou l'une des valeurs prédéfinies suivantes peut être passée.</span><span class="sxs-lookup"><span data-stu-id="31e5e-109">A bookmark can be created using the [IMAPITable::CreateBookmark](imapitable-createbookmark.md) method, or one of the following predefined values can be passed.</span></span> 
    
<span data-ttu-id="31e5e-110">BOOKMARK_BEGINNING</span><span class="sxs-lookup"><span data-stu-id="31e5e-110">BOOKMARK_BEGINNING</span></span> 
  
> <span data-ttu-id="31e5e-111">Démarre l'opération Seek à partir du début de la table.</span><span class="sxs-lookup"><span data-stu-id="31e5e-111">Starts the seek operation from the beginning of the table.</span></span> 
    
<span data-ttu-id="31e5e-112">BOOKMARK_CURRENT</span><span class="sxs-lookup"><span data-stu-id="31e5e-112">BOOKMARK_CURRENT</span></span> 
  
> <span data-ttu-id="31e5e-113">Démarre l'opération Seek à partir de la ligne dans la table où se trouve le curseur.</span><span class="sxs-lookup"><span data-stu-id="31e5e-113">Starts the seek operation from the row in the table where the cursor is located.</span></span> 
    
<span data-ttu-id="31e5e-114">BOOKMARK_END</span><span class="sxs-lookup"><span data-stu-id="31e5e-114">BOOKMARK_END</span></span> 
  
> <span data-ttu-id="31e5e-115">Démarre l'opération Seek à partir de la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="31e5e-115">Starts the seek operation from the end of the table.</span></span> 
    
 <span data-ttu-id="31e5e-116">_lRowCount_</span><span class="sxs-lookup"><span data-stu-id="31e5e-116">_lRowCount_</span></span>
  
> <span data-ttu-id="31e5e-117">dans Nombre signé du nombre de lignes à déplacer, en commençant par le signet identifié par le paramètre _bkOrigin_ .</span><span class="sxs-lookup"><span data-stu-id="31e5e-117">[in] The signed count of the number of rows to move, starting from the bookmark identified by the  _bkOrigin_ parameter.</span></span> 
    
 <span data-ttu-id="31e5e-118">_lplRowsSought_</span><span class="sxs-lookup"><span data-stu-id="31e5e-118">_lplRowsSought_</span></span>
  
> <span data-ttu-id="31e5e-119">remarquer Si _lRowCount_ est un pointeur valide sur l'entrée, _lplRowsSought_ pointe vers le nombre de lignes traitées dans l'opération Seek, dont le signe indique le sens de la recherche, à l'avant ou vers l'arrière.</span><span class="sxs-lookup"><span data-stu-id="31e5e-119">[out] If  _lRowCount_ is a valid pointer on input,  _lplRowsSought_ points to the number of rows that were processed in the seek operation, the sign of which indicates the direction of search, forward or backward.</span></span> <span data-ttu-id="31e5e-120">Si _lRowCount_ est négatif, _lplRowsSought_ est négatif.</span><span class="sxs-lookup"><span data-stu-id="31e5e-120">If  _lRowCount_ is negative, then  _lplRowsSought_ is negative.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="31e5e-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="31e5e-121">Return value</span></span>

<span data-ttu-id="31e5e-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="31e5e-122">S_OK</span></span> 
  
> <span data-ttu-id="31e5e-123">L'opération Seek a réussi.</span><span class="sxs-lookup"><span data-stu-id="31e5e-123">The seek operation was successful.</span></span>
    
<span data-ttu-id="31e5e-124">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="31e5e-124">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="31e5e-125">Une autre opération est en cours, ce qui empêche le démarrage de l'opération de recherche de lignes.</span><span class="sxs-lookup"><span data-stu-id="31e5e-125">Another operation is in progress that prevents the row-seeking operation from starting.</span></span> <span data-ttu-id="31e5e-126">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="31e5e-126">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="31e5e-127">MAPI_E_INVALID_BOOKMARK</span><span class="sxs-lookup"><span data-stu-id="31e5e-127">MAPI_E_INVALID_BOOKMARK</span></span> 
  
> <span data-ttu-id="31e5e-128">Le signet spécifié dans le paramètre _bkOrigin_ n'est pas valide car il a été supprimé ou parce qu'il se trouve au-delà de la dernière ligne demandée.</span><span class="sxs-lookup"><span data-stu-id="31e5e-128">The bookmark specified in the  _bkOrigin_ parameter is invalid because it was removed or because it is beyond the last row requested.</span></span> 
    
<span data-ttu-id="31e5e-129">MAPI_W_POSITION_CHANGED</span><span class="sxs-lookup"><span data-stu-id="31e5e-129">MAPI_W_POSITION_CHANGED</span></span> 
  
> <span data-ttu-id="31e5e-130">L'appel a réussi, mais le signet spécifié dans le paramètre _bkOrigin_ n'est plus défini sur la même ligne que lors de sa dernière utilisation.</span><span class="sxs-lookup"><span data-stu-id="31e5e-130">The call succeeded, but the bookmark specified in the  _bkOrigin_ parameter is no longer set at the same row as it was when it was last used.</span></span> <span data-ttu-id="31e5e-131">Si le signet n'a pas été utilisé, il n'est plus dans la même position qu'il l'était lors de sa création.</span><span class="sxs-lookup"><span data-stu-id="31e5e-131">If the bookmark has not been used, it is no longer in the same position as it was when it was created.</span></span> <span data-ttu-id="31e5e-132">Lorsque cet avertissement est renvoyé, l'appel doit être géré comme réussi.</span><span class="sxs-lookup"><span data-stu-id="31e5e-132">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="31e5e-133">Pour tester cet avertissement, utilisez la macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="31e5e-133">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="31e5e-134">Pour plus d'informations, consultez la rubrique [utilisation des macros pour la gestion des erreurs](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="31e5e-134">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="31e5e-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="31e5e-135">Remarks</span></span>

<span data-ttu-id="31e5e-136">La méthode **IMAPITable:: SeekRow** établit une nouvelle position BOOKMARK_CURRENT pour le curseur.</span><span class="sxs-lookup"><span data-stu-id="31e5e-136">The **IMAPITable::SeekRow** method establishes a new BOOKMARK_CURRENT position for the cursor.</span></span> <span data-ttu-id="31e5e-137">Le paramètre _lRowCount_ indique le nombre de lignes que le curseur déplace et le sens du mouvement.</span><span class="sxs-lookup"><span data-stu-id="31e5e-137">The  _lRowCount_ parameter indicates the number of rows that the cursor moves and the direction of movement.</span></span> 
  
<span data-ttu-id="31e5e-138">Si la position résultante se trouve au-delà de la dernière ligne du tableau, le curseur est positionné après la dernière ligne.</span><span class="sxs-lookup"><span data-stu-id="31e5e-138">If the resulting position is beyond the last row of the table, the cursor is positioned after the last row.</span></span> <span data-ttu-id="31e5e-139">Si la position obtenue se trouve avant la première ligne de la table, le curseur est positionné au début de la première ligne.</span><span class="sxs-lookup"><span data-stu-id="31e5e-139">If the resulting position is before the first row of the table, the cursor is positioned at the beginning of the first row.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="31e5e-140">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="31e5e-140">Notes to implementers</span></span>

<span data-ttu-id="31e5e-141">Si la ligne sur laquelle pointe _bkOrigin_ n'existe plus dans le tableau et que vous ne pouvez pas établir une nouvelle position pour le signet, renvoyez MAPI_E_INVALID_BOOKMARK.</span><span class="sxs-lookup"><span data-stu-id="31e5e-141">If the row pointed to by  _bkOrigin_ no longer exists in the table and you cannot establish a new position for the bookmark, return MAPI_E_INVALID_BOOKMARK.</span></span> <span data-ttu-id="31e5e-142">Si la ligne sur laquelle pointe _bkOrigin_ n'existe plus et que vous pouvez établir une nouvelle position pour le signet, renvoyez MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="31e5e-142">If the row pointed to by  _bkOrigin_ no longer exists and you can establish a new position for the bookmark, return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="31e5e-143">Un signet pointant vers une ligne qui est réduite de la vue tableau peut toujours être utilisé.</span><span class="sxs-lookup"><span data-stu-id="31e5e-143">A bookmark pointing to a row that is collapsed out of the table view can still be used.</span></span> <span data-ttu-id="31e5e-144">Si l'appelant tente de déplacer le curseur vers un signet de ce type, déplacez le curseur sur la ligne visible suivante et renvoyez MAPI_W_POSITION_CHANGED.</span><span class="sxs-lookup"><span data-stu-id="31e5e-144">If the caller attempts to move the cursor to such a bookmark, move the cursor to the next visible row and return MAPI_W_POSITION_CHANGED.</span></span> 
  
<span data-ttu-id="31e5e-145">Vous pouvez déplacer les signets des positions réduites en vue, soit au moment de l'utilisation, soit au moment de la réduction de la ligne.</span><span class="sxs-lookup"><span data-stu-id="31e5e-145">You can move bookmarks for positions collapsed out of view, either at the time of use or at the time that the row is collapsed.</span></span> <span data-ttu-id="31e5e-146">Si un signet est déplacé au moment où la ligne est réduite, conservez un bit qui indique si le signet a été déplacé depuis sa dernière utilisation ou, s'il n'a jamais été utilisé, depuis sa création.</span><span class="sxs-lookup"><span data-stu-id="31e5e-146">If a bookmark is moved at the time that the row is collapsed, keep a bit in the bookmark that indicates whether the bookmark has moved since its last use or, if it has never been used, since its creation.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="31e5e-147">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="31e5e-147">Notes to callers</span></span>

<span data-ttu-id="31e5e-148">Pour indiquer un déplacement vers l'arrière pour la propriété **SeekRow**, transmettez une valeur négative dans _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="31e5e-148">To indicate a backward move for **SeekRow**, pass a negative value in  _lRowCount_.</span></span> <span data-ttu-id="31e5e-149">Pour effectuer une recherche jusqu'au début de la table, transmettez zéro dans _lRowCount_ et la valeur BOOKMARK_BEGINNING dans _bkOrigin_.</span><span class="sxs-lookup"><span data-stu-id="31e5e-149">To search to the beginning of the table, pass zero in  _lRowCount_ and the value BOOKMARK_BEGINNING in  _bkOrigin_.</span></span> 
  
<span data-ttu-id="31e5e-150">S'il y a beaucoup de lignes dans la table, l'opération **SeekRow** peut être lente.</span><span class="sxs-lookup"><span data-stu-id="31e5e-150">If there are lots of rows in the table, the **SeekRow** operation can be slow.</span></span> <span data-ttu-id="31e5e-151">Les performances peuvent également être affectées si vous avez besoin d'un nombre de lignes à renvoyer dans le contenu du paramètre _lplRowsSought_ .</span><span class="sxs-lookup"><span data-stu-id="31e5e-151">Performance can also be affected if you require a row count to be returned in the contents of the  _lplRowsSought_ parameter.</span></span> 
  
 <span data-ttu-id="31e5e-152">**SeekRow** renvoie le nombre de lignes réellement recherchées, positives ou négatives, dans la variable désignée par _lRowCount_.</span><span class="sxs-lookup"><span data-stu-id="31e5e-152">**SeekRow** returns the number of rows actually searched through, positive or negative, in the variable pointed to by  _lRowCount_.</span></span> <span data-ttu-id="31e5e-153">En fonctionnement normal, elle doit renvoyer la même valeur pour _lplRowsSought_ que celle qui a été transmise pour _lRowCount_, sauf si la recherche a atteint le début ou la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="31e5e-153">In ordinary operation, it should return the same value for  _lplRowsSought_ as passed in for  _lRowCount_, unless the search reached the beginning or end of the table.</span></span> 
  
<span data-ttu-id="31e5e-154">N'affectez pas un nombre supérieur à 50 à _lRowCount_ .</span><span class="sxs-lookup"><span data-stu-id="31e5e-154">Do not set  _lRowCount_ to a number greater than 50.</span></span> <span data-ttu-id="31e5e-155">Pour rechercher un plus grand nombre de lignes, utilisez la méthode [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md) .</span><span class="sxs-lookup"><span data-stu-id="31e5e-155">To seek through a larger number of rows, use the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="31e5e-156">Référence MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="31e5e-156">MFCMAPI reference</span></span>

<span data-ttu-id="31e5e-157">Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="31e5e-157">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="31e5e-158">**Fichier**</span><span class="sxs-lookup"><span data-stu-id="31e5e-158">**File**</span></span>|<span data-ttu-id="31e5e-159">**Fonction**</span><span class="sxs-lookup"><span data-stu-id="31e5e-159">**Function**</span></span>|<span data-ttu-id="31e5e-160">**Commentaire**</span><span class="sxs-lookup"><span data-stu-id="31e5e-160">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="31e5e-161">MAPIProcessor. cpp</span><span class="sxs-lookup"><span data-stu-id="31e5e-161">MAPIProcessor.cpp</span></span>  <br/> |<span data-ttu-id="31e5e-162">CMAPIProcessor::P rocessMailboxTable</span><span class="sxs-lookup"><span data-stu-id="31e5e-162">CMAPIProcessor::ProcessMailboxTable</span></span>  <br/> |<span data-ttu-id="31e5e-163">MFCMAPI utilise la méthode **IMAPITable:: SeekRow** pour localiser le début de la table avant le traitement.</span><span class="sxs-lookup"><span data-stu-id="31e5e-163">MFCMAPI uses the **IMAPITable::SeekRow** method to locate the beginning of the table before processing.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31e5e-164">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="31e5e-164">See also</span></span>



[<span data-ttu-id="31e5e-165">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="31e5e-165">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="31e5e-166">IMAPITable::FindRow</span><span class="sxs-lookup"><span data-stu-id="31e5e-166">IMAPITable::FindRow</span></span>](imapitable-findrow.md)
  
[<span data-ttu-id="31e5e-167">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="31e5e-167">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="31e5e-168">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="31e5e-168">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="31e5e-169">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="31e5e-169">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="31e5e-170">MFCMAPI comme un exemple de Code</span><span class="sxs-lookup"><span data-stu-id="31e5e-170">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

