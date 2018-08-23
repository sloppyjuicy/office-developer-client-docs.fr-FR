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
ms.openlocfilehash: e6803c54ddd60c1bcebbe7a139c2edf2e7f4449d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572086"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="4e374-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="4e374-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="4e374-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e374-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e374-105">Déplace le curseur à une position en fraction approximative dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="4e374-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="4e374-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e374-106">Parameters</span></span>

 <span data-ttu-id="4e374-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="4e374-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="4e374-108">[in] Pointeur vers le numérateur de la fraction qui représente la position de la table.</span><span class="sxs-lookup"><span data-stu-id="4e374-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="4e374-109">Si le paramètre _ulNumerator_ est égale à zéro, le curseur est positionné au début de la table indépendamment de la valeur du dénominateur.</span><span class="sxs-lookup"><span data-stu-id="4e374-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="4e374-110">Si _ulNumerator_ est égal au paramètre _ulDenominator_ , le curseur est positionné après la dernière ligne du tableau.</span><span class="sxs-lookup"><span data-stu-id="4e374-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="4e374-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="4e374-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="4e374-112">[in] Pointeur vers le dénominateur de la fraction qui représente la position de la table.</span><span class="sxs-lookup"><span data-stu-id="4e374-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="4e374-113">Le paramètre _ulDenominator_ ne peut pas être égal à zéro.</span><span class="sxs-lookup"><span data-stu-id="4e374-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4e374-114">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4e374-114">Return value</span></span>

<span data-ttu-id="4e374-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e374-115">S_OK</span></span> 
  
> <span data-ttu-id="4e374-116">L’opération de recherche a réussi.</span><span class="sxs-lookup"><span data-stu-id="4e374-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="4e374-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="4e374-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="4e374-118">Une autre opération est en cours qui empêche la ligne opération de démarrage de recherche.</span><span class="sxs-lookup"><span data-stu-id="4e374-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="4e374-119">L’opération en cours doit être autorisée à effectuer ou il doit être arrêté.</span><span class="sxs-lookup"><span data-stu-id="4e374-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e374-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e374-120">Remarks</span></span>

<span data-ttu-id="4e374-121">La position du curseur dans une table après un appel à la méthode **IMAPI::SeekRowApprox** correspond à la fraction heuristique et peuvent ne pas être exacte.</span><span class="sxs-lookup"><span data-stu-id="4e374-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="4e374-122">Par exemple, certains fournisseurs peuvent implémenter une table par-dessus un arbre binaire, traitement mi-chemin la table en tant que la partie supérieure de l’arborescence pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="4e374-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="4e374-123">Si l’arborescence n’est pas équilibrée, le point à mi-chemin utilisé ne peut pas être exactement au cours de la table.</span><span class="sxs-lookup"><span data-stu-id="4e374-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="4e374-124">Notes aux appelants</span><span class="sxs-lookup"><span data-stu-id="4e374-124">Notes to callers</span></span>

<span data-ttu-id="4e374-125">Appelez **SeekRowApprox** pour fournir les données pour une implémentation de barre de défilement.</span><span class="sxs-lookup"><span data-stu-id="4e374-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="4e374-126">Par exemple, si l’utilisateur place le défilement zone 2/3 vers le bas de la barre de défilement, vous pouvez modéliser cette action en appelant **SeekRowApprox** et en passant une valeur décimale équivalente à l’aide de _ulNumerator_ et _ulDenominator_.</span><span class="sxs-lookup"><span data-stu-id="4e374-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="4e374-127">La recherche **SeekRowApprox** est toujours absolue depuis le début de la table.</span><span class="sxs-lookup"><span data-stu-id="4e374-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="4e374-128">Pour déplacer vers la fin de la table, les valeurs dans _ulNumerator_ et _ulDenominator_ doivent être identiques.</span><span class="sxs-lookup"><span data-stu-id="4e374-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="4e374-129">Utilisez le modèle de numéros est approprié.</span><span class="sxs-lookup"><span data-stu-id="4e374-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="4e374-130">Autrement dit, pour rechercher une position à mi-chemin par le biais de la table, vous pouvez spécifier 1/2, 10/20 ou 50/100.</span><span class="sxs-lookup"><span data-stu-id="4e374-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e374-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e374-131">See also</span></span>



[<span data-ttu-id="4e374-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e374-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

