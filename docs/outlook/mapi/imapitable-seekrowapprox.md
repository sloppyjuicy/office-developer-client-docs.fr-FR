---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328839"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="f5720-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="f5720-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="f5720-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f5720-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f5720-105">Place le curseur sur une position fractionnaire approximative dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="f5720-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="f5720-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f5720-106">Parameters</span></span>

 <span data-ttu-id="f5720-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="f5720-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="f5720-108">dans Pointeur vers le numérateur de la fraction représentant la position de la table.</span><span class="sxs-lookup"><span data-stu-id="f5720-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="f5720-109">Si le paramètre _ulNumerator_ est égal à zéro, le curseur est positionné au début de la table, quelle que soit la valeur du dénominateur.</span><span class="sxs-lookup"><span data-stu-id="f5720-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="f5720-110">Si _ulNumerator_ est égal au paramètre _ulDenominator_ , le curseur est positionné après la dernière ligne de tableau.</span><span class="sxs-lookup"><span data-stu-id="f5720-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="f5720-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="f5720-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="f5720-112">dans Pointeur vers le dénominateur de la fraction représentant la position de la table.</span><span class="sxs-lookup"><span data-stu-id="f5720-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="f5720-113">Le paramètre _ulDenominator_ ne peut pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="f5720-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f5720-114">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f5720-114">Return value</span></span>

<span data-ttu-id="f5720-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="f5720-115">S_OK</span></span> 
  
> <span data-ttu-id="f5720-116">L'opération Seek a réussi.</span><span class="sxs-lookup"><span data-stu-id="f5720-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="f5720-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f5720-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f5720-118">Une autre opération est en cours, ce qui empêche le démarrage de l'opération de recherche de ligne.</span><span class="sxs-lookup"><span data-stu-id="f5720-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="f5720-119">L'opération en cours doit être autorisée ou elle doit être arrêtée.</span><span class="sxs-lookup"><span data-stu-id="f5720-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f5720-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="f5720-120">Remarks</span></span>

<span data-ttu-id="f5720-121">La position du curseur dans un tableau après un appel à la méthode **IMAPITable:: SeekRowApprox** est la fraction de manière heuristique et peut ne pas être exacte.</span><span class="sxs-lookup"><span data-stu-id="f5720-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="f5720-122">Par exemple, certains fournisseurs peuvent implémenter une table en haut d'une arborescence binaire, en traitant le point central de la table en tant que haut de l'arborescence pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="f5720-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="f5720-123">Si l'arborescence n'est pas équilibrée, le point central utilisé peut ne pas être exactement au milieu de la table.</span><span class="sxs-lookup"><span data-stu-id="f5720-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f5720-124">Remarques pour les appelants</span><span class="sxs-lookup"><span data-stu-id="f5720-124">Notes to callers</span></span>

<span data-ttu-id="f5720-125">Appelez **SeekRowApprox** pour fournir les données d'une implémentation de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="f5720-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="f5720-126">Par exemple, si l'utilisateur positionne la case de défilement 2/3 vers le bas dans la barre de défilement, vous pouvez modéliser cette action en appelant **SeekRowApprox** et en transmettant une valeur fractionnaire équivalente à l'aide de _UlNumerator_ et de _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="f5720-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="f5720-127">La recherche **SeekRowApprox** est toujours absolue à partir du début de la table.</span><span class="sxs-lookup"><span data-stu-id="f5720-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="f5720-128">Pour accéder à la fin de la table, les valeurs dans _ulNumerator_ et _ulDenominator_ doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="f5720-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="f5720-129">Utilisez un modèle de nombre approprié.</span><span class="sxs-lookup"><span data-stu-id="f5720-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="f5720-130">Autrement dit, pour rechercher une position à mi-parcours de la table, vous pouvez spécifier 1/2, 10/20 ou 50/100.</span><span class="sxs-lookup"><span data-stu-id="f5720-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f5720-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f5720-131">See also</span></span>



[<span data-ttu-id="f5720-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f5720-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

