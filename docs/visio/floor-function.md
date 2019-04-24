---
title: FLOOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arrondit un nombre vers 0 (zéro), l'entier suivant ou l'occurrence suivante de multiple.
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346178"
---
# <a name="floor-function"></a><span data-ttu-id="fec7c-103">Fonction FLOOR</span><span class="sxs-lookup"><span data-stu-id="fec7c-103">FLOOR Function</span></span>

<span data-ttu-id="fec7c-104">Arrondit un nombre vers 0 (zéro), l'entier suivant ou l'occurrence suivante de _multiple_.</span><span class="sxs-lookup"><span data-stu-id="fec7c-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="fec7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fec7c-105">Syntax</span></span>

<span data-ttu-id="fec7c-106">PLANCHER (\* \* *nombre* \* \*, \* \* *multiple* \* \*)</span><span class="sxs-lookup"><span data-stu-id="fec7c-106">FLOOR(\*\* *number* \*\*, \*\* *multiple* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="fec7c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fec7c-107">Parameters</span></span>

|<span data-ttu-id="fec7c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="fec7c-108">**Name**</span></span>|<span data-ttu-id="fec7c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="fec7c-109">**Required/Optional**</span></span>|<span data-ttu-id="fec7c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="fec7c-110">**Data Type**</span></span>|<span data-ttu-id="fec7c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="fec7c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="fec7c-112">_number_</span><span class="sxs-lookup"><span data-stu-id="fec7c-112">_number_</span></span> <br/> |<span data-ttu-id="fec7c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fec7c-113">Required</span></span>  <br/> |<span data-ttu-id="fec7c-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="fec7c-114">**Number**</span></span> <br/> |<span data-ttu-id="fec7c-115">Nombre à arrondir.</span><span class="sxs-lookup"><span data-stu-id="fec7c-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="fec7c-116">_sépar_</span><span class="sxs-lookup"><span data-stu-id="fec7c-116">_multiple_</span></span> <br/> |<span data-ttu-id="fec7c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="fec7c-117">Required</span></span>  <br/> |<span data-ttu-id="fec7c-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="fec7c-118">**Number**</span></span> <br/> |<span data-ttu-id="fec7c-119">Multiple vers lequel arrondir.</span><span class="sxs-lookup"><span data-stu-id="fec7c-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="fec7c-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="fec7c-120">Return value</span></span>

<span data-ttu-id="fec7c-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="fec7c-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fec7c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="fec7c-122">Remarks</span></span>

<span data-ttu-id="fec7c-123">Si le _multiple_ n'est pas spécifié, le nombre est arrondi à l'entier supérieur de 0.</span><span class="sxs-lookup"><span data-stu-id="fec7c-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="fec7c-124">_Number_ et _multiple_ doivent avoir les mêmes signes ou une #NUM!</span><span class="sxs-lookup"><span data-stu-id="fec7c-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="fec7c-125">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="fec7c-125">error is returned.</span></span> <span data-ttu-id="fec7c-126">Si _nombre_ ou _multiple_ ne peuvent pas être convertis en valeur, un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="fec7c-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="fec7c-127">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="fec7c-127">error is returned.</span></span> <span data-ttu-id="fec7c-128">Si _nombre_ ou _multiple_ est 0, le résultat est 0.</span><span class="sxs-lookup"><span data-stu-id="fec7c-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="fec7c-129">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="fec7c-129">Example 1</span></span>

<span data-ttu-id="fec7c-130">PLANCHER (3.7)</span><span class="sxs-lookup"><span data-stu-id="fec7c-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="fec7c-131">Renvoie 3.</span><span class="sxs-lookup"><span data-stu-id="fec7c-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="fec7c-132">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="fec7c-132">Example 2</span></span>

<span data-ttu-id="fec7c-133">PLANCHER (-3,7)</span><span class="sxs-lookup"><span data-stu-id="fec7c-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="fec7c-134">Renvoie -3.</span><span class="sxs-lookup"><span data-stu-id="fec7c-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="fec7c-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="fec7c-135">Example 3</span></span>

<span data-ttu-id="fec7c-136">PLANCHER (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="fec7c-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="fec7c-137">Renvoie 3,5.</span><span class="sxs-lookup"><span data-stu-id="fec7c-137">Returns 3.5.</span></span>
  

