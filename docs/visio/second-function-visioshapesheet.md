---
title: SECOND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Renvoie un nombre integer, de 0 à 59, qui représente le composant de secondes de date/heure ou d’expression.
ms.openlocfilehash: c23bbded12a3886fe3bd4dd2a3c3ba1bd6d11619
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404875"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="14413-103">SECOND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="14413-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="14413-104">Renvoie un nombre integer, de 0 à 59, qui représente le composant de secondes de  _date/heure_ ou  _d’expression_.</span><span class="sxs-lookup"><span data-stu-id="14413-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="14413-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14413-105">Syntax</span></span>

<span data-ttu-id="14413-106">SECOND( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="14413-106">SECOND(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="14413-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14413-107">Parameters</span></span>

|<span data-ttu-id="14413-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="14413-108">**Name**</span></span>|<span data-ttu-id="14413-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="14413-109">**Required/Optional**</span></span>|<span data-ttu-id="14413-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="14413-110">**Data Type**</span></span>|<span data-ttu-id="14413-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="14413-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="14413-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="14413-112">_datetime_</span></span> <br/> |<span data-ttu-id="14413-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="14413-113">Required</span></span>  <br/> |<span data-ttu-id="14413-114">**String**</span><span class="sxs-lookup"><span data-stu-id="14413-114">**String**</span></span> <br/> |<span data-ttu-id="14413-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="14413-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="14413-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="14413-116">_expression_</span></span> <br/> |<span data-ttu-id="14413-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="14413-117">Required</span></span>  <br/> |<span data-ttu-id="14413-118">**String**</span><span class="sxs-lookup"><span data-stu-id="14413-118">**String**</span></span> <br/> | <span data-ttu-id="14413-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="14413-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="14413-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="14413-120">_lcid_</span></span> <br/> |<span data-ttu-id="14413-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="14413-121">Optional</span></span>  <br/> |<span data-ttu-id="14413-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="14413-122">**Numeric**</span></span> <br/> |<span data-ttu-id="14413-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une  _date/heure_ non locale.</span><span class="sxs-lookup"><span data-stu-id="14413-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="14413-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="14413-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="14413-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14413-125">Return value</span></span>

<span data-ttu-id="14413-126">Entier</span><span class="sxs-lookup"><span data-stu-id="14413-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14413-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="14413-127">Remarks</span></span>

<span data-ttu-id="14413-128">Le composant date dans  _l’heure de date_  _ou l’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="14413-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="14413-129">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="14413-129">No rounding is done.</span></span> <span data-ttu-id="14413-130">Si  _la date/heure_ est manquante ou ne peut pas être convertie en un résultat valide, cette fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="14413-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="14413-131">La fonction SECOND accepte également une valeur de nombre unique pour  _l’expression_ où la partie décimale du résultat représente la fraction d’un jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="14413-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="14413-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="14413-132">Example 1</span></span>

<span data-ttu-id="14413-133">SECOND(« 30/05/1997 13:45:32 »)</span><span class="sxs-lookup"><span data-stu-id="14413-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="14413-134">Renvoie 32.</span><span class="sxs-lookup"><span data-stu-id="14413-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="14413-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="14413-135">Example 2</span></span>

<span data-ttu-id="14413-136">SECOND(TIMEVALUE("30 mai 1996 12:07:45") + 7 se.)</span><span class="sxs-lookup"><span data-stu-id="14413-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="14413-137">Renvoie 52.</span><span class="sxs-lookup"><span data-stu-id="14413-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="14413-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="14413-138">Example 3</span></span>

<span data-ttu-id="14413-139">SECOND(0,6337)</span><span class="sxs-lookup"><span data-stu-id="14413-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="14413-140">Renvoie 32.</span><span class="sxs-lookup"><span data-stu-id="14413-140">Returns 32.</span></span>
  

