---
title: Fonction RGB (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Renvoie une valeur représentant un index dans la palette de couleurs. Il spécifie une couleur en ses composants rouges, verts et bleus, chacune étant un nombre compris entre 0 et 255, inclus, ou une expression qui renvoie un nombre.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789479"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="24638-104">Fonction RGB (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="24638-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="24638-105">Renvoie une valeur représentant un index dans la palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="24638-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="24638-106">Il spécifie une couleur en ses composants rouges, verts et bleus, chacune étant un nombre compris entre 0 et 255, inclus, ou une expression qui renvoie un nombre.</span><span class="sxs-lookup"><span data-stu-id="24638-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="24638-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="24638-107">Syntax</span></span>

<span data-ttu-id="24638-108">RVB (** *rouge* **, ** *vert* **, ** *bleu* **)</span><span class="sxs-lookup"><span data-stu-id="24638-108">RGB(** *red* **, ** *green* **, ** *blue* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="24638-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="24638-109">Parameters</span></span>

|<span data-ttu-id="24638-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="24638-110">**Name**</span></span>|<span data-ttu-id="24638-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="24638-111">**Required/Optional**</span></span>|<span data-ttu-id="24638-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="24638-112">**Data Type**</span></span>|<span data-ttu-id="24638-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="24638-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="24638-114">_rouge_</span><span class="sxs-lookup"><span data-stu-id="24638-114">_red_</span></span> <br/> |<span data-ttu-id="24638-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="24638-115">Required</span></span>  <br/> |<span data-ttu-id="24638-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="24638-116">**Number**</span></span> <br/> |<span data-ttu-id="24638-117">Composante rouge</span><span class="sxs-lookup"><span data-stu-id="24638-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="24638-118">_vert_</span><span class="sxs-lookup"><span data-stu-id="24638-118">_green_</span></span> <br/> |<span data-ttu-id="24638-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="24638-119">Required</span></span>  <br/> |<span data-ttu-id="24638-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="24638-120">**Number**</span></span> <br/> |<span data-ttu-id="24638-121">Composante vert</span><span class="sxs-lookup"><span data-stu-id="24638-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="24638-122">_bleu_</span><span class="sxs-lookup"><span data-stu-id="24638-122">_blue_</span></span> <br/> |<span data-ttu-id="24638-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="24638-123">Required</span></span>  <br/> |<span data-ttu-id="24638-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="24638-124">**Nmber**</span></span> <br/> |<span data-ttu-id="24638-125">Composante bleu</span><span class="sxs-lookup"><span data-stu-id="24638-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="24638-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="24638-126">Return value</span></span>

<span data-ttu-id="24638-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="24638-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="24638-128">Note</span><span class="sxs-lookup"><span data-stu-id="24638-128">Remarks</span></span>

<span data-ttu-id="24638-129">Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs actuelle, elle est automatiquement ajoutée.</span><span class="sxs-lookup"><span data-stu-id="24638-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="24638-130">Le tableau ci-après présente les couleurs standard et les valeurs Rouge, Vert et Bleu qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="24638-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="24638-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="24638-131">**Color**</span></span>|<span data-ttu-id="24638-132">**Valeur rouge**</span><span class="sxs-lookup"><span data-stu-id="24638-132">**Red value**</span></span>|<span data-ttu-id="24638-133">**Valeur vert**</span><span class="sxs-lookup"><span data-stu-id="24638-133">**Green value**</span></span>|<span data-ttu-id="24638-134">**Valeur bleu**</span><span class="sxs-lookup"><span data-stu-id="24638-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="24638-135">Noir</span><span class="sxs-lookup"><span data-stu-id="24638-135">Black</span></span>  <br/> |<span data-ttu-id="24638-136">0</span><span class="sxs-lookup"><span data-stu-id="24638-136">0</span></span>  <br/> |<span data-ttu-id="24638-137">0</span><span class="sxs-lookup"><span data-stu-id="24638-137">0</span></span>  <br/> |<span data-ttu-id="24638-138">0</span><span class="sxs-lookup"><span data-stu-id="24638-138">0</span></span>  <br/> |
|<span data-ttu-id="24638-139">Bleu</span><span class="sxs-lookup"><span data-stu-id="24638-139">Blue</span></span>  <br/> |<span data-ttu-id="24638-140">0</span><span class="sxs-lookup"><span data-stu-id="24638-140">0</span></span>  <br/> |<span data-ttu-id="24638-141">0</span><span class="sxs-lookup"><span data-stu-id="24638-141">0</span></span>  <br/> |<span data-ttu-id="24638-142">255</span><span class="sxs-lookup"><span data-stu-id="24638-142">255</span></span>  <br/> |
|<span data-ttu-id="24638-143">Vert</span><span class="sxs-lookup"><span data-stu-id="24638-143">Green</span></span>  <br/> |<span data-ttu-id="24638-144">0</span><span class="sxs-lookup"><span data-stu-id="24638-144">0</span></span>  <br/> |<span data-ttu-id="24638-145">255</span><span class="sxs-lookup"><span data-stu-id="24638-145">255</span></span>  <br/> |<span data-ttu-id="24638-146">0</span><span class="sxs-lookup"><span data-stu-id="24638-146">0</span></span>  <br/> |
|<span data-ttu-id="24638-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="24638-147">Cyan</span></span>  <br/> |<span data-ttu-id="24638-148">0</span><span class="sxs-lookup"><span data-stu-id="24638-148">0</span></span>  <br/> |<span data-ttu-id="24638-149">255</span><span class="sxs-lookup"><span data-stu-id="24638-149">255</span></span>  <br/> |<span data-ttu-id="24638-150">255</span><span class="sxs-lookup"><span data-stu-id="24638-150">255</span></span>  <br/> |
|<span data-ttu-id="24638-151">Rouge</span><span class="sxs-lookup"><span data-stu-id="24638-151">Red</span></span>  <br/> |<span data-ttu-id="24638-152">255</span><span class="sxs-lookup"><span data-stu-id="24638-152">255</span></span>  <br/> |<span data-ttu-id="24638-153">0</span><span class="sxs-lookup"><span data-stu-id="24638-153">0</span></span>  <br/> |<span data-ttu-id="24638-154">0</span><span class="sxs-lookup"><span data-stu-id="24638-154">0</span></span>  <br/> |
|<span data-ttu-id="24638-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="24638-155">Magenta</span></span>  <br/> |<span data-ttu-id="24638-156">255</span><span class="sxs-lookup"><span data-stu-id="24638-156">255</span></span>  <br/> |<span data-ttu-id="24638-157">0</span><span class="sxs-lookup"><span data-stu-id="24638-157">0</span></span>  <br/> |<span data-ttu-id="24638-158">255</span><span class="sxs-lookup"><span data-stu-id="24638-158">255</span></span>  <br/> |
|<span data-ttu-id="24638-159">Jaune</span><span class="sxs-lookup"><span data-stu-id="24638-159">Yellow</span></span>  <br/> |<span data-ttu-id="24638-160">255</span><span class="sxs-lookup"><span data-stu-id="24638-160">255</span></span>  <br/> |<span data-ttu-id="24638-161">255</span><span class="sxs-lookup"><span data-stu-id="24638-161">255</span></span>  <br/> |<span data-ttu-id="24638-162">0</span><span class="sxs-lookup"><span data-stu-id="24638-162">0</span></span>  <br/> |
|<span data-ttu-id="24638-163">Blanc</span><span class="sxs-lookup"><span data-stu-id="24638-163">White</span></span>  <br/> |<span data-ttu-id="24638-164">255</span><span class="sxs-lookup"><span data-stu-id="24638-164">255</span></span>  <br/> |<span data-ttu-id="24638-165">255</span><span class="sxs-lookup"><span data-stu-id="24638-165">255</span></span>  <br/> |<span data-ttu-id="24638-166">255</span><span class="sxs-lookup"><span data-stu-id="24638-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="24638-167">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="24638-167">Example 1</span></span>

<span data-ttu-id="24638-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="24638-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="24638-169">Renvoie l’index associé à la couleur bleue.</span><span class="sxs-lookup"><span data-stu-id="24638-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="24638-170">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="24638-170">Example 2</span></span>

<span data-ttu-id="24638-171">RVB (rouge (Sheet.1 ! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="24638-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="24638-172">Renvoie l’index d’une couleur dont la composante rouge correspond au premier plan du remplissage de Feuille.1.</span><span class="sxs-lookup"><span data-stu-id="24638-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

