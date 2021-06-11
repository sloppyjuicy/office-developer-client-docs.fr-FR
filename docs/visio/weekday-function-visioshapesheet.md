---
title: WEEKDAY Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Renvoie un integer, de 1 à 7, représentant le jour de la semaine dans l’heure ou l’expression.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404805"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="bba35-103">WEEKDAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="bba35-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="bba35-104">Renvoie un integer, de 1 à 7, représentant le jour de la semaine dans _l’heure de date ou_ l’expression . </span><span class="sxs-lookup"><span data-stu-id="bba35-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bba35-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bba35-105">Syntax</span></span>

<span data-ttu-id="bba35-106">WEEKDAY( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="bba35-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bba35-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bba35-107">Parameters</span></span>

|<span data-ttu-id="bba35-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bba35-108">**Name**</span></span>|<span data-ttu-id="bba35-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="bba35-109">**Required/Optional**</span></span>|<span data-ttu-id="bba35-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bba35-110">**Data Type**</span></span>|<span data-ttu-id="bba35-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="bba35-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bba35-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="bba35-112">_datetime_</span></span> <br/> |<span data-ttu-id="bba35-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bba35-113">Required</span></span>  <br/> |<span data-ttu-id="bba35-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bba35-114">**String**</span></span> <br/> | <span data-ttu-id="bba35-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="bba35-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="bba35-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="bba35-116">_expression_</span></span> <br/> |<span data-ttu-id="bba35-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bba35-117">Required</span></span>  <br/> |<span data-ttu-id="bba35-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="bba35-118">**Varies**</span></span> <br/> |<span data-ttu-id="bba35-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="bba35-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="bba35-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="bba35-120">_lcid_</span></span> <br/> |<span data-ttu-id="bba35-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="bba35-121">Optional</span></span>  <br/> |<span data-ttu-id="bba35-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="bba35-122">**Numeric**</span></span> <br/> |<span data-ttu-id="bba35-p101">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="bba35-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bba35-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bba35-125">Return value</span></span>

<span data-ttu-id="bba35-126">Entier</span><span class="sxs-lookup"><span data-stu-id="bba35-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bba35-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="bba35-127">Remarks</span></span>

<span data-ttu-id="bba35-128">Le composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="bba35-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="bba35-129">Le résultat est compris entre lundi (1) et dimanche (7).</span><span class="sxs-lookup"><span data-stu-id="bba35-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="bba35-130">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="bba35-130">No rounding is done.</span></span> <span data-ttu-id="bba35-131">Si  _la date/heure_ est manquante ou ne peut pas être interprétée comme une date ou une heure valide, la fonction renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="bba35-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="bba35-132">erreur.</span><span class="sxs-lookup"><span data-stu-id="bba35-132">error.</span></span> 
  
<span data-ttu-id="bba35-133">La fonction WEEKDAY accepte également une valeur de nombre unique pour  _l’expression,_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="bba35-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="bba35-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="bba35-134">Example 1</span></span>

<span data-ttu-id="bba35-135">WEEKDAY("30 mai 1999")</span><span class="sxs-lookup"><span data-stu-id="bba35-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="bba35-136">Renvoie 7.</span><span class="sxs-lookup"><span data-stu-id="bba35-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bba35-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="bba35-137">Example 2</span></span>

<span data-ttu-id="bba35-138">WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)</span><span class="sxs-lookup"><span data-stu-id="bba35-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="bba35-139">Renvoie 2.</span><span class="sxs-lookup"><span data-stu-id="bba35-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bba35-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="bba35-140">Example 3</span></span>

<span data-ttu-id="bba35-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="bba35-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="bba35-142">Renvoie 4.</span><span class="sxs-lookup"><span data-stu-id="bba35-142">Returns 4.</span></span>
  

