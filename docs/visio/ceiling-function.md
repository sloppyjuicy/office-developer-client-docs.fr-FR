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
description: Arrondit un nombre en s'éloignant de 0 (zéro) à l'instance suivante de multiple. Si le multiple n'est pas spécifié, le nombre est arrondi de 0 à l'entier suivant.
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337225"
---
# <a name="ceiling-function"></a><span data-ttu-id="579d9-104">Fonction CEILING</span><span class="sxs-lookup"><span data-stu-id="579d9-104">CEILING Function</span></span>

<span data-ttu-id="579d9-105">Arrondit un nombre en s'éloignant de 0 (zéro) à l'instance suivante de _multiple_.</span><span class="sxs-lookup"><span data-stu-id="579d9-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="579d9-106">Si le _multiple_ n'est pas spécifié, le nombre est arrondi de 0 à l'entier suivant.</span><span class="sxs-lookup"><span data-stu-id="579d9-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="579d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="579d9-107">Syntax</span></span>

<span data-ttu-id="579d9-108">PLAFOND (\* \* *nombre* \* \*, \* \* *multiple* \* \*)</span><span class="sxs-lookup"><span data-stu-id="579d9-108">CEILING(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="579d9-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="579d9-109">Parameters</span></span>

|<span data-ttu-id="579d9-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="579d9-110">**Name**</span></span>|<span data-ttu-id="579d9-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="579d9-111">**Required/Optional**</span></span>|<span data-ttu-id="579d9-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="579d9-112">**Data Type**</span></span>|<span data-ttu-id="579d9-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="579d9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="579d9-114">_number_</span><span class="sxs-lookup"><span data-stu-id="579d9-114">_number_</span></span> <br/> |<span data-ttu-id="579d9-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="579d9-115">Required</span></span>  <br/> |<span data-ttu-id="579d9-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="579d9-116">**Number**</span></span> <br/> |<span data-ttu-id="579d9-117">Nombre à arrondir.</span><span class="sxs-lookup"><span data-stu-id="579d9-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="579d9-118">_sépar_</span><span class="sxs-lookup"><span data-stu-id="579d9-118">_multiple_</span></span> <br/> |<span data-ttu-id="579d9-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="579d9-119">Required</span></span>  <br/> |<span data-ttu-id="579d9-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="579d9-120">**Number**</span></span> <br/> |<span data-ttu-id="579d9-121">Multiple à arrondir.</span><span class="sxs-lookup"><span data-stu-id="579d9-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="579d9-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="579d9-122">Remarks</span></span>

 <span data-ttu-id="579d9-123">_Number_ et _multiple_ doivent avoir les mêmes signes ou une #NUM!</span><span class="sxs-lookup"><span data-stu-id="579d9-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="579d9-124">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="579d9-124">error is returned.</span></span> <span data-ttu-id="579d9-125">Si _nombre_ ou _multiple_ ne peuvent pas être convertis en valeur, un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="579d9-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="579d9-126">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="579d9-126">error is returned.</span></span> <span data-ttu-id="579d9-127">Si _nombre_ ou _multiple_ est 0, le résultat est 0.</span><span class="sxs-lookup"><span data-stu-id="579d9-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="579d9-128">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="579d9-128">Example 1</span></span>

<span data-ttu-id="579d9-129">PLAFOND (3.7)</span><span class="sxs-lookup"><span data-stu-id="579d9-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="579d9-130">Renvoie 4</span><span class="sxs-lookup"><span data-stu-id="579d9-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="579d9-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="579d9-131">Example 2</span></span>

<span data-ttu-id="579d9-132">PLAFOND (-3,7)</span><span class="sxs-lookup"><span data-stu-id="579d9-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="579d9-133">Renvoie -4</span><span class="sxs-lookup"><span data-stu-id="579d9-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="579d9-134">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="579d9-134">Example 3</span></span>

<span data-ttu-id="579d9-135">PLAFOND (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="579d9-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="579d9-136">Renvoie 3,75</span><span class="sxs-lookup"><span data-stu-id="579d9-136">Returns 3.75</span></span>
  

