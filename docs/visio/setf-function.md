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
description: Définit la formule d'une cellule.
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325836"
---
# <a name="setf-function"></a><span data-ttu-id="891b3-103">Fonction SETF</span><span class="sxs-lookup"><span data-stu-id="891b3-103">SETF Function</span></span>

<span data-ttu-id="891b3-104">Définit la formule d'une cellule.</span><span class="sxs-lookup"><span data-stu-id="891b3-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="891b3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="891b3-105">Syntax</span></span>

<span data-ttu-id="891b3-106">SETF (GETREF (\* \* *Cell* \* \*), \* \* *Formula* \* \*)</span><span class="sxs-lookup"><span data-stu-id="891b3-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="891b3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="891b3-107">Parameters</span></span>

|<span data-ttu-id="891b3-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="891b3-108">**Name**</span></span>|<span data-ttu-id="891b3-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="891b3-109">**Required/Optional**</span></span>|<span data-ttu-id="891b3-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="891b3-110">**Data Type**</span></span>|<span data-ttu-id="891b3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="891b3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="891b3-112">_Cell_</span><span class="sxs-lookup"><span data-stu-id="891b3-112">_cell_</span></span> <br/> |<span data-ttu-id="891b3-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="891b3-113">Required</span></span>  <br/> |<span data-ttu-id="891b3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="891b3-114">**String**</span></span> <br/> |<span data-ttu-id="891b3-115">Cellule dont la formule doit être définie.</span><span class="sxs-lookup"><span data-stu-id="891b3-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="891b3-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="891b3-116">_formula_</span></span> <br/> |<span data-ttu-id="891b3-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="891b3-117">Required</span></span>  <br/> |<span data-ttu-id="891b3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="891b3-118">**String**</span></span> <br/> |<span data-ttu-id="891b3-119">Formule à utiliser</span><span class="sxs-lookup"><span data-stu-id="891b3-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="891b3-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="891b3-120">Remarks</span></span>

<span data-ttu-id="891b3-121">Lors de l'évaluation, le résultat de l'expression dans _Formula_ devient la nouvelle formule dans la _cellule_.</span><span class="sxs-lookup"><span data-stu-id="891b3-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="891b3-122">Si la _formule_ est placée entre guillemets, l'expression quotée est écrite dans la _cellule_.</span><span class="sxs-lookup"><span data-stu-id="891b3-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="891b3-123">Pour définir la _cellule_ sur une chaîne, mettez la _formule_ entre trois guillemets.</span><span class="sxs-lookup"><span data-stu-id="891b3-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="891b3-p102">La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.</span><span class="sxs-lookup"><span data-stu-id="891b3-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="891b3-126">Si la _cellule_ n'est pas spécifiée à l'aide de getRef ou sous forme de chaîne, la fonction renvoie une erreur et aucune formule de cellule n'est modifiée.</span><span class="sxs-lookup"><span data-stu-id="891b3-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="891b3-127">Si la _formule_ contient une erreur de syntaxe, la fonction renvoie une erreur et la formule dans la _cellule_ n'est pas modifiée.</span><span class="sxs-lookup"><span data-stu-id="891b3-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="891b3-128">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="891b3-128">Example 1</span></span>

<span data-ttu-id="891b3-129">SETF (GETREF (Scratch. a1), 1,5 en \* 6 + 1 ft)</span><span class="sxs-lookup"><span data-stu-id="891b3-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="891b3-130">Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.</span><span class="sxs-lookup"><span data-stu-id="891b3-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="891b3-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="891b3-131">Example 2</span></span>

<span data-ttu-id="891b3-132">SETF (GETREF (Scratch. a1), "1,5 en \* 6 + 1 ft")</span><span class="sxs-lookup"><span data-stu-id="891b3-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="891b3-133">Définit la formule de travail.</span><span class="sxs-lookup"><span data-stu-id="891b3-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="891b3-134">A1 à l'expression 1,5 en\*6 + 1 ft.</span><span class="sxs-lookup"><span data-stu-id="891b3-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="891b3-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="891b3-135">Example 3</span></span>

<span data-ttu-id="891b3-136">SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="891b3-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="891b3-137">Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".</span><span class="sxs-lookup"><span data-stu-id="891b3-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

