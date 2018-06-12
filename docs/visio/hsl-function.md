---
title: HSL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Renvoie une valeur représentant un index dans la palette de couleurs. Il spécifie une couleur en sa teinte, la saturation et composants de luminosité.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788789"
---
# <a name="hsl-function"></a><span data-ttu-id="d8e21-104">HSL, fonction</span><span class="sxs-lookup"><span data-stu-id="d8e21-104">HSL Function</span></span>

<span data-ttu-id="d8e21-105">Renvoie une valeur représentant un index dans la palette de couleurs.</span><span class="sxs-lookup"><span data-stu-id="d8e21-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="d8e21-106">Il spécifie une couleur en sa teinte, la saturation et composants de luminosité.</span><span class="sxs-lookup"><span data-stu-id="d8e21-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d8e21-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d8e21-107">Syntax</span></span>

<span data-ttu-id="d8e21-108">TSL (** *teinte* **, ** *saturation* **, ** *luminosité* **)</span><span class="sxs-lookup"><span data-stu-id="d8e21-108">HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d8e21-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d8e21-109">Parameters</span></span>

|<span data-ttu-id="d8e21-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d8e21-110">**Name**</span></span>|<span data-ttu-id="d8e21-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="d8e21-111">**Required/Optional**</span></span>|<span data-ttu-id="d8e21-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="d8e21-112">**Data Type**</span></span>|<span data-ttu-id="d8e21-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="d8e21-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d8e21-114">_teinte_</span><span class="sxs-lookup"><span data-stu-id="d8e21-114">_hue_</span></span> <br/> |<span data-ttu-id="d8e21-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d8e21-115">Required</span></span>  <br/> |<span data-ttu-id="d8e21-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="d8e21-116">**Number**</span></span> <br/> |<span data-ttu-id="d8e21-117">Teinte de la couleur, exprimée par une valeur de 0 à 239 inclus, ou par une expression ayant cette valeur pour résultat.</span><span class="sxs-lookup"><span data-stu-id="d8e21-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="d8e21-118">_saturation_</span><span class="sxs-lookup"><span data-stu-id="d8e21-118">_saturation_</span></span> <br/> |<span data-ttu-id="d8e21-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d8e21-119">Required</span></span>  <br/> |<span data-ttu-id="d8e21-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="d8e21-120">**Number**</span></span> <br/> |<span data-ttu-id="d8e21-121">Saturation de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.</span><span class="sxs-lookup"><span data-stu-id="d8e21-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="d8e21-122">_luminosité_</span><span class="sxs-lookup"><span data-stu-id="d8e21-122">_luminosity_</span></span> <br/> |<span data-ttu-id="d8e21-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="d8e21-123">Required</span></span>  <br/> |<span data-ttu-id="d8e21-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="d8e21-124">**Number**</span></span> <br/> | <span data-ttu-id="d8e21-125">Luminosité de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.</span><span class="sxs-lookup"><span data-stu-id="d8e21-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d8e21-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="d8e21-126">Return value</span></span>

<span data-ttu-id="d8e21-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="d8e21-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8e21-128">Note</span><span class="sxs-lookup"><span data-stu-id="d8e21-128">Remarks</span></span>

