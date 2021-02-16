---
title: CEILING, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: Arrondit un nombre de 0 (zéro) à l’instance suivante de plusieurs. Si plusieurs n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404126"
---
# <a name="ceiling-function"></a><span data-ttu-id="491f0-104">Fonction CEILING</span><span class="sxs-lookup"><span data-stu-id="491f0-104">CEILING Function</span></span>

<span data-ttu-id="491f0-105">Arrondit un nombre de 0 (zéro) à l’instance suivante de  _plusieurs_.</span><span class="sxs-lookup"><span data-stu-id="491f0-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="491f0-106">Si  _plusieurs_ n’est pas spécifié, le nombre est arrondi de 0 à l’integer suivant.</span><span class="sxs-lookup"><span data-stu-id="491f0-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="491f0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="491f0-107">Syntax</span></span>

<span data-ttu-id="491f0-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span><span class="sxs-lookup"><span data-stu-id="491f0-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="491f0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="491f0-109">Parameters</span></span>

|<span data-ttu-id="491f0-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="491f0-110">**Name**</span></span>|<span data-ttu-id="491f0-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="491f0-111">**Required/Optional**</span></span>|<span data-ttu-id="491f0-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="491f0-112">**Data Type**</span></span>|<span data-ttu-id="491f0-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="491f0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="491f0-114">_number_</span><span class="sxs-lookup"><span data-stu-id="491f0-114">_number_</span></span> <br/> |<span data-ttu-id="491f0-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="491f0-115">Required</span></span>  <br/> |<span data-ttu-id="491f0-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="491f0-116">**Number**</span></span> <br/> |<span data-ttu-id="491f0-117">Nombre à arrondir.</span><span class="sxs-lookup"><span data-stu-id="491f0-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="491f0-118">_multiple_</span><span class="sxs-lookup"><span data-stu-id="491f0-118">_multiple_</span></span> <br/> |<span data-ttu-id="491f0-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="491f0-119">Required</span></span>  <br/> |<span data-ttu-id="491f0-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="491f0-120">**Number**</span></span> <br/> |<span data-ttu-id="491f0-121">Multiple à arrondir.</span><span class="sxs-lookup"><span data-stu-id="491f0-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="491f0-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="491f0-122">Remarks</span></span>

 <span data-ttu-id="491f0-123">_Les_  _nombres et multiples_ doivent avoir les mêmes signes ou une #NUM !</span><span class="sxs-lookup"><span data-stu-id="491f0-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="491f0-124">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="491f0-124">error is returned.</span></span> <span data-ttu-id="491f0-125">Si un  _nombre ou_  _plusieurs ne_ peut pas être converti en valeur, un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="491f0-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="491f0-126">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="491f0-126">error is returned.</span></span> <span data-ttu-id="491f0-127">Si le  _nombre ou_  _plusieurs est_ 0, le résultat est 0.</span><span class="sxs-lookup"><span data-stu-id="491f0-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="491f0-128">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="491f0-128">Example 1</span></span>

<span data-ttu-id="491f0-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="491f0-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="491f0-130">Renvoie 4</span><span class="sxs-lookup"><span data-stu-id="491f0-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="491f0-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="491f0-131">Example 2</span></span>

<span data-ttu-id="491f0-132">CEILING(-3,7)</span><span class="sxs-lookup"><span data-stu-id="491f0-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="491f0-133">Renvoie -4</span><span class="sxs-lookup"><span data-stu-id="491f0-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="491f0-134">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="491f0-134">Example 3</span></span>

<span data-ttu-id="491f0-135">CEILING(3.7, 0.25)</span><span class="sxs-lookup"><span data-stu-id="491f0-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="491f0-136">Renvoie 3,75</span><span class="sxs-lookup"><span data-stu-id="491f0-136">Returns 3.75</span></span>
  

