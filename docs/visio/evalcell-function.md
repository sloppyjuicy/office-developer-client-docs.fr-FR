---
title: EVALCELL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Prend une référence à une cellule qui contient une fonction personnalisée, ainsi qu'une ou plusieurs paires nom-valeur à transmettre à la fonction personnalisée en tant qu'arguments (facultatif). Renvoie le résultat calculé de la fonction personnalisée selon les arguments et les valeurs spécifiés.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329070"
---
# <a name="evalcell-function"></a><span data-ttu-id="716eb-104">Fonction EVALCELL</span><span class="sxs-lookup"><span data-stu-id="716eb-104">EVALCELL Function</span></span>

<span data-ttu-id="716eb-105">Prend une référence à une cellule qui contient une fonction personnalisée, ainsi qu'une ou plusieurs paires nom-valeur à transmettre à la fonction personnalisée en tant qu'arguments (facultatif).</span><span class="sxs-lookup"><span data-stu-id="716eb-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="716eb-106">Renvoie le résultat calculé de la fonction personnalisée selon les arguments et les valeurs spécifiés.</span><span class="sxs-lookup"><span data-stu-id="716eb-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="716eb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="716eb-107">Syntax</span></span>

<span data-ttu-id="716eb-108">EVALCELL (\* \* *cellRef* \* *, [* \* *arg1Name, arg1* \* *], [* \* *arg2Name, arg2* \* \*],...)</span><span class="sxs-lookup"><span data-stu-id="716eb-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="716eb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="716eb-109">Parameters</span></span>

|<span data-ttu-id="716eb-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="716eb-110">**Name**</span></span>|<span data-ttu-id="716eb-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="716eb-111">**Required/Optional**</span></span>|<span data-ttu-id="716eb-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="716eb-112">**Data Type**</span></span>|<span data-ttu-id="716eb-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="716eb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="716eb-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="716eb-114">_cellRef_</span></span> <br/> |<span data-ttu-id="716eb-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="716eb-115">Required</span></span>  <br/> |<span data-ttu-id="716eb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="716eb-116">**String**</span></span> <br/> |<span data-ttu-id="716eb-117">Référence à la cellule contenant la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="716eb-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="716eb-118">Les références inter-feuilles sont acceptées.</span><span class="sxs-lookup"><span data-stu-id="716eb-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="716eb-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="716eb-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="716eb-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="716eb-120">Optional</span></span>  <br/> |<span data-ttu-id="716eb-121">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="716eb-121">**String**</span></span> <br/> |<span data-ttu-id="716eb-122">Nom du premier argument à transmettre à la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="716eb-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="716eb-123">Les espaces sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="716eb-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="716eb-124">_Arg1_</span><span class="sxs-lookup"><span data-stu-id="716eb-124">_arg1_</span></span> <br/> |<span data-ttu-id="716eb-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="716eb-125">Optional</span></span>  <br/> |<span data-ttu-id="716eb-126">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="716eb-126">**Varies**</span></span> <br/> |<span data-ttu-id="716eb-127">Valeur du paramètre _Arg1_ .</span><span class="sxs-lookup"><span data-stu-id="716eb-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="716eb-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="716eb-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="716eb-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="716eb-129">Optional</span></span>  <br/> |<span data-ttu-id="716eb-130">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="716eb-130">**String**</span></span> <br/> |<span data-ttu-id="716eb-131">Nom du deuxième argument à transmettre à la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="716eb-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="716eb-132">Les espaces sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="716eb-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="716eb-133">_Arg2_</span><span class="sxs-lookup"><span data-stu-id="716eb-133">_arg2_</span></span> <br/> |<span data-ttu-id="716eb-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="716eb-134">Optional</span></span>  <br/> |<span data-ttu-id="716eb-135">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="716eb-135">**Varies**</span></span> <br/> |<span data-ttu-id="716eb-136">Valeur du paramètre _Arg2_ .</span><span class="sxs-lookup"><span data-stu-id="716eb-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="716eb-137">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="716eb-137">Return value</span></span>

<span data-ttu-id="716eb-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="716eb-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="716eb-139">Remarques</span><span class="sxs-lookup"><span data-stu-id="716eb-139">Remarks</span></span>

<span data-ttu-id="716eb-140">La cellule d’appel n’a pas besoin de spécifier chaque argument utilisé par la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="716eb-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="716eb-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="716eb-141">Example</span></span>

<span data-ttu-id="716eb-142">L’exemple suivant montre comment utiliser la fonction EVALCELL conjointement avec la fonction ARG pour trouver la valeur médiane parmi un ensemble de trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="716eb-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="716eb-143">Dans la cellule d’expression, placez le code suivant qui définit la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="716eb-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="716eb-144">Dans les cellules d’appel, placez le code suivant qui appelle la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="716eb-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


