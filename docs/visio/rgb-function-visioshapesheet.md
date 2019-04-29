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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426302"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="e2d87-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e2d87-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e2d87-105">Renvoie une valeur représentant un index dans la palette de couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="e2d87-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="e2d87-106">Il spécifie une couleur par ses composants rouge, vert et bleu, où chacun est un nombre compris entre 0 et 255 inclus, ou une expression qui renvoie à ce nombre.</span><span class="sxs-lookup"><span data-stu-id="e2d87-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e2d87-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2d87-107">Syntax</span></span>

<span data-ttu-id="e2d87-108">RVB (\* \* *rouge* \* \*, \* \* *vert* \* \*, \* \* *bleu* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e2d87-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e2d87-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2d87-109">Parameters</span></span>

|<span data-ttu-id="e2d87-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e2d87-110">**Name**</span></span>|<span data-ttu-id="e2d87-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e2d87-111">**Required/Optional**</span></span>|<span data-ttu-id="e2d87-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e2d87-112">**Data Type**</span></span>|<span data-ttu-id="e2d87-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="e2d87-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e2d87-114">_b_</span><span class="sxs-lookup"><span data-stu-id="e2d87-114">_red_</span></span> <br/> |<span data-ttu-id="e2d87-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2d87-115">Required</span></span>  <br/> |<span data-ttu-id="e2d87-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="e2d87-116">**Number**</span></span> <br/> |<span data-ttu-id="e2d87-117">Composante rouge</span><span class="sxs-lookup"><span data-stu-id="e2d87-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="e2d87-118">_informatique_</span><span class="sxs-lookup"><span data-stu-id="e2d87-118">_green_</span></span> <br/> |<span data-ttu-id="e2d87-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2d87-119">Required</span></span>  <br/> |<span data-ttu-id="e2d87-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="e2d87-120">**Number**</span></span> <br/> |<span data-ttu-id="e2d87-121">Composante vert</span><span class="sxs-lookup"><span data-stu-id="e2d87-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="e2d87-122">_Blue_</span><span class="sxs-lookup"><span data-stu-id="e2d87-122">_blue_</span></span> <br/> |<span data-ttu-id="e2d87-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e2d87-123">Required</span></span>  <br/> |<span data-ttu-id="e2d87-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="e2d87-124">**Nmber**</span></span> <br/> |<span data-ttu-id="e2d87-125">Composante bleu</span><span class="sxs-lookup"><span data-stu-id="e2d87-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e2d87-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e2d87-126">Return value</span></span>

<span data-ttu-id="e2d87-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="e2d87-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2d87-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="e2d87-128">Remarks</span></span>

<span data-ttu-id="e2d87-129">Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs actuelle, elle est automatiquement ajoutée.</span><span class="sxs-lookup"><span data-stu-id="e2d87-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="e2d87-130">Le tableau ci-après présente les couleurs standard et les valeurs Rouge, Vert et Bleu qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="e2d87-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="e2d87-131">**Couleur**</span><span class="sxs-lookup"><span data-stu-id="e2d87-131">**Color**</span></span>|<span data-ttu-id="e2d87-132">**Valeur rouge**</span><span class="sxs-lookup"><span data-stu-id="e2d87-132">**Red value**</span></span>|<span data-ttu-id="e2d87-133">**Valeur vert**</span><span class="sxs-lookup"><span data-stu-id="e2d87-133">**Green value**</span></span>|<span data-ttu-id="e2d87-134">**Valeur bleue**</span><span class="sxs-lookup"><span data-stu-id="e2d87-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e2d87-135">Noir</span><span class="sxs-lookup"><span data-stu-id="e2d87-135">Black</span></span>  <br/> |<span data-ttu-id="e2d87-136">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-136">0</span></span>  <br/> |<span data-ttu-id="e2d87-137">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-137">0</span></span>  <br/> |<span data-ttu-id="e2d87-138">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-138">0</span></span>  <br/> |
|<span data-ttu-id="e2d87-139">Bleu</span><span class="sxs-lookup"><span data-stu-id="e2d87-139">Blue</span></span>  <br/> |<span data-ttu-id="e2d87-140">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-140">0</span></span>  <br/> |<span data-ttu-id="e2d87-141">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-141">0</span></span>  <br/> |<span data-ttu-id="e2d87-142">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-142">255</span></span>  <br/> |
|<span data-ttu-id="e2d87-143">Vert</span><span class="sxs-lookup"><span data-stu-id="e2d87-143">Green</span></span>  <br/> |<span data-ttu-id="e2d87-144">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-144">0</span></span>  <br/> |<span data-ttu-id="e2d87-145">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-145">255</span></span>  <br/> |<span data-ttu-id="e2d87-146">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-146">0</span></span>  <br/> |
|<span data-ttu-id="e2d87-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="e2d87-147">Cyan</span></span>  <br/> |<span data-ttu-id="e2d87-148">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-148">0</span></span>  <br/> |<span data-ttu-id="e2d87-149">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-149">255</span></span>  <br/> |<span data-ttu-id="e2d87-150">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-150">255</span></span>  <br/> |
|<span data-ttu-id="e2d87-151">Rouge</span><span class="sxs-lookup"><span data-stu-id="e2d87-151">Red</span></span>  <br/> |<span data-ttu-id="e2d87-152">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-152">255</span></span>  <br/> |<span data-ttu-id="e2d87-153">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-153">0</span></span>  <br/> |<span data-ttu-id="e2d87-154">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-154">0</span></span>  <br/> |
|<span data-ttu-id="e2d87-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="e2d87-155">Magenta</span></span>  <br/> |<span data-ttu-id="e2d87-156">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-156">255</span></span>  <br/> |<span data-ttu-id="e2d87-157">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-157">0</span></span>  <br/> |<span data-ttu-id="e2d87-158">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-158">255</span></span>  <br/> |
|<span data-ttu-id="e2d87-159">Jaune</span><span class="sxs-lookup"><span data-stu-id="e2d87-159">Yellow</span></span>  <br/> |<span data-ttu-id="e2d87-160">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-160">255</span></span>  <br/> |<span data-ttu-id="e2d87-161">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-161">255</span></span>  <br/> |<span data-ttu-id="e2d87-162">0</span><span class="sxs-lookup"><span data-stu-id="e2d87-162">0</span></span>  <br/> |
|<span data-ttu-id="e2d87-163">Blanc</span><span class="sxs-lookup"><span data-stu-id="e2d87-163">White</span></span>  <br/> |<span data-ttu-id="e2d87-164">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-164">255</span></span>  <br/> |<span data-ttu-id="e2d87-165">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-165">255</span></span>  <br/> |<span data-ttu-id="e2d87-166">255</span><span class="sxs-lookup"><span data-stu-id="e2d87-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="e2d87-167">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e2d87-167">Example 1</span></span>

<span data-ttu-id="e2d87-168">RVB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="e2d87-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="e2d87-169">Renvoie l’index associé à la couleur bleue.</span><span class="sxs-lookup"><span data-stu-id="e2d87-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e2d87-170">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e2d87-170">Example 2</span></span>

<span data-ttu-id="e2d87-171">RVB (rouge (feuille. 1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="e2d87-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="e2d87-172">Renvoie l’index d’une couleur dont la composante rouge correspond au premier plan du remplissage de Feuille.1.</span><span class="sxs-lookup"><span data-stu-id="e2d87-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

