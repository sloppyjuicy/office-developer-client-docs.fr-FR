---
title: DATETIME, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251413
localization_priority: Normal
ms.assetid: 0bf7f757-0b7f-dec1-9709-6612c9ad0d53
description: Renvoie la valeur de date et d'heure représentée par dateheure ou expression.
ms.openlocfilehash: 2da084f685c044d48495b04f727a877140b51004
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360318"
---
# <a name="datetime-function"></a><span data-ttu-id="eab28-103">Fonction DATETIME</span><span class="sxs-lookup"><span data-stu-id="eab28-103">DATETIME Function</span></span>

<span data-ttu-id="eab28-104">Renvoie la valeur de date et d'heure représentée par _DateHeure_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="eab28-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eab28-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eab28-105">Syntax</span></span>

<span data-ttu-id="eab28-106">DATETIME ("\* \* *DateTime* \* \*" | \* \* *expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="eab28-106">DATETIME(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eab28-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="eab28-107">Parameters</span></span>

|<span data-ttu-id="eab28-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="eab28-108">**Name**</span></span>|<span data-ttu-id="eab28-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="eab28-109">**Required/Optional**</span></span>|<span data-ttu-id="eab28-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="eab28-110">**Data Type**</span></span>|<span data-ttu-id="eab28-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="eab28-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eab28-112">_structure_</span><span class="sxs-lookup"><span data-stu-id="eab28-112">_datetime_</span></span> <br/> |<span data-ttu-id="eab28-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="eab28-113">Required</span></span>  <br/> |<span data-ttu-id="eab28-114">**String**</span><span class="sxs-lookup"><span data-stu-id="eab28-114">**String**</span></span> <br/> |<span data-ttu-id="eab28-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="eab28-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="eab28-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="eab28-116">_expression_</span></span> <br/> |<span data-ttu-id="eab28-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="eab28-117">Required</span></span>  <br/> |<span data-ttu-id="eab28-118">**String**</span><span class="sxs-lookup"><span data-stu-id="eab28-118">**String**</span></span> <br/> |<span data-ttu-id="eab28-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="eab28-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="eab28-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="eab28-120">_lcid_</span></span> <br/> |<span data-ttu-id="eab28-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="eab28-121">Optional</span></span>  <br/> |<span data-ttu-id="eab28-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="eab28-122">**Number**</span></span> <br/> |<span data-ttu-id="eab28-p101">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="eab28-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eab28-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="eab28-125">Return value</span></span>

<span data-ttu-id="eab28-126">Structure</span><span class="sxs-lookup"><span data-stu-id="eab28-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eab28-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="eab28-127">Remarks</span></span>

<span data-ttu-id="eab28-128">Si l'argument *DateHeure* est introuvable ou ne peut pas être interprété comme une date ou une heure valide, DateTime renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="eab28-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="eab28-129">«.</span><span class="sxs-lookup"><span data-stu-id="eab28-129">error.</span></span> 
  
<span data-ttu-id="eab28-130">La valeur renvoyée est formatée selon les formats d’heure et de date abrégés définis dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="eab28-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="eab28-131">La fonction DATETIME accepte également une valeur numérique simple pour *expression* où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899 et la partie décimale la fraction du jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="eab28-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="eab28-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="eab28-132">Example 1</span></span>

<span data-ttu-id="eab28-133">DATETIME("30 mai 1997") + 5 je.</span><span class="sxs-lookup"><span data-stu-id="eab28-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="eab28-134">Renvoie la valeur représentant le 04/06/97.</span><span class="sxs-lookup"><span data-stu-id="eab28-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="eab28-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="eab28-135">Example 2</span></span>

<span data-ttu-id="eab28-136">FORMAT(DATETIME("20/05/1997 14:30:45"), "C")</span><span class="sxs-lookup"><span data-stu-id="eab28-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="eab28-137">Renvoie la chaîne « mardi 20 mai 1997 14:30:45 ».</span><span class="sxs-lookup"><span data-stu-id="eab28-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="eab28-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="eab28-138">Example 3</span></span>

<span data-ttu-id="eab28-139">DATETIME("13:30 19 juillet")</span><span class="sxs-lookup"><span data-stu-id="eab28-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="eab28-140">Renvoie la valeur représentant 19/07/01 13:30 (en supposant que l’année actuelle soit 2001).</span><span class="sxs-lookup"><span data-stu-id="eab28-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="eab28-141">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="eab28-141">Example 4</span></span>

<span data-ttu-id="eab28-142">DATE ET HEURE (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="eab28-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="eab28-143">Renvoie la valeur représentant 30/05/97 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="eab28-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

