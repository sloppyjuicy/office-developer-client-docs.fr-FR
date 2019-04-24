---
title: RGB Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants rouge, vert et bleu, où chacun est un nombre compris entre 0 et 255 inclus, ou une expression qui renvoie à ce nombre.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326739"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="a8973-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a8973-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a8973-105">Renvoie une valeur représentant un index dans la palette de couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="a8973-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="a8973-106">Il spécifie une couleur par ses composants rouge, vert et bleu, où chacun est un nombre compris entre 0 et 255 inclus, ou une expression qui renvoie à ce nombre.</span><span class="sxs-lookup"><span data-stu-id="a8973-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a8973-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8973-107">Syntax</span></span>

<span data-ttu-id="a8973-108">RVB (\* \* *rouge* \* \*, \* \* *vert* \* \*, \* \* *bleu* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a8973-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a8973-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8973-109">Parameters</span></span>

|<span data-ttu-id="a8973-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a8973-110">**Name**</span></span>|<span data-ttu-id="a8973-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a8973-111">**Required/Optional**</span></span>|<span data-ttu-id="a8973-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a8973-112">**Data Type**</span></span>|<span data-ttu-id="a8973-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8973-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a8973-114">_b_</span><span class="sxs-lookup"><span data-stu-id="a8973-114">_red_</span></span> <br/> |<span data-ttu-id="a8973-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8973-115">Required</span></span>  <br/> |<span data-ttu-id="a8973-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="a8973-116">**Number**</span></span> <br/> |<span data-ttu-id="a8973-117">Composante rouge</span><span class="sxs-lookup"><span data-stu-id="a8973-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="a8973-118">_informatique_</span><span class="sxs-lookup"><span data-stu-id="a8973-118">_green_</span></span> <br/> |<span data-ttu-id="a8973-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8973-119">Required</span></span>  <br/> |<span data-ttu-id="a8973-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="a8973-120">**Number**</span></span> <br/> |<span data-ttu-id="a8973-121">Composante vert</span><span class="sxs-lookup"><span data-stu-id="a8973-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="a8973-122">_Blue_</span><span class="sxs-lookup"><span data-stu-id="a8973-122">_blue_</span></span> <br/> |<span data-ttu-id="a8973-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8973-123">Required</span></span>  <br/> |<span data-ttu-id="a8973-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="a8973-124">**Nmber**</span></span> <br/> |<span data-ttu-id="a8973-125">Composante bleu</span><span class="sxs-lookup"><span data-stu-id="a8973-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a8973-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8973-126">Return value</span></span>

<span data-ttu-id="a8973-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="a8973-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8973-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8973-128">Remarks</span></span>

<span data-ttu-id="a8973-129">Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs actuelle, elle est automatiquement ajoutée.</span><span class="sxs-lookup"><span data-stu-id="a8973-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="a8973-130">Le tableau ci-après présente les couleurs standard et les valeurs Rouge, Vert et Bleu qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="a8973-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="a8973-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="a8973-131">**Color**</span></span>|<span data-ttu-id="a8973-132">**Valeur rouge**</span><span class="sxs-lookup"><span data-stu-id="a8973-132">**Red value**</span></span>|<span data-ttu-id="a8973-133">**Valeur vert**</span><span class="sxs-lookup"><span data-stu-id="a8973-133">**Green value**</span></span>|<span data-ttu-id="a8973-134">**Valeur bleue**</span><span class="sxs-lookup"><span data-stu-id="a8973-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8973-135">Noir</span><span class="sxs-lookup"><span data-stu-id="a8973-135">Black</span></span>  <br/> |<span data-ttu-id="a8973-136">0</span><span class="sxs-lookup"><span data-stu-id="a8973-136">0</span></span>  <br/> |<span data-ttu-id="a8973-137">0</span><span class="sxs-lookup"><span data-stu-id="a8973-137">0</span></span>  <br/> |<span data-ttu-id="a8973-138">0</span><span class="sxs-lookup"><span data-stu-id="a8973-138">0</span></span>  <br/> |
|<span data-ttu-id="a8973-139">Bleu</span><span class="sxs-lookup"><span data-stu-id="a8973-139">Blue</span></span>  <br/> |<span data-ttu-id="a8973-140">0</span><span class="sxs-lookup"><span data-stu-id="a8973-140">0</span></span>  <br/> |<span data-ttu-id="a8973-141">0</span><span class="sxs-lookup"><span data-stu-id="a8973-141">0</span></span>  <br/> |<span data-ttu-id="a8973-142">255</span><span class="sxs-lookup"><span data-stu-id="a8973-142">255</span></span>  <br/> |
|<span data-ttu-id="a8973-143">Vert</span><span class="sxs-lookup"><span data-stu-id="a8973-143">Green</span></span>  <br/> |<span data-ttu-id="a8973-144">0</span><span class="sxs-lookup"><span data-stu-id="a8973-144">0</span></span>  <br/> |<span data-ttu-id="a8973-145">255</span><span class="sxs-lookup"><span data-stu-id="a8973-145">255</span></span>  <br/> |<span data-ttu-id="a8973-146">0</span><span class="sxs-lookup"><span data-stu-id="a8973-146">0</span></span>  <br/> |
|<span data-ttu-id="a8973-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="a8973-147">Cyan</span></span>  <br/> |<span data-ttu-id="a8973-148">0</span><span class="sxs-lookup"><span data-stu-id="a8973-148">0</span></span>  <br/> |<span data-ttu-id="a8973-149">255</span><span class="sxs-lookup"><span data-stu-id="a8973-149">255</span></span>  <br/> |<span data-ttu-id="a8973-150">255</span><span class="sxs-lookup"><span data-stu-id="a8973-150">255</span></span>  <br/> |
|<span data-ttu-id="a8973-151">Rouge</span><span class="sxs-lookup"><span data-stu-id="a8973-151">Red</span></span>  <br/> |<span data-ttu-id="a8973-152">255</span><span class="sxs-lookup"><span data-stu-id="a8973-152">255</span></span>  <br/> |<span data-ttu-id="a8973-153">0</span><span class="sxs-lookup"><span data-stu-id="a8973-153">0</span></span>  <br/> |<span data-ttu-id="a8973-154">0</span><span class="sxs-lookup"><span data-stu-id="a8973-154">0</span></span>  <br/> |
|<span data-ttu-id="a8973-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="a8973-155">Magenta</span></span>  <br/> |<span data-ttu-id="a8973-156">255</span><span class="sxs-lookup"><span data-stu-id="a8973-156">255</span></span>  <br/> |<span data-ttu-id="a8973-157">0</span><span class="sxs-lookup"><span data-stu-id="a8973-157">0</span></span>  <br/> |<span data-ttu-id="a8973-158">255</span><span class="sxs-lookup"><span data-stu-id="a8973-158">255</span></span>  <br/> |
|<span data-ttu-id="a8973-159">Jaune</span><span class="sxs-lookup"><span data-stu-id="a8973-159">Yellow</span></span>  <br/> |<span data-ttu-id="a8973-160">255</span><span class="sxs-lookup"><span data-stu-id="a8973-160">255</span></span>  <br/> |<span data-ttu-id="a8973-161">255</span><span class="sxs-lookup"><span data-stu-id="a8973-161">255</span></span>  <br/> |<span data-ttu-id="a8973-162">0</span><span class="sxs-lookup"><span data-stu-id="a8973-162">0</span></span>  <br/> |
|<span data-ttu-id="a8973-163">Blanc</span><span class="sxs-lookup"><span data-stu-id="a8973-163">White</span></span>  <br/> |<span data-ttu-id="a8973-164">255</span><span class="sxs-lookup"><span data-stu-id="a8973-164">255</span></span>  <br/> |<span data-ttu-id="a8973-165">255</span><span class="sxs-lookup"><span data-stu-id="a8973-165">255</span></span>  <br/> |<span data-ttu-id="a8973-166">255</span><span class="sxs-lookup"><span data-stu-id="a8973-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="a8973-167">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a8973-167">Example 1</span></span>

<span data-ttu-id="a8973-168">RVB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="a8973-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="a8973-169">Renvoie l’index associé à la couleur bleue.</span><span class="sxs-lookup"><span data-stu-id="a8973-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a8973-170">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a8973-170">Example 2</span></span>

<span data-ttu-id="a8973-171">RVB (rouge (feuille. 1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="a8973-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="a8973-172">Renvoie l’index d’une couleur dont la composante rouge correspond au premier plan du remplissage de Feuille.1.</span><span class="sxs-lookup"><span data-stu-id="a8973-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

