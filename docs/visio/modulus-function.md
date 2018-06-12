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
description: Renvoie le reste (module) qui se produit lorsqu’un nombre est divisé par un diviseur.
ms.openlocfilehash: 4e2ef7acf9dc04e788cb2b8a0ff737f12a79c61a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789153"
---
# <a name="modulus-function"></a><span data-ttu-id="e5614-103">MODULUS, fonction</span><span class="sxs-lookup"><span data-stu-id="e5614-103">MODULUS Function</span></span>

<span data-ttu-id="e5614-104">Renvoie le reste (module) qui se produit lorsqu’un nombre est divisé par un diviseur.</span><span class="sxs-lookup"><span data-stu-id="e5614-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e5614-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e5614-105">Syntax</span></span>

<span data-ttu-id="e5614-106">MODULE (** *numéro* **, ** *diviseur* **)</span><span class="sxs-lookup"><span data-stu-id="e5614-106">MODULUS(** *number* **, ** *divisor* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e5614-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e5614-107">Parameters</span></span>

|<span data-ttu-id="e5614-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e5614-108">**Name**</span></span>|<span data-ttu-id="e5614-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e5614-109">**Required/Optional**</span></span>|<span data-ttu-id="e5614-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e5614-110">**Data Type**</span></span>|<span data-ttu-id="e5614-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e5614-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e5614-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e5614-112">_number_</span></span> <br/> |<span data-ttu-id="e5614-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5614-113">Required</span></span>  <br/> |<span data-ttu-id="e5614-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="e5614-114">**Number**</span></span> <br/> |<span data-ttu-id="e5614-115">Dividende</span><span class="sxs-lookup"><span data-stu-id="e5614-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="e5614-116">_diviseur_</span><span class="sxs-lookup"><span data-stu-id="e5614-116">_divisor_</span></span> <br/> |<span data-ttu-id="e5614-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e5614-117">Required</span></span>  <br/> |<span data-ttu-id="e5614-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="e5614-118">**Number**</span></span> <br/> |<span data-ttu-id="e5614-119">Diviseur</span><span class="sxs-lookup"><span data-stu-id="e5614-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e5614-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e5614-120">Return value</span></span>

<span data-ttu-id="e5614-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="e5614-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5614-122">Note</span><span class="sxs-lookup"><span data-stu-id="e5614-122">Remarks</span></span>

<span data-ttu-id="e5614-p101">Le résultat a le même signe que le diviseur. Une erreur #DIV/0! est renvoyée si le diviseur est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="e5614-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="e5614-126">Dans la plupart des cas, il est préférable d’utiliser la fonction MODULUS plutôt que la fonction MOD.</span><span class="sxs-lookup"><span data-stu-id="e5614-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e5614-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e5614-127">Example 1</span></span>

<span data-ttu-id="e5614-128">MODULUS(5; 1,4)</span><span class="sxs-lookup"><span data-stu-id="e5614-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="e5614-129">Renvoie 0,8.</span><span class="sxs-lookup"><span data-stu-id="e5614-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e5614-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e5614-130">Example 2</span></span>

<span data-ttu-id="e5614-131">MODULUS(5; -1,4)</span><span class="sxs-lookup"><span data-stu-id="e5614-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="e5614-132">Renvoie -0,6.</span><span class="sxs-lookup"><span data-stu-id="e5614-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e5614-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e5614-133">Example 3</span></span>

<span data-ttu-id="e5614-134">MODULUS(-5; 1,4)</span><span class="sxs-lookup"><span data-stu-id="e5614-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="e5614-135">Renvoie 0,6.</span><span class="sxs-lookup"><span data-stu-id="e5614-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="e5614-136">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="e5614-136">Example 4</span></span>

<span data-ttu-id="e5614-137">MODULUS(-5; -1,4)</span><span class="sxs-lookup"><span data-stu-id="e5614-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="e5614-138">Renvoie -0,8.</span><span class="sxs-lookup"><span data-stu-id="e5614-138">Returns -0.8.</span></span>
  

