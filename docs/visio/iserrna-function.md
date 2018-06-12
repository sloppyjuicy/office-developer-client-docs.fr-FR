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
description: 'Renvoie la valeur TRUE si la valeur de cellreference est erreur type # n/a ! (non disponible) ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: a471119265d77866e51ccc6bb556f2ce0095d31d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788864"
---
# <a name="iserrna-function"></a><span data-ttu-id="a0fc9-105">ISERRNA, fonction</span><span class="sxs-lookup"><span data-stu-id="a0fc9-105">ISERRNA Function</span></span>

<span data-ttu-id="a0fc9-106">Renvoie la valeur TRUE si la valeur de _cellreference_ est erreur type # n/a !</span><span class="sxs-lookup"><span data-stu-id="a0fc9-106">Returns TRUE if the value of  _cellreference_ is error type #N/A!</span></span> <span data-ttu-id="a0fc9-107">(non disponible) ; dans le cas contraire, elle renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="a0fc9-107">(not available); otherwise, it returns FALSE.</span></span> <span data-ttu-id="a0fc9-108">La fonction ISERRNA est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="a0fc9-108">The ISERRNA function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a0fc9-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0fc9-109">Syntax</span></span>

<span data-ttu-id="a0fc9-110">ISERRNA (** *cellreference* **)</span><span class="sxs-lookup"><span data-stu-id="a0fc9-110">ISERRNA(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a0fc9-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0fc9-111">Parameters</span></span>

|<span data-ttu-id="a0fc9-112">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-112">**Name**</span></span>|<span data-ttu-id="a0fc9-113">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-113">**Required/Optional**</span></span>|<span data-ttu-id="a0fc9-114">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-114">**Data Type**</span></span>|<span data-ttu-id="a0fc9-115">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0fc9-116">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="a0fc9-116">_cellreference_</span></span> <br/> |<span data-ttu-id="a0fc9-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a0fc9-117">Required</span></span>  <br/> |<span data-ttu-id="a0fc9-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-118">**String**</span></span> <br/> |<span data-ttu-id="a0fc9-119">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="a0fc9-119">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="a0fc9-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a0fc9-120">Example 1</span></span>

|<span data-ttu-id="a0fc9-121">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-121">**Cell**</span></span>|<span data-ttu-id="a0fc9-122">**Formula**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-122">**Formula**</span></span>|<span data-ttu-id="a0fc9-123">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-123">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0fc9-124">Cellule Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="a0fc9-124">Scratch.A1</span></span>  <br/> |<span data-ttu-id="a0fc9-125">="5 + 3"</span><span class="sxs-lookup"><span data-stu-id="a0fc9-125">="5 + 3"</span></span>  <br/> |<span data-ttu-id="a0fc9-126">« 8 »</span><span class="sxs-lookup"><span data-stu-id="a0fc9-126">"8"</span></span>  <br/> |
|<span data-ttu-id="a0fc9-127">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="a0fc9-127">Scratch.B1</span></span>  <br/> |<span data-ttu-id="a0fc9-128">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="a0fc9-128">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="a0fc9-129">FALSE</span><span class="sxs-lookup"><span data-stu-id="a0fc9-129">FALSE</span></span>  <br/> |
   
<span data-ttu-id="a0fc9-130">Renvoie FALSE parce que la valeur renvoyée est disponible.</span><span class="sxs-lookup"><span data-stu-id="a0fc9-130">Returns FALSE because the value returned is available.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a0fc9-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a0fc9-131">Example 2</span></span>

|<span data-ttu-id="a0fc9-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-132">**Cell**</span></span>|<span data-ttu-id="a0fc9-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-133">**Formula**</span></span>|<span data-ttu-id="a0fc9-134">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="a0fc9-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a0fc9-135">Cellule Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="a0fc9-135">Scratch.A1</span></span>  <br/> |<span data-ttu-id="a0fc9-136">=NA( )</span><span class="sxs-lookup"><span data-stu-id="a0fc9-136">=NA( )</span></span>  <br/> |<span data-ttu-id="a0fc9-137">#N/A!</span><span class="sxs-lookup"><span data-stu-id="a0fc9-137">#N/A!</span></span>  <br/> |
|<span data-ttu-id="a0fc9-138">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="a0fc9-138">Scratch.B1</span></span>  <br/> |<span data-ttu-id="a0fc9-139">=ISERRNA(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="a0fc9-139">=ISERRNA(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="a0fc9-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="a0fc9-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="a0fc9-141">Renvoie TRUE parce que la valeur renvoyée est du type d’erreur #N/A!</span><span class="sxs-lookup"><span data-stu-id="a0fc9-141">Returns TRUE because the value returned is error type #N/A!</span></span>
  

