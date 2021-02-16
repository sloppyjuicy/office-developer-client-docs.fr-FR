---
title: TIMEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Renvoie la valeur d’heure représentée par l’heure ou l’expression, en fonction des paramètres de région et de langue du système.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432323"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="c0a96-103">TIMEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="c0a96-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="c0a96-104">Renvoie la valeur d’heure représentée par _l’heure ou_ l’expression, en fonction des paramètres de région et de langue du système. </span><span class="sxs-lookup"><span data-stu-id="c0a96-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c0a96-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0a96-105">Syntax</span></span>

<span data-ttu-id="c0a96-106">TIMEVALUE( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="c0a96-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0a96-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0a96-107">Parameters</span></span>

|<span data-ttu-id="c0a96-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c0a96-108">**Name**</span></span>|<span data-ttu-id="c0a96-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c0a96-109">**Required/Optional**</span></span>|<span data-ttu-id="c0a96-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c0a96-110">**Data Type**</span></span>|<span data-ttu-id="c0a96-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0a96-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0a96-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="c0a96-112">_datetime_</span></span> <br/> |<span data-ttu-id="c0a96-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0a96-113">Required</span></span>  <br/> |<span data-ttu-id="c0a96-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c0a96-114">**String**</span></span> <br/> | <span data-ttu-id="c0a96-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="c0a96-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="c0a96-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="c0a96-116">_expression_</span></span> <br/> |<span data-ttu-id="c0a96-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0a96-117">Required</span></span>  <br/> |<span data-ttu-id="c0a96-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="c0a96-118">**Varies**</span></span> <br/> | <span data-ttu-id="c0a96-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="c0a96-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="c0a96-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="c0a96-120">_lcid_</span></span> <br/> |<span data-ttu-id="c0a96-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c0a96-121">Optional</span></span>  <br/> |<span data-ttu-id="c0a96-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="c0a96-122">**Number**</span></span> <br/> |<span data-ttu-id="c0a96-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="c0a96-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="c0a96-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="c0a96-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0a96-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0a96-125">Remarks</span></span>

<span data-ttu-id="c0a96-126">Tout composant de date dans _l’heure de date_ ou l’expression est ignoré. </span><span class="sxs-lookup"><span data-stu-id="c0a96-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="c0a96-127">Si  _la date/heure_ est manquante ou ne peut pas être convertie en un résultat valide, cette fonction renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="c0a96-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="c0a96-128">erreur.</span><span class="sxs-lookup"><span data-stu-id="c0a96-128">error.</span></span> 
  
<span data-ttu-id="c0a96-129">La fonction TIMEVALUE accepte également une valeur de nombre unique pour  _l’expression_ où la partie décimale du résultat représente la fraction d’un jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="c0a96-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c0a96-130">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="c0a96-130">Example 1</span></span>

<span data-ttu-id="c0a96-131">TIMEVALUE("6:00")</span><span class="sxs-lookup"><span data-stu-id="c0a96-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="c0a96-132">Renvoie la valeur représentant 06:00:00.</span><span class="sxs-lookup"><span data-stu-id="c0a96-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c0a96-133">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="c0a96-133">Example 2</span></span>

<span data-ttu-id="c0a96-134">TIMEVALUE("14:30") + 4 he.+ 30 me.</span><span class="sxs-lookup"><span data-stu-id="c0a96-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="c0a96-135">Renvoie la valeur représentant 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="c0a96-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c0a96-136">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="c0a96-136">Example 3</span></span>

<span data-ttu-id="c0a96-137">TIMEVALUE("11 h, 1er juillet 1997")</span><span class="sxs-lookup"><span data-stu-id="c0a96-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="c0a96-138">Renvoie la valeur représentant 11:00:00.</span><span class="sxs-lookup"><span data-stu-id="c0a96-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="c0a96-139">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="c0a96-139">Example 4</span></span>

<span data-ttu-id="c0a96-140">TIMEVALUE(0,6337)</span><span class="sxs-lookup"><span data-stu-id="c0a96-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="c0a96-141">Renvoie la valeur représentant 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="c0a96-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="c0a96-142">Exemple 5</span><span class="sxs-lookup"><span data-stu-id="c0a96-142">Example 5</span></span>

<span data-ttu-id="c0a96-143">TIMEVALUE(« 7:89 »)</span><span class="sxs-lookup"><span data-stu-id="c0a96-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="c0a96-p103">Renvoie une erreur #VALEUR!.</span><span class="sxs-lookup"><span data-stu-id="c0a96-p103">Returns a #VALUE! error.</span></span>
  

