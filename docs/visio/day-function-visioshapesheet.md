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
# <a name="day-function-visioshapesheet"></a><span data-ttu-id="868c1-104">DAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="868c1-104">DAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="868c1-105">Renvoie un integer, de 1 à 31, représentant le jour dans _l’heure de date_ ou l’expression . </span><span class="sxs-lookup"><span data-stu-id="868c1-105">Returns an integer, 1 to 31, representing the day in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="868c1-106">La fonction DAY utilise le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="868c1-106">The DAY function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="868c1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="868c1-107">Syntax</span></span>

<span data-ttu-id="868c1-108">DAY( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="868c1-108">DAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="868c1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="868c1-109">Parameters</span></span>

|<span data-ttu-id="868c1-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="868c1-110">**Name**</span></span>|<span data-ttu-id="868c1-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="868c1-111">**Required/Optional**</span></span>|<span data-ttu-id="868c1-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="868c1-112">**Data Type**</span></span>|<span data-ttu-id="868c1-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="868c1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="868c1-114">_datetime_</span><span class="sxs-lookup"><span data-stu-id="868c1-114">_datetime_</span></span> <br/> |<span data-ttu-id="868c1-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="868c1-115">Required</span></span>  <br/> |<span data-ttu-id="868c1-116">**String**</span><span class="sxs-lookup"><span data-stu-id="868c1-116">**String**</span></span> <br/> |<span data-ttu-id="868c1-117">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="868c1-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="868c1-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="868c1-118">_expression_</span></span> <br/> |<span data-ttu-id="868c1-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="868c1-119">Required</span></span>  <br/> |<span data-ttu-id="868c1-120">**String**</span><span class="sxs-lookup"><span data-stu-id="868c1-120">**String**</span></span> <br/> |<span data-ttu-id="868c1-121">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="868c1-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="868c1-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="868c1-122">_lcid_</span></span> <br/> |<span data-ttu-id="868c1-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="868c1-123">Optional</span></span>  <br/> |<span data-ttu-id="868c1-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="868c1-124">**Number**</span></span> <br/> |<span data-ttu-id="868c1-p103">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="868c1-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="868c1-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="868c1-127">Return value</span></span>

<span data-ttu-id="868c1-128">Entier</span><span class="sxs-lookup"><span data-stu-id="868c1-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="868c1-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="868c1-129">Remarks</span></span>

<span data-ttu-id="868c1-130">Tout composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="868c1-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="868c1-131">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="868c1-131">No rounding is done.</span></span> <span data-ttu-id="868c1-132">Si  _la date/heure_ est manquante ou ne peut pas être convertie en un résultat valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="868c1-132">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="868c1-133">La fonction DAY accepte également une valeur de nombre unique pour  _l’expression_ où la partie d’un nombre integer du résultat représente le nombre de jours depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="868c1-133">The DAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="868c1-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="868c1-134">Example 1</span></span>

<span data-ttu-id="868c1-135">DAY("30 mai 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="868c1-135">DAY("May 30, 1997 15:45:24")</span></span>
  
<span data-ttu-id="868c1-136">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="868c1-136">Returns 30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="868c1-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="868c1-137">Example 2</span></span>

<span data-ttu-id="868c1-138">DAY(DATEVALUE("30 mai 1997") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="868c1-138">DAY(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="868c1-139">Renvoie 6.</span><span class="sxs-lookup"><span data-stu-id="868c1-139">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="868c1-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="868c1-140">Example 3</span></span>

<span data-ttu-id="868c1-141">DAY(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="868c1-141">DAY(35580.6337)</span></span>
  
<span data-ttu-id="868c1-142">Renvoie 30.</span><span class="sxs-lookup"><span data-stu-id="868c1-142">Returns 30.</span></span>
  

