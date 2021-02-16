---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415662"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="51f99-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="51f99-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="51f99-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51f99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51f99-105">Extrait la position de ligne de tableau actuelle du curseur, en fonction d’une valeur fractionnaire.</span><span class="sxs-lookup"><span data-stu-id="51f99-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="51f99-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51f99-106">Parameters</span></span>

 <span data-ttu-id="51f99-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="51f99-107">_lpulRow_</span></span>
  
> <span data-ttu-id="51f99-108">[out] Pointeur vers le numéro de la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="51f99-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="51f99-109">Le numéro de ligne est de base zéro ; la première ligne du tableau est zéro.</span><span class="sxs-lookup"><span data-stu-id="51f99-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="51f99-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="51f99-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="51f99-111">[out] Pointeur vers le numérateur pour la fraction identifiant la position du tableau.</span><span class="sxs-lookup"><span data-stu-id="51f99-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="51f99-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="51f99-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="51f99-113">[out] Pointeur vers le dénominateur de la fraction identifiant la position du tableau.</span><span class="sxs-lookup"><span data-stu-id="51f99-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="51f99-114">Le  _paramètre lpulDenominator ne peut_ pas être zéro.</span><span class="sxs-lookup"><span data-stu-id="51f99-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="51f99-115">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51f99-115">Return value</span></span>

<span data-ttu-id="51f99-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="51f99-116">S_OK</span></span> 
  
> <span data-ttu-id="51f99-117">La méthode a renvoyé des valeurs valides dans  _lpulRow,_  _lpulNumerator_ et  _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="51f99-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51f99-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="51f99-118">Remarks</span></span>

<span data-ttu-id="51f99-119">La **méthode IMAPITable::QueryPosition** détermine la position de ligne actuelle et renvoie le numéro de la ligne actuelle et une valeur fractionnaire indiquant sa position relative à la fin du tableau.</span><span class="sxs-lookup"><span data-stu-id="51f99-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="51f99-120">MAPI définit la ligne actuelle comme ligne suivante à lire.</span><span class="sxs-lookup"><span data-stu-id="51f99-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="51f99-121">Remarques pour les responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="51f99-121">Notes to implementers</span></span>

<span data-ttu-id="51f99-122">Vous n’avez pas besoin de renvoyer le nombre exact de lignes dans la table pour le  _paramètre lpulDenominator_ ; Il peut s’agit d’une estimation.</span><span class="sxs-lookup"><span data-stu-id="51f99-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="51f99-123">Si vous ne pouvez pas déterminer la ligne actuelle, renvoyez une valeur de 0xFFFFFFFF dans  _lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="51f99-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="51f99-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="51f99-124">Notes to callers</span></span>

<span data-ttu-id="51f99-125">Vous pouvez utiliser **QueryPosition** pour positionner une case de défilement dans une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="51f99-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="51f99-126">Par exemple, dans un tableau de 100 lignes, si **QueryPosition** renvoie la valeur 75 dans le paramètre  _lpulNumerator,_ 100 dans le paramètre  _lpulDenominator_ et 75 dans le paramètre  _lpulRow,_ vous pouvez positionner la case de défilement 3/4 de la manière dans la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="51f99-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="51f99-127">Ne comptez pas sur la valeur  _dans lpulDenominator_ qui est le nombre de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="51f99-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="51f99-128">**QueryPosition ne** peut pas toujours identifier la ligne exacte sur la position du curseur.</span><span class="sxs-lookup"><span data-stu-id="51f99-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="51f99-129">Un appel à **QueryPosition** peut impliquer de grandes quantités de mémoire, en particulier pour les tables classées de grande taille.</span><span class="sxs-lookup"><span data-stu-id="51f99-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="51f99-130">Si le  _paramètre lpulRow_ est 0xFFFFFFFF, trop de mémoire était nécessaire pour **que QueryPosition** détermine la ligne actuelle.</span><span class="sxs-lookup"><span data-stu-id="51f99-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="51f99-131">Appelez [la méthode IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) pour positionner la table sur la ligne identifiée par les paramètres _lpulNumerator_ et _lpulDenominator._</span><span class="sxs-lookup"><span data-stu-id="51f99-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="51f99-132">Toutefois, n’attendez pas toujours que **SeekRowApprox** établisse en tant que position actuelle la même ligne **que QueryPosition** aurait si la mémoire n’avait pas été un facteur.</span><span class="sxs-lookup"><span data-stu-id="51f99-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51f99-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51f99-133">See also</span></span>



[<span data-ttu-id="51f99-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="51f99-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="51f99-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51f99-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

