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
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: c3c66b9e54f0776a8afd6b4638d36dec3393dda8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19784087"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="1b124-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="1b124-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="1b124-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1b124-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1b124-105">Extrait la position de ligne de tableau en cours du curseur, basée sur une valeur décimale.</span><span class="sxs-lookup"><span data-stu-id="1b124-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="1b124-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1b124-106">Parameters</span></span>

 <span data-ttu-id="1b124-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="1b124-107">_lpulRow_</span></span>
  
> <span data-ttu-id="1b124-108">[out] Pointeur vers le nombre de la ligne active.</span><span class="sxs-lookup"><span data-stu-id="1b124-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="1b124-109">Numéro de ligne est zéro ; la première ligne dans le tableau est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b124-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="1b124-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="1b124-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="1b124-111">[out] Pointeur vers le numérateur pour la fraction qui identifie la position de la table.</span><span class="sxs-lookup"><span data-stu-id="1b124-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="1b124-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="1b124-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="1b124-113">[out] Pointeur vers le dénominateur de la fraction qui identifie la position de la table.</span><span class="sxs-lookup"><span data-stu-id="1b124-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="1b124-114">Le paramètre _lpulDenominator_ ne peut pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="1b124-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1b124-115">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="1b124-115">Return value</span></span>

<span data-ttu-id="1b124-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1b124-116">S_OK</span></span> 
  
> <span data-ttu-id="1b124-117">La méthode a renvoyé les valeurs valides dans _lpulRow_, _lpulNumerator_et _lpulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="1b124-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1b124-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="1b124-118">Remarks</span></span>

<span data-ttu-id="1b124-119">La méthode **IMAPITable::QueryPosition** détermine la position de ligne en cours et renvoie le nombre de la ligne active et une valeur décimale qui indique sa position relative à la fin de la table.</span><span class="sxs-lookup"><span data-stu-id="1b124-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="1b124-120">MAPI définit la ligne active en tant que la ligne suivante à lire.</span><span class="sxs-lookup"><span data-stu-id="1b124-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1b124-121">Remarques destinées aux responsables de l’implémentation</span><span class="sxs-lookup"><span data-stu-id="1b124-121">Notes to implementers</span></span>

<span data-ttu-id="1b124-122">Vous n’avez pas besoin renvoyer le nombre exact de lignes dans la table pour le paramètre _lpulDenominator_ ; Il peut être une estimation.</span><span class="sxs-lookup"><span data-stu-id="1b124-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="1b124-123">Si vous ne pouvez pas déterminer la ligne actuelle, retourne une valeur de 0xFFFFFFFF _lpulRow_.</span><span class="sxs-lookup"><span data-stu-id="1b124-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="1b124-124">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="1b124-124">Notes to callers</span></span>

<span data-ttu-id="1b124-125">Vous pouvez utiliser **QueryPosition** pour positionner un curseur de défilement dans une barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="1b124-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="1b124-126">Par exemple, dans une table contenant les 100 lignes, si **QueryPosition** renvoie la valeur 75 dans le paramètre _lpulNumerator_ , 100 dans le paramètre _lpulDenominator_ et 75 dans le paramètre _lpulRow_ , vous pouvez placer le défilement case 3/4 la méthode dans la barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="1b124-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="1b124-127">Ne vous fiez pas la valeur de _lpulDenominator_ est le nombre de lignes dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="1b124-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="1b124-128">**QueryPosition** ne peut pas toujours identifier le curseur est positionné sur la ligne exacte.</span><span class="sxs-lookup"><span data-stu-id="1b124-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="1b124-129">Un appel à **QueryPosition** peut impliquer des grandes quantités de mémoire, en particulier pour les grandes tables par catégorie.</span><span class="sxs-lookup"><span data-stu-id="1b124-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="1b124-130">Si le paramètre _lpulRow_ est défini sur 0xFFFFFFFF, trop de mémoire était nécessaire pour **QueryPosition** déterminer la ligne active.</span><span class="sxs-lookup"><span data-stu-id="1b124-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="1b124-131">Appelez la méthode [IMAPI::SeekRowApprox](imapitable-seekrowapprox.md) pour positionner la table à la ligne identifiée par les paramètres _lpulNumerator_ et _lpulDenominator_ .</span><span class="sxs-lookup"><span data-stu-id="1b124-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="1b124-132">Toutefois, pas toujours attendez-vous **SeekRowApprox** pour établir que la position actuelle de la même ligne **que QueryPosition** aurait si la mémoire n’a pas été un facteur.</span><span class="sxs-lookup"><span data-stu-id="1b124-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1b124-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1b124-133">See also</span></span>



[<span data-ttu-id="1b124-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="1b124-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="1b124-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1b124-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

