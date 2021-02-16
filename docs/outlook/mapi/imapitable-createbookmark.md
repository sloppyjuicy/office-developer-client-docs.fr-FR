---
title: IMAPITableCreateBookmark
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CreateBookmark
api_type:
- COM
ms.assetid: 320af2ff-c2a5-43b1-b3a1-76cb5ffd6a4f
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: c251dacce0d4e1743a74f1ba45e395b6e1c05064
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408823"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="eea1f-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="eea1f-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="eea1f-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eea1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eea1f-105">Crée un signet à la position actuelle du tableau.</span><span class="sxs-lookup"><span data-stu-id="eea1f-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="eea1f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eea1f-106">Parameters</span></span>

 <span data-ttu-id="eea1f-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="eea1f-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="eea1f-108">[out] Pointeur vers la valeur de signet 32 bits renvoyée.</span><span class="sxs-lookup"><span data-stu-id="eea1f-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="eea1f-109">Ce signet peut ensuite être transmis dans un appel à la [méthode IMAPITable::SeekRow.](imapitable-seekrow.md)</span><span class="sxs-lookup"><span data-stu-id="eea1f-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eea1f-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eea1f-110">Return value</span></span>

<span data-ttu-id="eea1f-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="eea1f-111">S_OK</span></span> 
  
> <span data-ttu-id="eea1f-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="eea1f-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="eea1f-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="eea1f-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="eea1f-114">L’opération demandée n’a pas pu être terminée.</span><span class="sxs-lookup"><span data-stu-id="eea1f-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eea1f-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="eea1f-115">Remarks</span></span>

<span data-ttu-id="eea1f-116">La **méthode IMAPITable::CreateBookmark** marque une position de tableau en créant une valeur appelée signet.</span><span class="sxs-lookup"><span data-stu-id="eea1f-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="eea1f-117">Un signet peut être utilisé pour revenir à la position identifiée par le signet.</span><span class="sxs-lookup"><span data-stu-id="eea1f-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="eea1f-118">La position avec signet est associée à l’objet à cette ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="eea1f-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="eea1f-119">Les signets ne sont pas pris en charge sur les tables de pièces jointes et les implémentations de table de pièces jointes **de CreateBookmark** MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="eea1f-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="eea1f-120">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="eea1f-120">Notes to implementers</span></span>

<span data-ttu-id="eea1f-121">En raison de la dépense de mémoire de la gestion des positions du curseur avec des signets, limitez le nombre de signets que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="eea1f-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="eea1f-122">Lorsque vous atteignez ce nombre, renvoyez MAPI_E_UNABLE_TO_COMPLETE de tous les appels suivants **à CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="eea1f-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="eea1f-123">Parfois, un signet pointe vers une ligne qui n’est plus dans l’affichage Tableau.</span><span class="sxs-lookup"><span data-stu-id="eea1f-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="eea1f-124">Si un appelant utilise un signet de ce type, déplacez le curseur sur la ligne visible suivante et arrêtez-le.</span><span class="sxs-lookup"><span data-stu-id="eea1f-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="eea1f-125">Lorsque l’appelant tente d’utiliser un signet qui pointe vers une ligne nonvisible parce qu’elle a été réduire, renvoyer MAPI_W_POSITION_CHANGED après le déplacement du signet.</span><span class="sxs-lookup"><span data-stu-id="eea1f-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="eea1f-126">Vous pouvez repositionner le signet sur la ligne visible suivante à ce moment-là ou lorsque la réduction se produit dans la **méthode SetCollapseState.**</span><span class="sxs-lookup"><span data-stu-id="eea1f-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="eea1f-127">Si vous déplacez le signet au moment où la ligne est réduire, vous devez conserver un bit dans le signet qui indique exactement quand le signet a été déplacé : depuis sa dernière utilisation ou s’il n’a jamais été utilisé depuis sa création.</span><span class="sxs-lookup"><span data-stu-id="eea1f-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eea1f-128">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="eea1f-128">Notes to callers</span></span>

 <span data-ttu-id="eea1f-129">**CreateBookmark alloue** de la mémoire pour le signet qu’il crée.</span><span class="sxs-lookup"><span data-stu-id="eea1f-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="eea1f-130">Libérez les ressources du signet en appelant la [méthode IMAPITable::FreeBookmark.](imapitable-freebookmark.md)</span><span class="sxs-lookup"><span data-stu-id="eea1f-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="eea1f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eea1f-131">See also</span></span>



[<span data-ttu-id="eea1f-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="eea1f-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="eea1f-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="eea1f-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="eea1f-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eea1f-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

