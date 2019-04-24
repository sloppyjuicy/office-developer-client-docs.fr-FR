---
title: CY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253223
localization_priority: Normal
ms.assetid: abb27f90-21b4-08cd-6995-9520fbcebd78
description: Renvoie une valeur monétaire.
ms.openlocfilehash: 65c88d69669e2fa7f708402d9d50dfe035456edb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344988"
---
# <a name="cy-function"></a><span data-ttu-id="52223-103">Fonction CY</span><span class="sxs-lookup"><span data-stu-id="52223-103">CY Function</span></span>

<span data-ttu-id="52223-104">Renvoie une valeur monétaire.</span><span class="sxs-lookup"><span data-stu-id="52223-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="52223-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52223-105">Syntax</span></span>

<span data-ttu-id="52223-106">CY (\* \* *valeur* \* \*, \* \* *cyID* \* \*)</span><span class="sxs-lookup"><span data-stu-id="52223-106">CY(\*\* *value* \*\*, \*\* *cyID* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="52223-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52223-107">Parameters</span></span>

|<span data-ttu-id="52223-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="52223-108">**Name**</span></span>|<span data-ttu-id="52223-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="52223-109">**Required/Optional**</span></span>|<span data-ttu-id="52223-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="52223-110">**Data Type**</span></span>|<span data-ttu-id="52223-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="52223-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="52223-112">_value_</span><span class="sxs-lookup"><span data-stu-id="52223-112">_value_</span></span> <br/> |<span data-ttu-id="52223-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="52223-113">Optional</span></span>  <br/> |<span data-ttu-id="52223-114">**Numéro ou Chaîne**</span><span class="sxs-lookup"><span data-stu-id="52223-114">**Number or String**</span></span> <br/> |<span data-ttu-id="52223-115">Nombre ou chaîne qui inclut la mise en forme spécifique à la monnaie.</span><span class="sxs-lookup"><span data-stu-id="52223-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="52223-116">Si ce paramètre n'est pas spécifié, la valeur de la devise est mise en forme selon le style monétaire défini dans les paramètres région et langue du système.</span><span class="sxs-lookup"><span data-stu-id="52223-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="52223-117">_cyID_</span><span class="sxs-lookup"><span data-stu-id="52223-117">_cyID_</span></span> <br/> |<span data-ttu-id="52223-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="52223-118">Optional</span></span>  <br/> |<span data-ttu-id="52223-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="52223-119">**Number**</span></span> <br/> |<span data-ttu-id="52223-120">Un numéro de devise numérique ou une chaîne entre guillemets à trois caractères pour l'abréviation ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="52223-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52223-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="52223-121">Remarks</span></span>

<span data-ttu-id="52223-122">Pour spécifier une autre devise, vous devez inclure un _cyID_valide.</span><span class="sxs-lookup"><span data-stu-id="52223-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="52223-123">Pour obtenir la liste des constantes monétaires, reportez-vous à la rubrique [À propos des constantes monétaires](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="52223-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="52223-124">Si la _valeur_ n'est pas compatible avec le type de devise désigné, ou si un argument non valide comme «pas un numéro» est spécifié, une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="52223-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="52223-125">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="52223-125">error is returned.</span></span> <span data-ttu-id="52223-126">Si _value_ est supérieur à 922 337 203 685 477,5807 ou inférieur à-922 337 203 685 477,5808, un #VALUE!</span><span class="sxs-lookup"><span data-stu-id="52223-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="52223-127">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="52223-127">error is returned.</span></span> 
  
<span data-ttu-id="52223-128">Pour une meilleure précision des valeurs monétaires très importantes incluant des fractions d'une unité, comme 3 600 000 000 000, utilisez des arguments de chaîne pour _value_.</span><span class="sxs-lookup"><span data-stu-id="52223-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="52223-129">La spécification d'un _cyID_ non valide renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="52223-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="52223-130">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="52223-130">Example 1</span></span>

<span data-ttu-id="52223-131">Si les paramètres régionaux et de langue de l’utilisateur indiquent le dollar des États-Unis :</span><span class="sxs-lookup"><span data-stu-id="52223-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="52223-132">CY (999998.993)</span><span class="sxs-lookup"><span data-stu-id="52223-132">CY(999998.993)</span></span>
  
<span data-ttu-id="52223-133">Renvoie 999 998,99 USD</span><span class="sxs-lookup"><span data-stu-id="52223-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="52223-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="52223-134">Example 2</span></span>

<span data-ttu-id="52223-135">CY (12345678,993, "USD")</span><span class="sxs-lookup"><span data-stu-id="52223-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="52223-136">Renvoie 12 345 678,99 USD</span><span class="sxs-lookup"><span data-stu-id="52223-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="52223-137">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="52223-137">Example 3</span></span>

<span data-ttu-id="52223-138">CY(12345678,993, "EUR")</span><span class="sxs-lookup"><span data-stu-id="52223-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="52223-139">Renvoie 12 345 678,99 EUR</span><span class="sxs-lookup"><span data-stu-id="52223-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="52223-140">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="52223-140">Example 4</span></span>

<span data-ttu-id="52223-141">CY(12345678,7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="52223-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="52223-142">Renvoie 12 345 678,78</span><span class="sxs-lookup"><span data-stu-id="52223-142">Returns 12,345,678.78</span></span>
  

