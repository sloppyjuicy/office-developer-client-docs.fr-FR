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
description: Renvoie le reste (modulo) obtenu lorsqu'un nombre est divisé par un diviseur.
ms.openlocfilehash: f6b713b1b3a9d2afa85f49de9d451642a00d8dad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356993"
---
# <a name="modulus-function"></a><span data-ttu-id="51dfd-103">Fonction MODULUS</span><span class="sxs-lookup"><span data-stu-id="51dfd-103">MODULUS Function</span></span>

<span data-ttu-id="51dfd-104">Renvoie le reste (modulo) obtenu lorsqu'un nombre est divisé par un diviseur.</span><span class="sxs-lookup"><span data-stu-id="51dfd-104">Returns the remainder (modulus) that results when a number is divided by a divisor.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="51dfd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51dfd-105">Syntax</span></span>

<span data-ttu-id="51dfd-106">MODULO (\* \* *nombre* \* \*, \* \* \*\* diviseur \* \*)</span><span class="sxs-lookup"><span data-stu-id="51dfd-106">MODULUS(\*\* *number* \*\*, \*\* *divisor* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="51dfd-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51dfd-107">Parameters</span></span>

|<span data-ttu-id="51dfd-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="51dfd-108">**Name**</span></span>|<span data-ttu-id="51dfd-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="51dfd-109">**Required/Optional**</span></span>|<span data-ttu-id="51dfd-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="51dfd-110">**Data Type**</span></span>|<span data-ttu-id="51dfd-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="51dfd-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="51dfd-112">_number_</span><span class="sxs-lookup"><span data-stu-id="51dfd-112">_number_</span></span> <br/> |<span data-ttu-id="51dfd-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="51dfd-113">Required</span></span>  <br/> |<span data-ttu-id="51dfd-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="51dfd-114">**Number**</span></span> <br/> |<span data-ttu-id="51dfd-115">Dividende</span><span class="sxs-lookup"><span data-stu-id="51dfd-115">The dividend.</span></span>  <br/> |
| <span data-ttu-id="51dfd-116">_Division_</span><span class="sxs-lookup"><span data-stu-id="51dfd-116">_divisor_</span></span> <br/> |<span data-ttu-id="51dfd-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="51dfd-117">Required</span></span>  <br/> |<span data-ttu-id="51dfd-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="51dfd-118">**Number**</span></span> <br/> |<span data-ttu-id="51dfd-119">Diviseur</span><span class="sxs-lookup"><span data-stu-id="51dfd-119">The divisor.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="51dfd-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="51dfd-120">Return value</span></span>

<span data-ttu-id="51dfd-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="51dfd-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="51dfd-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="51dfd-122">Remarks</span></span>

<span data-ttu-id="51dfd-p101">Le résultat a le même signe que le diviseur. Une erreur #DIV/0! est renvoyée si le diviseur est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="51dfd-p101">The result has the same sign as the divisor. A #DIV/0! error is returned if the divisor is 0.</span></span> 
  
<span data-ttu-id="51dfd-126">Dans la plupart des cas, il est préférable d’utiliser la fonction MODULUS plutôt que la fonction MOD.</span><span class="sxs-lookup"><span data-stu-id="51dfd-126">In almost all situations, the MODULUS function should be used rather than the MOD function.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="51dfd-127">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="51dfd-127">Example 1</span></span>

<span data-ttu-id="51dfd-128">MODULUS(5; 1,4)</span><span class="sxs-lookup"><span data-stu-id="51dfd-128">MODULUS(5, 1.4)</span></span>
  
<span data-ttu-id="51dfd-129">Renvoie 0,8.</span><span class="sxs-lookup"><span data-stu-id="51dfd-129">Returns 0.8.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="51dfd-130">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="51dfd-130">Example 2</span></span>

<span data-ttu-id="51dfd-131">MODULUS(5; -1,4)</span><span class="sxs-lookup"><span data-stu-id="51dfd-131">MODULUS(5, -1.4)</span></span>
  
<span data-ttu-id="51dfd-132">Renvoie -0,6.</span><span class="sxs-lookup"><span data-stu-id="51dfd-132">Returns -0.6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="51dfd-133">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="51dfd-133">Example 3</span></span>

<span data-ttu-id="51dfd-134">MODULUS(-5; 1,4)</span><span class="sxs-lookup"><span data-stu-id="51dfd-134">MODULUS(-5, 1.4)</span></span>
  
<span data-ttu-id="51dfd-135">Renvoie 0,6.</span><span class="sxs-lookup"><span data-stu-id="51dfd-135">Returns 0.6.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="51dfd-136">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="51dfd-136">Example 4</span></span>

<span data-ttu-id="51dfd-137">MODULUS(-5; -1,4)</span><span class="sxs-lookup"><span data-stu-id="51dfd-137">MODULUS(-5, -1.4)</span></span>
  
<span data-ttu-id="51dfd-138">Renvoie -0,8.</span><span class="sxs-lookup"><span data-stu-id="51dfd-138">Returns -0.8.</span></span>
  

