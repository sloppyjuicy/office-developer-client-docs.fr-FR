---
title: ISERRNA, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251451
localization_priority: Normal
ms.assetid: 6ee7dc3d-efe9-c862-f71d-034b3d9c3ec6
description: 'Renvoie TRUE si la valeur de cellreference est de type erreur #N/A! (non disponible) ; Sinon, elle renvoie FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: 8a398eca6da659a6b8f29e4ef8e31b18abf56fde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432113"
---
# <a name="iserrna-function"></a><span data-ttu-id="1ac74-105">Fonction ISERRNA</span><span class="sxs-lookup"><span data-stu-id="1ac74-105">ISERRNA Function</span></span>

<span data-ttu-id="1ac74-106">Renvoie TRUE si la valeur de  _cellreference_ est de type erreur #N/A!</span><span class="sxs-lookup"><span data-stu-id="1ac74-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="1ac74-107">(non disponible) ; Sinon, elle renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="1ac74-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="1ac74-108">La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="1ac74-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1ac74-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ac74-109">Syntax</span></span>

<span data-ttu-id="1ac74-110">ISERRNA(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="1ac74-110">ISERRNA(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1ac74-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ac74-111">Parameters</span></span>

|<span data-ttu-id="1ac74-112">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1ac74-112">**Name**</span></span>|<span data-ttu-id="1ac74-113">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1ac74-113">**Required/Optional**</span></span>|<span data-ttu-id="1ac74-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1ac74-114">**Data Type**</span></span>|<span data-ttu-id="1ac74-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="1ac74-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1ac74-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="1ac74-116">_cellreference_</span></span> <br/> |<span data-ttu-id="1ac74-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1ac74-117">Required</span></span>  <br/> |<span data-ttu-id="1ac74-118">**String**</span><span class="sxs-lookup"><span data-stu-id="1ac74-118">**String**</span></span> <br/> |<span data-ttu-id="1ac74-119">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="1ac74-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="1ac74-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="1ac74-120">Example 1</span></span>

|<span data-ttu-id="1ac74-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1ac74-121">**Cell**</span></span>|<span data-ttu-id="1ac74-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="1ac74-122">**Formula**</span></span>|<span data-ttu-id="1ac74-123">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="1ac74-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ac74-124">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="1ac74-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="1ac74-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="1ac74-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="1ac74-126">"8"</span><span class="sxs-lookup"><span data-stu-id="1ac74-126">"8"</span></span>  <br/> |
|<span data-ttu-id="1ac74-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="1ac74-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="1ac74-128">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="1ac74-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="1ac74-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="1ac74-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="1ac74-130">Renvoie FALSE parce que la valeur renvoyée est disponible.</span><span class="sxs-lookup"><span data-stu-id="1ac74-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="1ac74-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="1ac74-131">Example 2</span></span>

|<span data-ttu-id="1ac74-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="1ac74-132">**Cell**</span></span>|<span data-ttu-id="1ac74-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="1ac74-133">**Formula**</span></span>|<span data-ttu-id="1ac74-134">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="1ac74-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1ac74-135">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="1ac74-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="1ac74-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="1ac74-136">=NA( )</span></span>  <br/> |<span data-ttu-id="1ac74-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="1ac74-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="1ac74-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="1ac74-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="1ac74-139">=ISERRNA(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="1ac74-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="1ac74-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="1ac74-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="1ac74-141">Renvoie TRUE parce que la valeur renvoyée est du type d’erreur #N/A!</span><span class="sxs-lookup"><span data-stu-id="1ac74-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

