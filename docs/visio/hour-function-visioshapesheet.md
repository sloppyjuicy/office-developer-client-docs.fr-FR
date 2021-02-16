---
title: HOUR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251437
localization_priority: Normal
ms.assetid: 2a21d6f9-bad6-92ab-6d36-477bcb9d7f17
description: Renvoie un nombre integer, de 0 à 23, qui représente l’heure du jour du date/heure ou de l’expression.
ms.openlocfilehash: 1d0c6ec2bd80605401f44d2a5ef6e3d41bc72556
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429634"
---
# <a name="hour-function-visioshapesheet"></a><span data-ttu-id="42f7b-103">HOUR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="42f7b-103">HOUR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="42f7b-104">Renvoie un nombre integer, de 0 à 23, qui représente l’heure du jour du  _date/heure_ ou de  _l’expression_.</span><span class="sxs-lookup"><span data-stu-id="42f7b-104">Returns an integer, 0 to 23, representing the hour of the day of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="42f7b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42f7b-105">Syntax</span></span>

<span data-ttu-id="42f7b-106">HOUR( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="42f7b-106">HOUR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="42f7b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42f7b-107">Parameters</span></span>

|<span data-ttu-id="42f7b-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="42f7b-108">**Name**</span></span>|<span data-ttu-id="42f7b-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="42f7b-109">**Required/Optional**</span></span>|<span data-ttu-id="42f7b-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="42f7b-110">**Data Type**</span></span>|<span data-ttu-id="42f7b-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="42f7b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="42f7b-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="42f7b-112">_datetime_</span></span> <br/> |<span data-ttu-id="42f7b-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="42f7b-113">Required</span></span>  <br/> |<span data-ttu-id="42f7b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="42f7b-114">**String**</span></span> <br/> | <span data-ttu-id="42f7b-115">Chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="42f7b-115">A string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="42f7b-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="42f7b-116">_expression_</span></span> <br/> |<span data-ttu-id="42f7b-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="42f7b-117">Required</span></span>  <br/> |<span data-ttu-id="42f7b-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="42f7b-118">**Varies**</span></span> <br/> |<span data-ttu-id="42f7b-119">Expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="42f7b-119">An expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="42f7b-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="42f7b-120">_lcid_</span></span> <br/> |<span data-ttu-id="42f7b-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="42f7b-121">Optional</span></span>  <br/> |<span data-ttu-id="42f7b-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="42f7b-122">**Number**</span></span> <br/> | <span data-ttu-id="42f7b-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="42f7b-123">A locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="42f7b-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="42f7b-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42f7b-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="42f7b-125">Remarks</span></span>

<span data-ttu-id="42f7b-126">Le composant date dans  *l’heure et*  *l’expression*  est ignoré.</span><span class="sxs-lookup"><span data-stu-id="42f7b-126">The date component in  *datetime*  and  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="42f7b-127">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="42f7b-127">No rounding is done.</span></span> <span data-ttu-id="42f7b-128">Si la  *date/heure*  est manquante ou ne peut pas être convertie en un résultat valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="42f7b-128">If the  *datetime*  is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="42f7b-129">La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="42f7b-129">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="42f7b-130">La fonction HOUR accepte également une valeur de nombre unique pour  *l’expression*  où la partie décimale du résultat représente la fraction d’un jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="42f7b-130">The HOUR function also accepts a single number value for  *expression*  where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="42f7b-131">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="42f7b-131">Example 1</span></span>

<span data-ttu-id="42f7b-132">HOUR(« 15:45 »)</span><span class="sxs-lookup"><span data-stu-id="42f7b-132">HOUR("15:45")</span></span>
  
<span data-ttu-id="42f7b-133">Renvoie 15.</span><span class="sxs-lookup"><span data-stu-id="42f7b-133">Returns 15.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="42f7b-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="42f7b-134">Example 2</span></span>

<span data-ttu-id="42f7b-135">HOUR("30 mai 1997 15:45:24")</span><span class="sxs-lookup"><span data-stu-id="42f7b-135">HOUR("May 30, 1997 3:45:24 PM")</span></span>
  
<span data-ttu-id="42f7b-136">Renvoie 15.</span><span class="sxs-lookup"><span data-stu-id="42f7b-136">Returns 15.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="42f7b-137">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="42f7b-137">Example 3</span></span>

<span data-ttu-id="42f7b-138">HOUR(0,5)</span><span class="sxs-lookup"><span data-stu-id="42f7b-138">HOUR(0.5)</span></span>
  
<span data-ttu-id="42f7b-139">Renvoie 12.</span><span class="sxs-lookup"><span data-stu-id="42f7b-139">Returns 12.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="42f7b-140">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="42f7b-140">Example 4</span></span>

<span data-ttu-id="42f7b-141">HOUR(« 30/5/1997 »)</span><span class="sxs-lookup"><span data-stu-id="42f7b-141">HOUR("5/30/1997")</span></span>
  
<span data-ttu-id="42f7b-142">Renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="42f7b-142">Returns 0.</span></span>
  

