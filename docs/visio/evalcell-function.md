---
title: EVALCELL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Prend une référence à une cellule qui contient une fonction personnalisée ainsi que sur une ou plusieurs paires nom-valeur à passer à la fonction personnalisée comme arguments (facultatif). Renvoie le résultat de la fonction personnalisée les arguments spécifiés et les valeurs calculé.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788565"
---
# <a name="evalcell-function"></a><span data-ttu-id="a962f-104">EVALCELL, fonction</span><span class="sxs-lookup"><span data-stu-id="a962f-104">EVALCELL Function</span></span>

<span data-ttu-id="a962f-105">Prend une référence à une cellule qui contient une fonction personnalisée ainsi que sur une ou plusieurs paires nom-valeur à passer à la fonction personnalisée comme arguments (facultatif).</span><span class="sxs-lookup"><span data-stu-id="a962f-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="a962f-106">Renvoie le résultat de la fonction personnalisée les arguments spécifiés et les valeurs calculé.</span><span class="sxs-lookup"><span data-stu-id="a962f-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a962f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a962f-107">Syntax</span></span>

<span data-ttu-id="a962f-108">EVALCELL (** *cellRef* **, [** *arg1Name, arg1* **], [** *arg2Name, arg2* **], …)</span><span class="sxs-lookup"><span data-stu-id="a962f-108">EVALCELL(** *cellRef* **,[ ** *arg1Name,arg1* ** ],[ ** *arg2Name,arg2* ** ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a962f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a962f-109">Parameters</span></span>

|<span data-ttu-id="a962f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a962f-110">**Name**</span></span>|<span data-ttu-id="a962f-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a962f-111">**Required/Optional**</span></span>|<span data-ttu-id="a962f-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a962f-112">**Data Type**</span></span>|<span data-ttu-id="a962f-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="a962f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a962f-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="a962f-114">_cellRef_</span></span> <br/> |<span data-ttu-id="a962f-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a962f-115">Required</span></span>  <br/> |<span data-ttu-id="a962f-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a962f-116">**String**</span></span> <br/> |<span data-ttu-id="a962f-117">Une référence à la cellule contenant la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a962f-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="a962f-118">Références entre différentes feuilles sont autorisées.</span><span class="sxs-lookup"><span data-stu-id="a962f-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="a962f-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="a962f-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="a962f-120">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a962f-120">Optional</span></span>  <br/> |<span data-ttu-id="a962f-121">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a962f-121">**String**</span></span> <br/> |<span data-ttu-id="a962f-p104">Nom du premier argument à transmettre à la fonction personnalisée. Les espaces sont acceptés.</span><span class="sxs-lookup"><span data-stu-id="a962f-p104">The name of the first argument to be passed to the custom function. Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="a962f-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="a962f-124">_arg1_</span></span> <br/> |<span data-ttu-id="a962f-125">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a962f-125">Optional</span></span>  <br/> |<span data-ttu-id="a962f-126">**Varie**</span><span class="sxs-lookup"><span data-stu-id="a962f-126">**Varies**</span></span> <br/> |<span data-ttu-id="a962f-127">Valeur du paramètre _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="a962f-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="a962f-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="a962f-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="a962f-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a962f-129">Optional</span></span>  <br/> |<span data-ttu-id="a962f-130">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a962f-130">**String**</span></span> <br/> |<span data-ttu-id="a962f-131">Le nom du deuxième argument à transmettre à la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a962f-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="a962f-132">Les espaces sont autorisés.</span><span class="sxs-lookup"><span data-stu-id="a962f-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="a962f-133">_Arg2_</span><span class="sxs-lookup"><span data-stu-id="a962f-133">_arg2_</span></span> <br/> |<span data-ttu-id="a962f-134">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a962f-134">Optional</span></span>  <br/> |<span data-ttu-id="a962f-135">**Varie**</span><span class="sxs-lookup"><span data-stu-id="a962f-135">**Varies**</span></span> <br/> |<span data-ttu-id="a962f-136">Valeur du paramètre _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="a962f-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a962f-137">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a962f-137">Return value</span></span>

<span data-ttu-id="a962f-138">Nombre</span><span class="sxs-lookup"><span data-stu-id="a962f-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a962f-139">Note</span><span class="sxs-lookup"><span data-stu-id="a962f-139">Remarks</span></span>

<span data-ttu-id="a962f-140">La cellule d’appel n’a pas besoin de spécifier chaque argument utilisé par la fonction personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a962f-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a962f-141">Exemple</span><span class="sxs-lookup"><span data-stu-id="a962f-141">Example</span></span>

<span data-ttu-id="a962f-142">L’exemple suivant montre comment utiliser la fonction EVALCELL conjointement avec la fonction ARG pour trouver la valeur médiane parmi un ensemble de trois valeurs.</span><span class="sxs-lookup"><span data-stu-id="a962f-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="a962f-143">Dans la cellule d’expression, placez le code suivant qui définit la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="a962f-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="a962f-144">Dans les cellules d’appel, placez le code suivant qui appelle la fonction personnalisée :</span><span class="sxs-lookup"><span data-stu-id="a962f-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


