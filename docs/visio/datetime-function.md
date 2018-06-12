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
description: Renvoie la date et l’heure représentées par les paramètres datetime ou expression.
ms.openlocfilehash: 001430acaf9fcb670e95157380e474e12b9728cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788431"
---
# <a name="datetime-function"></a><span data-ttu-id="e0feb-103">DATETIME, fonction</span><span class="sxs-lookup"><span data-stu-id="e0feb-103">DATETIME Function</span></span>

<span data-ttu-id="e0feb-104">Renvoie la date et l’heure représentées par les _paramètres datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="e0feb-104">Returns the date and time value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e0feb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e0feb-105">Syntax</span></span>

<span data-ttu-id="e0feb-106">DATETIME (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="e0feb-106">DATETIME(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e0feb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e0feb-107">Parameters</span></span>

|<span data-ttu-id="e0feb-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e0feb-108">**Name**</span></span>|<span data-ttu-id="e0feb-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e0feb-109">**Required/Optional**</span></span>|<span data-ttu-id="e0feb-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e0feb-110">**Data Type**</span></span>|<span data-ttu-id="e0feb-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e0feb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e0feb-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="e0feb-112">_datetime_</span></span> <br/> |<span data-ttu-id="e0feb-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e0feb-113">Required</span></span>  <br/> |<span data-ttu-id="e0feb-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0feb-114">**String**</span></span> <br/> |<span data-ttu-id="e0feb-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="e0feb-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="e0feb-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="e0feb-116">_expression_</span></span> <br/> |<span data-ttu-id="e0feb-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e0feb-117">Required</span></span>  <br/> |<span data-ttu-id="e0feb-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="e0feb-118">**String**</span></span> <br/> |<span data-ttu-id="e0feb-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="e0feb-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="e0feb-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="e0feb-120">_lcid_</span></span> <br/> |<span data-ttu-id="e0feb-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e0feb-121">Optional</span></span>  <br/> |<span data-ttu-id="e0feb-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="e0feb-122">**Number**</span></span> <br/> |<span data-ttu-id="e0feb-p101">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="e0feb-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e0feb-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="e0feb-125">Return value</span></span>

<span data-ttu-id="e0feb-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="e0feb-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0feb-127">Note</span><span class="sxs-lookup"><span data-stu-id="e0feb-127">Remarks</span></span>

<span data-ttu-id="e0feb-128">Si *datetime* est introuvable ou ne peut pas être interprété comme une date ou heure valide, DATETIME renvoie une #VALUE !</span><span class="sxs-lookup"><span data-stu-id="e0feb-128">If  *datetime*  is missing or cannot be interpreted as a valid date or time, DATETIME returns a #VALUE!</span></span> <span data-ttu-id="e0feb-129">erreur.</span><span class="sxs-lookup"><span data-stu-id="e0feb-129">error.</span></span> 
  
<span data-ttu-id="e0feb-130">La valeur renvoyée est formatée selon les formats d’heure et de date abrégés définis dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="e0feb-130">The returned value is formatted according to the short date style and time style in the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="e0feb-131">La fonction DATETIME accepte également une valeur numérique simple pour *expression* où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899 et la partie décimale représente la fraction du jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="e0feb-131">The DATETIME function also accepts a single number value for  *expression*  where the integer portion of the result represents the number of days since December 30, 1899, and the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e0feb-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e0feb-132">Example 1</span></span>

<span data-ttu-id="e0feb-133">DATETIME("30 mai 1997") + 5 je.</span><span class="sxs-lookup"><span data-stu-id="e0feb-133">DATETIME("May 30, 1997")+5 ed.</span></span>
  
<span data-ttu-id="e0feb-134">Renvoie la valeur représentant le 04/06/97.</span><span class="sxs-lookup"><span data-stu-id="e0feb-134">Returns the value representing 6/4/1997.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e0feb-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e0feb-135">Example 2</span></span>

<span data-ttu-id="e0feb-136">FORMAT(DATETIME("20/05/1997 14:30:45"), "C")</span><span class="sxs-lookup"><span data-stu-id="e0feb-136">FORMAT(DATETIME("5/20/1997 14:30:45"),"C")</span></span>
  
<span data-ttu-id="e0feb-137">Renvoie la chaîne « mardi 20 mai 1997 14:30:45 ».</span><span class="sxs-lookup"><span data-stu-id="e0feb-137">Returns the string "Tuesday, May 20, 1997 2:30:45 PM."</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e0feb-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e0feb-138">Example 3</span></span>

<span data-ttu-id="e0feb-139">DATETIME("13:30 19 juillet")</span><span class="sxs-lookup"><span data-stu-id="e0feb-139">DATETIME("1:30 PM July 19")</span></span>
  
<span data-ttu-id="e0feb-140">Renvoie la valeur représentant 19/07/01 13:30 (en supposant que l’année actuelle soit 2001).</span><span class="sxs-lookup"><span data-stu-id="e0feb-140">Returns the value representing 7/19/2001 1:30:00 PM (assuming the current year is 2001).</span></span>
  
## <a name="example-4"></a><span data-ttu-id="e0feb-141">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="e0feb-141">Example 4</span></span>

<span data-ttu-id="e0feb-142">DATETIME(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="e0feb-142">DATETIME(35580.6337)</span></span>
  
<span data-ttu-id="e0feb-143">Renvoie la valeur représentant 30/05/97 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="e0feb-143">Returns the value representing 5/30/1997 3:12:32 PM.</span></span>
  

