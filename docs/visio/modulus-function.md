---
title: MODULUS, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251465
localization_priority: Normal
ms.assetid: cb6326a5-1bf8-b6a3-5c0d-d38c071353a5
description: Renvoie le reste (module) qui se traduit lorsqu’un nombre est divisé par un diviseur.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429270"
---
# <a name="modulus-function"></a><span data-ttu-id="6c99c-103">Fonction MODULUS</span><span class="sxs-lookup"><span data-stu-id="6c99c-103">MODULUS Function</span></span>

<span data-ttu-id="6c99c-104">Renvoie le reste (module) qui se traduit lorsqu’un nombre est divisé par un diviseur.</span><span class="sxs-lookup"><span data-stu-id="6c99c-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="6c99c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6c99c-105">Syntax</span></span>

<span data-ttu-id="6c99c-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span><span class="sxs-lookup"><span data-stu-id="6c99c-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6c99c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6c99c-107">Parameters</span></span>

|<span data-ttu-id="6c99c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="6c99c-108">**Name**</span></span>|<span data-ttu-id="6c99c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="6c99c-109">**Required/Optional**</span></span>|<span data-ttu-id="6c99c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="6c99c-110">**Data Type**</span></span>|<span data-ttu-id="6c99c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="6c99c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6c99c-112">_number_</span><span class="sxs-lookup"><span data-stu-id="6c99c-112">_number_</span></span> <br/> |<span data-ttu-id="6c99c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c99c-113">Required</span></span>  <br/> |<span data-ttu-id="6c99c-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="6c99c-114">**Number**</span></span> <br/> |<span data-ttu-id="6c99c-115">Dividende</span><span class="sxs-lookup"><span data-stu-id="6c99c-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="6c99c-116">_diviseur_</span><span class="sxs-lookup"><span data-stu-id="6c99c-116">_divisor_</span></span> <br/> |<span data-ttu-id="6c99c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="6c99c-117">Required</span></span>  <br/> |<span data-ttu-id="6c99c-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="6c99c-118">**Number**</span></span> <br/> |<span data-ttu-id="6c99c-119">Diviseur</span><span class="sxs-lookup"><span data-stu-id="6c99c-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6c99c-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="6c99c-120">Return value</span></span>

<span data-ttu-id="6c99c-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="6c99c-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6c99c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="6c99c-122">Remarks</span></span>

<span data-ttu-id="6c99c-p101">Le résultat a le même signe que le diviseur. Une erreur #DIV/0! est renvoyée si le diviseur est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="6c99c-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="6c99c-126">Dans la plupart des cas, il est préférable d’utiliser la fonction MODULUS plutôt que la fonction MOD.</span><span class="sxs-lookup"><span data-stu-id="6c99c-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="6c99c-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="6c99c-127">Example 1</span></span>

<span data-ttu-id="6c99c-128">MODULUS(5; 1,4)</span><span class="sxs-lookup"><span data-stu-id="6c99c-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="6c99c-129">Renvoie 0,8.</span><span class="sxs-lookup"><span data-stu-id="6c99c-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="6c99c-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="6c99c-130">Example 2</span></span>

<span data-ttu-id="6c99c-131">MODULUS(5; -1,4)</span><span class="sxs-lookup"><span data-stu-id="6c99c-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="6c99c-132">Renvoie -0,6.</span><span class="sxs-lookup"><span data-stu-id="6c99c-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="6c99c-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="6c99c-133">Example 3</span></span>

<span data-ttu-id="6c99c-134">MODULUS(-5; 1,4)</span><span class="sxs-lookup"><span data-stu-id="6c99c-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="6c99c-135">Renvoie 0,6.</span><span class="sxs-lookup"><span data-stu-id="6c99c-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="6c99c-136">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="6c99c-136">Example 4</span></span>

<span data-ttu-id="6c99c-137">MODULUS(-5; -1,4)</span><span class="sxs-lookup"><span data-stu-id="6c99c-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="6c99c-138">Renvoie -0,8.</span><span class="sxs-lookup"><span data-stu-id="6c99c-138">Returns -0.8.</span></span>
  

