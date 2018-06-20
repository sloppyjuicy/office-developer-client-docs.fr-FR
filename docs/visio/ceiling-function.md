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
description: Arrondit un nombre éloignée de 0 (zéro) à l’occurrence suivante du dénominateur. Si plusieurs n’est pas spécifié, le nombre est arrondi éloignée de 0 à l’entier.
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788201"
---
# <a name="ceiling-function"></a><span data-ttu-id="6f491-104">CEILING, fonction</span><span class="sxs-lookup"><span data-stu-id="6f491-104">CEILING Function</span></span>

<span data-ttu-id="6f491-105">Arrondit un nombre éloignée de 0 (zéro) à l’occurrence suivante de _multiple_.</span><span class="sxs-lookup"><span data-stu-id="6f491-105">Rounds a number away from 0 (zero) to the next instance of  _multiple_.</span></span> <span data-ttu-id="6f491-106">Si _plusieurs_ n’est pas spécifié, le nombre est arrondi éloignée de 0 à l’entier.</span><span class="sxs-lookup"><span data-stu-id="6f491-106">If  _multiple_ is not specified, the number rounds away from 0 to the next integer.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6f491-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6f491-107">Syntax</span></span>

<span data-ttu-id="6f491-108">CEILING (** *numéro* **, ** *plusieurs* **)</span><span class="sxs-lookup"><span data-stu-id="6f491-108">CEILING(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6f491-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6f491-109">Parameters</span></span>

|<span data-ttu-id="6f491-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="6f491-110">**Name**</span></span>|<span data-ttu-id="6f491-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="6f491-111">**Required/Optional**</span></span>|<span data-ttu-id="6f491-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="6f491-112">**Data Type**</span></span>|<span data-ttu-id="6f491-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="6f491-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6f491-114">_number_</span><span class="sxs-lookup"><span data-stu-id="6f491-114">_number_</span></span> <br/> |<span data-ttu-id="6f491-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6f491-115">Required</span></span>  <br/> |<span data-ttu-id="6f491-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="6f491-116">**Number**</span></span> <br/> |<span data-ttu-id="6f491-117">Nombre à arrondir.</span><span class="sxs-lookup"><span data-stu-id="6f491-117">The number to round.</span></span>  <br/> |
| <span data-ttu-id="6f491-118">_plusieurs_</span><span class="sxs-lookup"><span data-stu-id="6f491-118">_multiple_</span></span> <br/> |<span data-ttu-id="6f491-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6f491-119">Required</span></span>  <br/> |<span data-ttu-id="6f491-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="6f491-120">**Number**</span></span> <br/> |<span data-ttu-id="6f491-121">Plusieurs à arrondir à.</span><span class="sxs-lookup"><span data-stu-id="6f491-121">The multiple to round to.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f491-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="6f491-122">Remarks</span></span>

 <span data-ttu-id="6f491-123">_Nombre_ et _plusieurs_ doivent avoir le même signe, sinon une #NUM !</span><span class="sxs-lookup"><span data-stu-id="6f491-123">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="6f491-124">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="6f491-124">error is returned.</span></span> <span data-ttu-id="6f491-125">Si _nombre_ ou _multiple_ ne peut pas être convertie en une valeur, un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="6f491-125">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="6f491-126">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="6f491-126">error is returned.</span></span> <span data-ttu-id="6f491-127">Si le _nombre_ ou le _multiple_ est égal à 0, le résultat est 0.</span><span class="sxs-lookup"><span data-stu-id="6f491-127">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6f491-128">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="6f491-128">Example 1</span></span>

<span data-ttu-id="6f491-129">CEILING(3.7)</span><span class="sxs-lookup"><span data-stu-id="6f491-129">CEILING(3.7)</span></span>
  
<span data-ttu-id="6f491-130">Renvoie 4</span><span class="sxs-lookup"><span data-stu-id="6f491-130">Returns 4</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6f491-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="6f491-131">Example 2</span></span>

<span data-ttu-id="6f491-132">CEILING(-3.7)</span><span class="sxs-lookup"><span data-stu-id="6f491-132">CEILING(-3.7)</span></span>
  
<span data-ttu-id="6f491-133">Renvoie -4</span><span class="sxs-lookup"><span data-stu-id="6f491-133">Returns -4</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6f491-134">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="6f491-134">Example 3</span></span>

<span data-ttu-id="6f491-135">CEILING (3.7, 0,25)</span><span class="sxs-lookup"><span data-stu-id="6f491-135">CEILING(3.7, 0.25)</span></span>
  
<span data-ttu-id="6f491-136">Renvoie 3,75</span><span class="sxs-lookup"><span data-stu-id="6f491-136">Returns 3.75</span></span>
  

