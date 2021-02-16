---
title: YEAR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Renvoie un entier qui représente l’année grégorien dans l’heure ou l’expression date/heure, mise en forme selon le style de date courte définie par les paramètres de région et de langue actuels du système.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420709"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="f882f-103">YEAR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="f882f-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="f882f-104">Renvoie un entier qui représente l’année grégorien dans l’heure ou _l’expression date/heure,_ mise en forme selon le style de date courte définie par les paramètres de région et de langue actuels du système. </span><span class="sxs-lookup"><span data-stu-id="f882f-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f882f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f882f-105">Syntax</span></span>

<span data-ttu-id="f882f-106">YEAR( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="f882f-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f882f-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f882f-107">Parameters</span></span>

|<span data-ttu-id="f882f-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f882f-108">**Name**</span></span>|<span data-ttu-id="f882f-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f882f-109">**Required/Optional**</span></span>|<span data-ttu-id="f882f-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f882f-110">**Data Type**</span></span>|<span data-ttu-id="f882f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f882f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f882f-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="f882f-112">_datetime_</span></span> <br/> |<span data-ttu-id="f882f-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f882f-113">Required</span></span>  <br/> |<span data-ttu-id="f882f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f882f-114">**String**</span></span> <br/> | <span data-ttu-id="f882f-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="f882f-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="f882f-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="f882f-116">_expression_</span></span> <br/> |<span data-ttu-id="f882f-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f882f-117">Required</span></span>  <br/> |<span data-ttu-id="f882f-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="f882f-118">**Varies**</span></span> <br/> |<span data-ttu-id="f882f-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="f882f-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="f882f-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="f882f-120">_lcid_</span></span> <br/> |<span data-ttu-id="f882f-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="f882f-121">Optional</span></span>  <br/> |<span data-ttu-id="f882f-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="f882f-122">**Numeric**</span></span> <br/> |<span data-ttu-id="f882f-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="f882f-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="f882f-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="f882f-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f882f-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f882f-125">Return value</span></span>

<span data-ttu-id="f882f-126">Entier</span><span class="sxs-lookup"><span data-stu-id="f882f-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f882f-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="f882f-127">Remarks</span></span>

<span data-ttu-id="f882f-128">Le composant d’heure  _dans l’heure ou_  _l’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="f882f-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="f882f-129">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="f882f-129">No rounding is done.</span></span> <span data-ttu-id="f882f-130">Si  _la date/heure_ est manquante ou ne peut pas être interprétée comme une date ou une heure valide, YEAR renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="f882f-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="f882f-131">La fonction YEAR accepte également une valeur de nombre unique pour  _l’expression,_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="f882f-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="f882f-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="f882f-132">Example 1</span></span>

<span data-ttu-id="f882f-133">YEAR(« 27/10/2007 13:45:24 »)</span><span class="sxs-lookup"><span data-stu-id="f882f-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="f882f-134">Renvoie 2007.</span><span class="sxs-lookup"><span data-stu-id="f882f-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="f882f-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="f882f-135">Example 2</span></span>

<span data-ttu-id="f882f-136">YEAR(VALEURDATE("25 déc. 2006") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="f882f-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="f882f-137">Renvoie 2007.</span><span class="sxs-lookup"><span data-stu-id="f882f-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="f882f-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="f882f-138">Example 3</span></span>

<span data-ttu-id="f882f-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="f882f-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="f882f-140">Renvoie 1997.</span><span class="sxs-lookup"><span data-stu-id="f882f-140">Returns 1997.</span></span>
  

