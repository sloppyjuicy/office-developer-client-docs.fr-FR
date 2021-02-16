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
ms.openlocfilehash: 63050de92394ebbdce6cfe053e15347ca3ce5c7f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425973"
---
# <a name="setf-function"></a><span data-ttu-id="a1d02-103">Fonction SETF</span><span class="sxs-lookup"><span data-stu-id="a1d02-103">SETF Function</span></span>

<span data-ttu-id="a1d02-104">Définit la formule d’une cellule.</span><span class="sxs-lookup"><span data-stu-id="a1d02-104">Sets a cell's formula.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a1d02-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a1d02-105">Syntax</span></span>

<span data-ttu-id="a1d02-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a1d02-106">SETF( GETREF(\*\* *cell* \*\* ), \*\* *formula* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a1d02-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a1d02-107">Parameters</span></span>

|<span data-ttu-id="a1d02-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a1d02-108">**Name**</span></span>|<span data-ttu-id="a1d02-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a1d02-109">**Required/Optional**</span></span>|<span data-ttu-id="a1d02-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a1d02-110">**Data Type**</span></span>|<span data-ttu-id="a1d02-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a1d02-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a1d02-112">_cell_</span><span class="sxs-lookup"><span data-stu-id="a1d02-112">_cell_</span></span> <br/> |<span data-ttu-id="a1d02-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a1d02-113">Required</span></span>  <br/> |<span data-ttu-id="a1d02-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a1d02-114">**String**</span></span> <br/> |<span data-ttu-id="a1d02-115">Cellule dont la formule doit être définie.</span><span class="sxs-lookup"><span data-stu-id="a1d02-115">The cell whose formula to set.</span></span>  <br/> |
| <span data-ttu-id="a1d02-116">_formula_</span><span class="sxs-lookup"><span data-stu-id="a1d02-116">_formula_</span></span> <br/> |<span data-ttu-id="a1d02-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a1d02-117">Required</span></span>  <br/> |<span data-ttu-id="a1d02-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a1d02-118">**String**</span></span> <br/> |<span data-ttu-id="a1d02-119">Formule à utiliser</span><span class="sxs-lookup"><span data-stu-id="a1d02-119">The formula to use.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1d02-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="a1d02-120">Remarks</span></span>

<span data-ttu-id="a1d02-121">Lorsqu’elle est évaluée, le résultat de l’expression _dans_ la formule devient la nouvelle formule dans la _cellule._</span><span class="sxs-lookup"><span data-stu-id="a1d02-121">When evaluated, the result of the expression in  _formula_ becomes the new formula in  _cell_.</span></span> <span data-ttu-id="a1d02-122">Si _la formule_ est entre guillemets, l’expression entre guillemets est écrite dans la _cellule._</span><span class="sxs-lookup"><span data-stu-id="a1d02-122">If  _formula_ is enclosed in quotation marks, the quoted expression is written to  _cell_.</span></span> <span data-ttu-id="a1d02-123">Pour définir  _une cellule_ sur une chaîne, inséz-la  _entre_ trois guillemets.</span><span class="sxs-lookup"><span data-stu-id="a1d02-123">To set  _cell_ to a string, enclose  _formula_ in three sets of quotation marks.</span></span> 
  
<span data-ttu-id="a1d02-p102">La cellule cible doit être définie à l’aide d’une référence GETREF() ou sous forme de chaîne pour éviter la circularité. Il est préférable d’utiliser GETREF, car Microsoft Visio peut ajuster les références lorsque la forme est déplacée vers un autre document.</span><span class="sxs-lookup"><span data-stu-id="a1d02-p102">The target cell must be specified using a GETREF() reference or as a string to avoid circularity. Using GETREF is preferred, because Microsoft Visio can adjust references when the shape is moved to a different document.</span></span>
  
<span data-ttu-id="a1d02-126">Si  _la cellule_ n’est pas spécifiée à l’aide de GETREF ou en tant que chaîne, la fonction renvoie une erreur et aucune formule de cellule n’est modifiée.</span><span class="sxs-lookup"><span data-stu-id="a1d02-126">If  _cell_ is not specified using GETREF or as a string, the function returns an error, and no cell's formula is changed.</span></span> <span data-ttu-id="a1d02-127">Si _la formule_ contient une erreur de syntaxe, la fonction renvoie une erreur et la formule de la cellule n’est pas modifiée. </span><span class="sxs-lookup"><span data-stu-id="a1d02-127">If  _formula_ contains a syntax error, the function returns an error, and the formula in  _cell_ is not changed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a1d02-128">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a1d02-128">Example 1</span></span>

<span data-ttu-id="a1d02-129">SETF( GETREF(Scratch.A1), 1,5 en \* 6 + 1 pi)</span><span class="sxs-lookup"><span data-stu-id="a1d02-129">SETF( GETREF(Scratch.A1), 1.5 in \* 6 + 1 ft)</span></span>
  
<span data-ttu-id="a1d02-130">Cette commande donne à la formule Scratch.A1 une valeur de 533,4 millimètres.</span><span class="sxs-lookup"><span data-stu-id="a1d02-130">Sets the formula of Scratch.A1 to 21 inches.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a1d02-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a1d02-131">Example 2</span></span>

<span data-ttu-id="a1d02-132">SETF( GETREF(Scratch.A1), « 1,5 en \* 6 + 1 m »)</span><span class="sxs-lookup"><span data-stu-id="a1d02-132">SETF( GETREF(Scratch.A1), "1.5 in \* 6 + 1 ft")</span></span>
  
<span data-ttu-id="a1d02-133">Définit la formule de Scratch.</span><span class="sxs-lookup"><span data-stu-id="a1d02-133">Sets the formula of Scratch.</span></span> <span data-ttu-id="a1d02-134">A1 to the expression 1.5 in \* 6+1 ft.</span><span class="sxs-lookup"><span data-stu-id="a1d02-134">A1 to the expression 1.5 in\*6+1 ft.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a1d02-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="a1d02-135">Example 3</span></span>

<span data-ttu-id="a1d02-136">SETF(GETREF(Scratch.A1), """Dites """"ahh""""""")</span><span class="sxs-lookup"><span data-stu-id="a1d02-136">SETF( GETREF(Scratch.A1), """Say """"ahh""""""")</span></span>
  
<span data-ttu-id="a1d02-137">Donne pour valeur à la cellule Scratch.A1 la chaîne "Dites ""ahh""" ce qui revient à Dites "ahh".</span><span class="sxs-lookup"><span data-stu-id="a1d02-137">Sets the formula of Scratch.A1 to the string "Say ""ahh""" which evaluates to Say "ahh".</span></span>
  

