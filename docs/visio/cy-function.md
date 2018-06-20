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
description: Renvoie une valeur de devise.
ms.openlocfilehash: ea7696e7628939466730b9c054a706a7a9fa264e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788382"
---
# <a name="cy-function"></a><span data-ttu-id="7be0a-103">CY, fonction</span><span class="sxs-lookup"><span data-stu-id="7be0a-103">CY Function</span></span>

<span data-ttu-id="7be0a-104">Renvoie une valeur de devise.</span><span class="sxs-lookup"><span data-stu-id="7be0a-104">Returns a currency value.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="7be0a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7be0a-105">Syntax</span></span>

<span data-ttu-id="7be0a-106">CY (** *valeur* **, ** *IDdev* **)</span><span class="sxs-lookup"><span data-stu-id="7be0a-106">CY(** *value* **, ** *cyID* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7be0a-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7be0a-107">Parameters</span></span>

|<span data-ttu-id="7be0a-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="7be0a-108">**Name**</span></span>|<span data-ttu-id="7be0a-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7be0a-109">**Required/Optional**</span></span>|<span data-ttu-id="7be0a-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7be0a-110">**Data Type**</span></span>|<span data-ttu-id="7be0a-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7be0a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7be0a-112">_valeur_</span><span class="sxs-lookup"><span data-stu-id="7be0a-112">_value_</span></span> <br/> |<span data-ttu-id="7be0a-113">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7be0a-113">Optional</span></span>  <br/> |<span data-ttu-id="7be0a-114">**Nombre ou chaîne**</span><span class="sxs-lookup"><span data-stu-id="7be0a-114">**Number or String**</span></span> <br/> |<span data-ttu-id="7be0a-115">Nombre ou chaîne qui inclut la mise en forme spécifique à une devise.</span><span class="sxs-lookup"><span data-stu-id="7be0a-115">A number or a string that includes currency-specific formatting.</span></span> <span data-ttu-id="7be0a-116">Le cas contraire, la valeur de devise est formatée selon le style défini dans les paramètres régionaux et de langue du système.</span><span class="sxs-lookup"><span data-stu-id="7be0a-116">If not specified, the currency value is formatted according to the currency style in the system's Region and Language settings.</span></span>  <br/> |
| <span data-ttu-id="7be0a-117">_IDdev_</span><span class="sxs-lookup"><span data-stu-id="7be0a-117">_cyID_</span></span> <br/> |<span data-ttu-id="7be0a-118">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7be0a-118">Optional</span></span>  <br/> |<span data-ttu-id="7be0a-119">**Number**</span><span class="sxs-lookup"><span data-stu-id="7be0a-119">**Number**</span></span> <br/> |<span data-ttu-id="7be0a-120">ID monétaire numérique ou une chaîne entre guillemets trois caractères pour l’abréviation ISO 4217.</span><span class="sxs-lookup"><span data-stu-id="7be0a-120">A numeric currency ID or a three-character quoted string for the ISO 4217 abbreviation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7be0a-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="7be0a-121">Remarks</span></span>

<span data-ttu-id="7be0a-122">Pour spécifier une autre devise, vous devez inclure un _argument IDdev_valide.</span><span class="sxs-lookup"><span data-stu-id="7be0a-122">To specify a different currency, you must include a valid  _cyID_.</span></span> <span data-ttu-id="7be0a-123">Pour obtenir la liste, voir [à propos des constantes de devise](about-currency-constants.md).</span><span class="sxs-lookup"><span data-stu-id="7be0a-123">For a list, see [About currency constants](about-currency-constants.md).</span></span>
  
<span data-ttu-id="7be0a-124">Si la _valeur_ n’est pas compatible avec le type de devise défini ou si un argument non valide, tel que « pas un nombre » est spécifié, un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="7be0a-124">If  _value_ is incompatible with the designated currency type, or if an invalid argument such as "not a number" is specified, a #VALUE!</span></span> <span data-ttu-id="7be0a-125">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="7be0a-125">error is returned.</span></span> <span data-ttu-id="7be0a-126">Si la _valeur_ est supérieure à 922,337,203,685,477.5807 ou inférieur à-922,337,203,685,477.5808, un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="7be0a-126">If  _value_ is greater than 922,337,203,685,477.5807 or less than -922,337,203,685,477.5808, a #VALUE!</span></span> <span data-ttu-id="7be0a-127">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="7be0a-127">error is returned.</span></span> 
  
<span data-ttu-id="7be0a-128">Pour améliorer la précision des valeurs monétaires très élevées contenant des fractions d’une unité, telles que 3,6 trillions, utilisez des arguments de chaîne pour _valeur_.</span><span class="sxs-lookup"><span data-stu-id="7be0a-128">For better precision with very large currency values that include fractions of a unit, such as 3.6 trillion, use string arguments for  _value_.</span></span>
  
<span data-ttu-id="7be0a-129">Spécifier un _argument IDdev_ incorrect renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="7be0a-129">Specifying an invalid  _cyID_ returns an error.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7be0a-130">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="7be0a-130">Example 1</span></span>

<span data-ttu-id="7be0a-131">Si les paramètres régionaux et de langue de l’utilisateur indiquent le dollar des États-Unis :</span><span class="sxs-lookup"><span data-stu-id="7be0a-131">If the user's Region and Language settings specify United States dollars:</span></span>
  
<span data-ttu-id="7be0a-132">CY(999998.993)</span><span class="sxs-lookup"><span data-stu-id="7be0a-132">CY(999998.993)</span></span>
  
<span data-ttu-id="7be0a-133">Renvoie 999 998,99 USD</span><span class="sxs-lookup"><span data-stu-id="7be0a-133">Returns $999,998.99</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7be0a-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="7be0a-134">Example 2</span></span>

<span data-ttu-id="7be0a-135">CY (12345678,993, "USD")</span><span class="sxs-lookup"><span data-stu-id="7be0a-135">CY(12345678.993, "USD")</span></span>
  
<span data-ttu-id="7be0a-136">Renvoie 12 345 678,99 USD</span><span class="sxs-lookup"><span data-stu-id="7be0a-136">Returns $12,345,678.99</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7be0a-137">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="7be0a-137">Example 3</span></span>

<span data-ttu-id="7be0a-138">CY(12345678,993, "EUR")</span><span class="sxs-lookup"><span data-stu-id="7be0a-138">CY(12345678.993, "DEM")</span></span>
  
<span data-ttu-id="7be0a-139">Renvoie 12 345 678,99 EUR</span><span class="sxs-lookup"><span data-stu-id="7be0a-139">Returns 12,345,678.99 DEM</span></span>
  
## <a name="example-4"></a><span data-ttu-id="7be0a-140">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="7be0a-140">Example 4</span></span>

<span data-ttu-id="7be0a-141">CY(12345678,7832, "XXX")</span><span class="sxs-lookup"><span data-stu-id="7be0a-141">CY(12345678.7832, "XXX")</span></span>
  
<span data-ttu-id="7be0a-142">Renvoie 12 345 678,78</span><span class="sxs-lookup"><span data-stu-id="7be0a-142">Returns 12,345,678.78</span></span>
  

