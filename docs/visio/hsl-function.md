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
description: Renvoie une valeur représentant un index dans la palette de couleurs du document. Il spécifie une couleur par ses composants teinte, saturation et luminosité.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420961"
---
# <a name="hsl-function"></a><span data-ttu-id="5f103-104">Fonction HSL</span><span class="sxs-lookup"><span data-stu-id="5f103-104">HSL Function</span></span>

<span data-ttu-id="5f103-105">Renvoie une valeur représentant un index dans la palette de couleurs du document.</span><span class="sxs-lookup"><span data-stu-id="5f103-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="5f103-106">Il spécifie une couleur par ses composants teinte, saturation et luminosité.</span><span class="sxs-lookup"><span data-stu-id="5f103-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5f103-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5f103-107">Syntax</span></span>

<span data-ttu-id="5f103-108">TSL (\* \* *teinte* \* \*, \* \* *saturation* \* \*, \* \* *luminosité* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5f103-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5f103-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5f103-109">Parameters</span></span>

|<span data-ttu-id="5f103-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5f103-110">**Name**</span></span>|<span data-ttu-id="5f103-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="5f103-111">**Required/Optional**</span></span>|<span data-ttu-id="5f103-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="5f103-112">**Data Type**</span></span>|<span data-ttu-id="5f103-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="5f103-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5f103-114">_couleurs_</span><span class="sxs-lookup"><span data-stu-id="5f103-114">_hue_</span></span> <br/> |<span data-ttu-id="5f103-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5f103-115">Required</span></span>  <br/> |<span data-ttu-id="5f103-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="5f103-116">**Number**</span></span> <br/> |<span data-ttu-id="5f103-117">Teinte de la couleur, exprimée par une valeur de 0 à 239 inclus, ou par une expression ayant cette valeur pour résultat.</span><span class="sxs-lookup"><span data-stu-id="5f103-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="5f103-118">_curseur_</span><span class="sxs-lookup"><span data-stu-id="5f103-118">_saturation_</span></span> <br/> |<span data-ttu-id="5f103-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5f103-119">Required</span></span>  <br/> |<span data-ttu-id="5f103-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="5f103-120">**Number**</span></span> <br/> |<span data-ttu-id="5f103-121">Saturation de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.</span><span class="sxs-lookup"><span data-stu-id="5f103-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="5f103-122">_luminosité_</span><span class="sxs-lookup"><span data-stu-id="5f103-122">_luminosity_</span></span> <br/> |<span data-ttu-id="5f103-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5f103-123">Required</span></span>  <br/> |<span data-ttu-id="5f103-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="5f103-124">**Number**</span></span> <br/> | <span data-ttu-id="5f103-125">Luminosité de la couleur, exprimée par une valeur de 0 à 240 inclus, ou par une expression ayant cette valeur pour résultat.</span><span class="sxs-lookup"><span data-stu-id="5f103-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5f103-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5f103-126">Return value</span></span>

<span data-ttu-id="5f103-127">Nombre</span><span class="sxs-lookup"><span data-stu-id="5f103-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5f103-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="5f103-128">Remarks</span></span>

<span data-ttu-id="5f103-129">Si la couleur renvoyée par la fonction n’existe pas dans la palette de couleurs du document actif, elle est ajoutée dans la liste des couleurs associée au document.</span><span class="sxs-lookup"><span data-stu-id="5f103-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="5f103-130">Le tableau suivant répertorie les couleurs standard ainsi que la teinte, la saturation et la luminosité qui leur sont associées.</span><span class="sxs-lookup"><span data-stu-id="5f103-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="5f103-131">**Couleur**</span><span class="sxs-lookup"><span data-stu-id="5f103-131">**Color**</span></span>|<span data-ttu-id="5f103-132">**Teinte**</span><span class="sxs-lookup"><span data-stu-id="5f103-132">**Hue value**</span></span>|<span data-ttu-id="5f103-133">**Saturation**</span><span class="sxs-lookup"><span data-stu-id="5f103-133">**Saturation value**</span></span>|<span data-ttu-id="5f103-134">**Luminosité**</span><span class="sxs-lookup"><span data-stu-id="5f103-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="5f103-135">Noir</span><span class="sxs-lookup"><span data-stu-id="5f103-135">Black</span></span>  <br/> |<span data-ttu-id="5f103-136">0</span><span class="sxs-lookup"><span data-stu-id="5f103-136">0</span></span>  <br/> |<span data-ttu-id="5f103-137">0</span><span class="sxs-lookup"><span data-stu-id="5f103-137">0</span></span>  <br/> |<span data-ttu-id="5f103-138">heures/24</span><span class="sxs-lookup"><span data-stu-id="5f103-138">24</span></span>  <br/> |
|<span data-ttu-id="5f103-139">Bleu</span><span class="sxs-lookup"><span data-stu-id="5f103-139">Blue</span></span>  <br/> |<span data-ttu-id="5f103-140">160</span><span class="sxs-lookup"><span data-stu-id="5f103-140">160</span></span>  <br/> |<span data-ttu-id="5f103-141">240</span><span class="sxs-lookup"><span data-stu-id="5f103-141">240</span></span>  <br/> |<span data-ttu-id="5f103-142">120</span><span class="sxs-lookup"><span data-stu-id="5f103-142">120</span></span>  <br/> |
|<span data-ttu-id="5f103-143">Vert</span><span class="sxs-lookup"><span data-stu-id="5f103-143">Green</span></span>  <br/> |<span data-ttu-id="5f103-144">80</span><span class="sxs-lookup"><span data-stu-id="5f103-144">80</span></span>  <br/> |<span data-ttu-id="5f103-145">240</span><span class="sxs-lookup"><span data-stu-id="5f103-145">240</span></span>  <br/> |<span data-ttu-id="5f103-146">120</span><span class="sxs-lookup"><span data-stu-id="5f103-146">120</span></span>  <br/> |
|<span data-ttu-id="5f103-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="5f103-147">Cyan</span></span>  <br/> |<span data-ttu-id="5f103-148">120</span><span class="sxs-lookup"><span data-stu-id="5f103-148">120</span></span>  <br/> |<span data-ttu-id="5f103-149">240</span><span class="sxs-lookup"><span data-stu-id="5f103-149">240</span></span>  <br/> |<span data-ttu-id="5f103-150">120</span><span class="sxs-lookup"><span data-stu-id="5f103-150">120</span></span>  <br/> |
|<span data-ttu-id="5f103-151">Rouge</span><span class="sxs-lookup"><span data-stu-id="5f103-151">Red</span></span>  <br/> |<span data-ttu-id="5f103-152">0</span><span class="sxs-lookup"><span data-stu-id="5f103-152">0</span></span>  <br/> |<span data-ttu-id="5f103-153">240</span><span class="sxs-lookup"><span data-stu-id="5f103-153">240</span></span>  <br/> |<span data-ttu-id="5f103-154">120</span><span class="sxs-lookup"><span data-stu-id="5f103-154">120</span></span>  <br/> |
|<span data-ttu-id="5f103-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="5f103-155">Magenta</span></span>  <br/> |<span data-ttu-id="5f103-156">200</span><span class="sxs-lookup"><span data-stu-id="5f103-156">200</span></span>  <br/> |<span data-ttu-id="5f103-157">240</span><span class="sxs-lookup"><span data-stu-id="5f103-157">240</span></span>  <br/> |<span data-ttu-id="5f103-158">120</span><span class="sxs-lookup"><span data-stu-id="5f103-158">120</span></span>  <br/> |
|<span data-ttu-id="5f103-159">Jaune</span><span class="sxs-lookup"><span data-stu-id="5f103-159">Yellow</span></span>  <br/> |<span data-ttu-id="5f103-160">40</span><span class="sxs-lookup"><span data-stu-id="5f103-160">40</span></span>  <br/> |<span data-ttu-id="5f103-161">240</span><span class="sxs-lookup"><span data-stu-id="5f103-161">240</span></span>  <br/> |<span data-ttu-id="5f103-162">120</span><span class="sxs-lookup"><span data-stu-id="5f103-162">120</span></span>  <br/> |
|<span data-ttu-id="5f103-163">Blanc</span><span class="sxs-lookup"><span data-stu-id="5f103-163">White</span></span>  <br/> |<span data-ttu-id="5f103-164">0</span><span class="sxs-lookup"><span data-stu-id="5f103-164">0</span></span>  <br/> |<span data-ttu-id="5f103-165">0</span><span class="sxs-lookup"><span data-stu-id="5f103-165">0</span></span>  <br/> |<span data-ttu-id="5f103-166">240</span><span class="sxs-lookup"><span data-stu-id="5f103-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="5f103-167">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="5f103-167">Example 1</span></span>

<span data-ttu-id="5f103-168">TSL (160240120)</span><span class="sxs-lookup"><span data-stu-id="5f103-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="5f103-169">Renvoie l’index associé à la couleur bleue.</span><span class="sxs-lookup"><span data-stu-id="5f103-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="5f103-170">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="5f103-170">Example 2</span></span>

<span data-ttu-id="5f103-171">TSL (TEINTe (FillForegnd), SAT (FillForegnd), MIN (LUM (FillForegnd) + 100240))</span><span class="sxs-lookup"><span data-stu-id="5f103-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="5f103-172">Renvoie l’index de la couleur de remplissage de premier plan en augmentant la luminosité.</span><span class="sxs-lookup"><span data-stu-id="5f103-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

