---
title: DAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251415
localization_priority: Normal
ms.assetid: 3b0842ae-6893-2d7b-6cb2-8905198fae30
description: Renvoie un integer, de 1 à 31, qui représente le jour dans l’expression ou l’heure de date. La fonction DAY utilise le calendrier grégorien.
ms.openlocfilehash: 49c29d5dc25bf11599f89a20cb2bc2367bd74187
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360295"
---
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="f1da0-104">DAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="f1da0-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="f1da0-105">Renvoie un integer, de 1 à 31, qui représente le jour dans _l’heure de date ou_ l’expression . </span><span class="sxs-lookup"><span data-stu-id="f1da0-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="f1da0-106">La fonction DAY utilise le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="f1da0-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f1da0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1da0-107">Syntax</span></span>

<span data-ttu-id="f1da0-108">DAY( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="f1da0-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f1da0-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1da0-109">Parameters</span></span>

|<span data-ttu-id="f1da0-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f1da0-110">**Name**</span></span>|<span data-ttu-id="f1da0-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f1da0-111">**Required/Optional**</span></span>|<span data-ttu-id="f1da0-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f1da0-112">**Data Type**</span></span>|<span data-ttu-id="f1da0-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="f1da0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f1da0-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="f1da0-114">_datetime_</span></span> <br/> |<span data-ttu-id="f1da0-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f1da0-115">Required</span></span>  <br/> |<span data-ttu-id="f1da0-116">**String**</span><span class="sxs-lookup"><span data-stu-id="f1da0-116">**String**</span></span> <br/> |<span data-ttu-id="f1da0-117">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="f1da0-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="f1da0-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="f1da0-118">_expression_</span></span> <br/> |<span data-ttu-id="f1da0-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f1da0-119">Required</span></span>  <br/> |<span data-ttu-id="f1da0-120">**String**</span><span class="sxs-lookup"><span data-stu-id="f1da0-120">**String**</span></span> <br/> |<span data-ttu-id="f1da0-121">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="f1da0-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="f1da0-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="f1da0-122">_lcid_</span></span> <br/> |<span data-ttu-id="f1da0-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f1da0-123">Optional</span></span>  <br/> |<span data-ttu-id="f1da0-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="f1da0-124">**Number**</span></span> <br/> |<span data-ttu-id="f1da0-p103">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="f1da0-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f1da0-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f1da0-127">Return value</span></span>

<span data-ttu-id="f1da0-128">Entier</span><span class="sxs-lookup"><span data-stu-id="f1da0-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f1da0-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="f1da0-129">Remarks</span></span>

<span data-ttu-id="f1da0-130">Tout composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f1da0-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="f1da0-131">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="f1da0-131">No rounding is done.</span></span> <span data-ttu-id="f1da0-132">Si  _la date/heure_ est manquante ou ne peut pas être convertie en un résultat valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="f1da0-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="f1da0-133">La fonction DAY accepte également une valeur de nombre unique pour  _l’expression_ où la partie d’un nombre integer du résultat représente le nombre de jours depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="f1da0-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f1da0-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="f1da0-134">Example 1</span></span>

<span data-ttu-id="f1da0-135">DAY("30 mai 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="f1da0-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="f1da0-136">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="f1da0-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f1da0-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="f1da0-137">Example 2</span></span>

<span data-ttu-id="f1da0-138">DAY(DATEVALUE("30 mai 1997") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="f1da0-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="f1da0-139">Renvoie 6.</span><span class="sxs-lookup"><span data-stu-id="f1da0-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f1da0-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="f1da0-140">Example 3</span></span>

<span data-ttu-id="f1da0-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="f1da0-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="f1da0-142">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="f1da0-142">Returns 30.</span></span>
  