<span data-ttu-id="d8e21-129">Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs du document actif, elle est ajoutée dans la liste des couleurs associée au document.</span><span class="sxs-lookup"><span data-stu-id="d8e21-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="d8e21-130">Le tableau suivant répertorie les couleurs standard ainsi que la teinte, la saturation et la luminosité qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="d8e21-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="d8e21-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="d8e21-131">**Color**</span></span>|<span data-ttu-id="d8e21-132">**Teinte**</span><span class="sxs-lookup"><span data-stu-id="d8e21-132">**Hue value**</span></span>|<span data-ttu-id="d8e21-133">**Valeur de la saturation**</span><span class="sxs-lookup"><span data-stu-id="d8e21-133">**Saturation value**</span></span>|<span data-ttu-id="d8e21-134">**Luminosité**</span><span class="sxs-lookup"><span data-stu-id="d8e21-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d8e21-135">Noir</span><span class="sxs-lookup"><span data-stu-id="d8e21-135">Black</span></span>  <br/> |<span data-ttu-id="d8e21-136">0</span><span class="sxs-lookup"><span data-stu-id="d8e21-136">0</span></span>  <br/> |<span data-ttu-id="d8e21-137">0</span><span class="sxs-lookup"><span data-stu-id="d8e21-137">0</span></span>  <br/> |<span data-ttu-id="d8e21-138">24</span><span class="sxs-lookup"><span data-stu-id="d8e21-138">24</span></span>  <br/> |
|<span data-ttu-id="d8e21-139">Bleu</span><span class="sxs-lookup"><span data-stu-id="d8e21-139">Blue</span></span>  <br/> |<span data-ttu-id="d8e21-140">160</span><span class="sxs-lookup"><span data-stu-id="d8e21-140">160</span></span>  <br/> |<span data-ttu-id="d8e21-141">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-141">240</span></span>  <br/> |<span data-ttu-id="d8e21-142">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-142">120</span></span>  <br/> |
|<span data-ttu-id="d8e21-143">Vert</span><span class="sxs-lookup"><span data-stu-id="d8e21-143">Green</span></span>  <br/> |<span data-ttu-id="d8e21-144">80</span><span class="sxs-lookup"><span data-stu-id="d8e21-144">80</span></span>  <br/> |<span data-ttu-id="d8e21-145">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-145">240</span></span>  <br/> |<span data-ttu-id="d8e21-146">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-146">120</span></span>  <br/> |
|<span data-ttu-id="d8e21-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="d8e21-147">Cyan</span></span>  <br/> |<span data-ttu-id="d8e21-148">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-148">120</span></span>  <br/> |<span data-ttu-id="d8e21-149">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-149">240</span></span>  <br/> |<span data-ttu-id="d8e21-150">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-150">120</span></span>  <br/> |
|<span data-ttu-id="d8e21-151">Rouge</span><span class="sxs-lookup"><span data-stu-id="d8e21-151">Red</span></span>  <br/> |<span data-ttu-id="d8e21-152">0</span><span class="sxs-lookup"><span data-stu-id="d8e21-152">0</span></span>  <br/> |<span data-ttu-id="d8e21-153">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-153">240</span></span>  <br/> |<span data-ttu-id="d8e21-154">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-154">120</span></span>  <br/> |
|<span data-ttu-id="d8e21-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="d8e21-155">Magenta</span></span>  <br/> |<span data-ttu-id="d8e21-156">200</span><span class="sxs-lookup"><span data-stu-id="d8e21-156">200</span></span>  <br/> |<span data-ttu-id="d8e21-157">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-157">240</span></span>  <br/> |<span data-ttu-id="d8e21-158">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-158">120</span></span>  <br/> |
|<span data-ttu-id="d8e21-159">Jaune</span><span class="sxs-lookup"><span data-stu-id="d8e21-159">Yellow</span></span>  <br/> |<span data-ttu-id="d8e21-160">40</span><span class="sxs-lookup"><span data-stu-id="d8e21-160">40</span></span>  <br/> |<span data-ttu-id="d8e21-161">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-161">240</span></span>  <br/> |<span data-ttu-id="d8e21-162">120</span><span class="sxs-lookup"><span data-stu-id="d8e21-162">120</span></span>  <br/> |
|<span data-ttu-id="d8e21-163">Blanc</span><span class="sxs-lookup"><span data-stu-id="d8e21-163">White</span></span>  <br/> |<span data-ttu-id="d8e21-164">0</span><span class="sxs-lookup"><span data-stu-id="d8e21-164">0</span></span>  <br/> |<span data-ttu-id="d8e21-165">0</span><span class="sxs-lookup"><span data-stu-id="d8e21-165">0</span></span>  <br/> |<span data-ttu-id="d8e21-166">240</span><span class="sxs-lookup"><span data-stu-id="d8e21-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="d8e21-167">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="d8e21-167">Example 1</span></span>

<span data-ttu-id="d8e21-168">HSL(160,240,120)</span><span class="sxs-lookup"><span data-stu-id="d8e21-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="d8e21-169">Renvoie l’index associé à la couleur bleue.</span><span class="sxs-lookup"><span data-stu-id="d8e21-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d8e21-170">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="d8e21-170">Example 2</span></span>

<span data-ttu-id="d8e21-171">HSL(Hue(FillForegnd),SAT(FillForegnd),min(Lum(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="d8e21-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="d8e21-172">Renvoie l’index de la couleur de remplissage de premier plan en augmentant la luminosité.</span><span class="sxs-lookup"><span data-stu-id="d8e21-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

