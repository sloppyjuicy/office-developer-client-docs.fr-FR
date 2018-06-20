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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: 34bd6de95f731c03466f19e0bc4fd6e2c9910900
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784068"
---
# <a name="imapitablecreatebookmark"></a><span data-ttu-id="b7111-103">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="b7111-103">IMAPITable::CreateBookmark</span></span>

  
  
<span data-ttu-id="b7111-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b7111-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b7111-105">Crée un signet à la position actuelle de la table.</span><span class="sxs-lookup"><span data-stu-id="b7111-105">Creates a bookmark at the table's current position.</span></span>
  
```cpp
HRESULT CreateBookmark(
BOOKMARK FAR * lpbkPosition
);
```

## <a name="parameters"></a><span data-ttu-id="b7111-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7111-106">Parameters</span></span>

 <span data-ttu-id="b7111-107">_lpbkPosition_</span><span class="sxs-lookup"><span data-stu-id="b7111-107">_lpbkPosition_</span></span>
  
> <span data-ttu-id="b7111-108">[out] Pointeur vers la valeur renvoyée signet 32 bits.</span><span class="sxs-lookup"><span data-stu-id="b7111-108">[out] Pointer to the returned 32-bit bookmark value.</span></span> <span data-ttu-id="b7111-109">Ce signet peut ensuite être passé dans un appel à la méthode [IMAPITable::SeekRow](imapitable-seekrow.md) .</span><span class="sxs-lookup"><span data-stu-id="b7111-109">This bookmark can later be passed in a call to the [IMAPITable::SeekRow](imapitable-seekrow.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b7111-110">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="b7111-110">Return value</span></span>

<span data-ttu-id="b7111-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="b7111-111">S_OK</span></span> 
  
> <span data-ttu-id="b7111-112">L'appel a r�ussi et a renvoy� la valeur attendue ou les valeurs.</span><span class="sxs-lookup"><span data-stu-id="b7111-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b7111-113">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="b7111-113">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="b7111-114">L’opération demandée n’a pas pu aboutir.</span><span class="sxs-lookup"><span data-stu-id="b7111-114">The requested operation could not be completed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b7111-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7111-115">Remarks</span></span>

<span data-ttu-id="b7111-116">La méthode **IMAPITable::CreateBookmark** marque une position de la table en créant une valeur appelée un signet.</span><span class="sxs-lookup"><span data-stu-id="b7111-116">The **IMAPITable::CreateBookmark** method marks a table position by creating a value called a bookmark.</span></span> <span data-ttu-id="b7111-117">Un signet peut être utilisé pour revenir à la position identifiée par le signet.</span><span class="sxs-lookup"><span data-stu-id="b7111-117">A bookmark can be used to return to the position identified by the bookmark.</span></span> <span data-ttu-id="b7111-118">La position du signet est associée à l’objet Row dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="b7111-118">The bookmarked position is associated with the object at that row in the table.</span></span> 
  
<span data-ttu-id="b7111-119">Les signets ne sont pas pris en charge sur les tables des pièces jointes et les implémentations de tableau de pièce jointe de **CreateBookmark** retourner MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="b7111-119">Bookmarks are not supported on attachment tables, and attachment table implementations of **CreateBookmark** return MAPI_E_NO_SUPPORT.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="b7111-120">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="b7111-120">Notes to implementers</span></span>

<span data-ttu-id="b7111-121">En raison de la note de frais mémoire de maintenance de positions de curseur avec les signets, limiter le nombre de signets que vous pouvez créer.</span><span class="sxs-lookup"><span data-stu-id="b7111-121">Because of the memory expense of maintaining cursor positions with bookmarks, limit the number of bookmarks that you can create.</span></span> <span data-ttu-id="b7111-122">Lorsque ce nombre est atteint, renvoyer MAPI_E_UNABLE_TO_COMPLETE à partir de tous les appels suivants à **CreateBookmark**.</span><span class="sxs-lookup"><span data-stu-id="b7111-122">When you reach that number, return MAPI_E_UNABLE_TO_COMPLETE from all subsequent calls to **CreateBookmark**.</span></span>
  
<span data-ttu-id="b7111-123">Parfois, un signet pointe vers une ligne qui n’est plus dans la vue table.</span><span class="sxs-lookup"><span data-stu-id="b7111-123">Sometimes a bookmark points to a row that is no longer in the table view.</span></span> <span data-ttu-id="b7111-124">Si un appelant utilise tel qu’un signet, déplacez le curseur sur la ligne suivante visible et s’y arrêter.</span><span class="sxs-lookup"><span data-stu-id="b7111-124">If a caller uses such a bookmark, move the cursor to the next visible row and stop there.</span></span> 
  
<span data-ttu-id="b7111-125">Lorsque l’appelant essaie d’utiliser un signet qui pointe vers une ligne non visibles, car elle a été réduite, renvoie MAPI_W_POSITION_CHANGED après avoir déplacé le signet.</span><span class="sxs-lookup"><span data-stu-id="b7111-125">When the caller attempts to use a bookmark that is pointing to a nonvisible row because it has been collapsed, return MAPI_W_POSITION_CHANGED after moving the bookmark.</span></span> <span data-ttu-id="b7111-126">Vous pouvez repositionner le signet à la ligne suivante visible à ce moment ou lorsque la réduction se produit dans la méthode **SetCollapseState** .</span><span class="sxs-lookup"><span data-stu-id="b7111-126">You can reposition the bookmark to the next visible row either at this time or when the collapsing occurs in the **SetCollapseState** method.</span></span> <span data-ttu-id="b7111-127">Si vous déplacez le signet au moment de la ligne est réduite, vous devez conserver un peu du signet indiquant exactement quand le signet a été déplacé : depuis son dernier utiliser ou s’il n’a jamais été utilisé depuis sa création.</span><span class="sxs-lookup"><span data-stu-id="b7111-127">If you move the bookmark at the time the row is collapsed, you must retain a bit in the bookmark that indicates exactly when the bookmark was moved: since its last use or if it has never been used since its creation.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b7111-128">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="b7111-128">Notes to callers</span></span>

 <span data-ttu-id="b7111-129">**CreateBookmark** alloue de la mémoire pour le signet qu’il crée.</span><span class="sxs-lookup"><span data-stu-id="b7111-129">**CreateBookmark** allocates memory for the bookmark it creates.</span></span> <span data-ttu-id="b7111-130">Libérer les ressources du signet en appelant la méthode [IMAPITable::FreeBookmark](imapitable-freebookmark.md) .</span><span class="sxs-lookup"><span data-stu-id="b7111-130">Release the resources for the bookmark by calling the [IMAPITable::FreeBookmark](imapitable-freebookmark.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b7111-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b7111-131">See also</span></span>



[<span data-ttu-id="b7111-132">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="b7111-132">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="b7111-133">IMAPITable::SeekRow</span><span class="sxs-lookup"><span data-stu-id="b7111-133">IMAPITable::SeekRow</span></span>](imapitable-seekrow.md)
  
[<span data-ttu-id="b7111-134">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b7111-134">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

