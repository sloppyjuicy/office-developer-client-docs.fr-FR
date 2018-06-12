---
title: SETF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251496
localization_priority: Normal
ms.assetid: fcf415c1-171f-b75f-6e40-2bbdbe8b1cfb
description: Définit la formule d’une cellule.
ms.openlocfilehash: a1e6a12014a77a20c0968b3ed2f7bc25badad8ce
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789619"
---
# <a name="setf-function"></a><span data-ttu-id="e5811-103">SETF, fonction</span><span class="sxs-lookup"><span data-stu-id="e5811-103">SETF Function</span></span>

<span data-ttu-id="e5811-104">Définit la formule d’une cellule.</span><span class="sxs-lookup"><span data-stu-id="e5811-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e5811-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5811-105">Syntax</span></span>

<span data-ttu-id="e5811-106">SETF (GETREF (** *cellule* **), ** *formule* **)</span><span class="sxs-lookup"><span data-stu-id="e5811-106">SETF( GETREF(** *cell* ** ), ** *formula* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5811-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5811-107">Parameters</span></span>

|<span data-ttu-id="e5811-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5811-108">**Name**</span></span>|<span data-ttu-id="e5811-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e5811-109">**Required/Optional**</span></span>|<span data-ttu-id="e5811-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e5811-110">**Data Type**</span></span>|<span data-ttu-id="e5811-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5811-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5811-112">_cellule_</span><span class="sxs-lookup"><span data-stu-id="e5811-112">_cell_</span></span> <br/> |<span data-ttu-id="e5811-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5811-113">Required</span></span>  <br/> |<span data-ttu-id="e5811-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e5811-114">**String**</span></span> <br/> |<span data-ttu-id="e5811-115">La cellule dont la formule à définir.</span><span class="sxs-lookup"><span data-stu-id="e5811-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="e5811-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="e5811-116">_formula_</span></span> <br/> |<span data-ttu-id="e5811-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5811-117">Required</span></span>  <br/> |<span data-ttu-id="e5811-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e5811-118">**String**</span></span> <br/> |<span data-ttu-id="e5811-119">Formule à utiliser</span><span class="sxs-lookup"><span data-stu-id="e5811-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5811-120">Note</span><span class="sxs-lookup"><span data-stu-id="e5811-120">Remarks</span></span>

<span data-ttu-id="e5811-121">Lors de l’évaluation, le résultat de l’expression _formule_ devient la nouvelle formule de _cellule_.</span><span class="sxs-lookup"><span data-stu-id="e5811-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="e5811-122">Si la _formule_ est placé entre guillemets, l’expression entre guillemets est écrit dans la _cellule_.</span><span class="sxs-lookup"><span data-stu-id="e5811-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="e5811-123">Pour définir la _cellule_ à une chaîne, mettez-le _formule_ dans trois jeux de guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="e5811-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="e5811-p102">La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.</span><span class="sxs-lookup"><span data-stu-id="e5811-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="e5811-126">Si la _cellule_ n’est pas spécifié à l’aide de GETREF ou sous forme de chaîne, la fonction renvoie une erreur, et pas la cellule est modifiée.</span><span class="sxs-lookup"><span data-stu-id="e5811-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="e5811-127">Si la _formule_ contient une erreur de syntaxe, la fonction renvoie une erreur et la formule de _cellule_ n’est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="e5811-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e5811-128">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e5811-128">Example 1</span></span>

<span data-ttu-id="e5811-129">SETF (GETREF(Scratch.A1), 1,5 dans \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="e5811-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="e5811-130">Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.</span><span class="sxs-lookup"><span data-stu-id="e5811-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e5811-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e5811-131">Example 2</span></span>

<span data-ttu-id="e5811-132">SETF (GETREF(Scratch.A1), « 1,5 pouces \* 6 + 1 ft »)</span><span class="sxs-lookup"><span data-stu-id="e5811-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="e5811-133">Définir la formule Scratch.a1.</span><span class="sxs-lookup"><span data-stu-id="e5811-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="e5811-134">A1 à l’expression 1,5 dans\*ft 6 + 1.</span><span class="sxs-lookup"><span data-stu-id="e5811-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e5811-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e5811-135">Example 3</span></span>

<span data-ttu-id="e5811-136">SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="e5811-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="e5811-137">Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".</span><span class="sxs-lookup"><span data-stu-id="e5811-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

