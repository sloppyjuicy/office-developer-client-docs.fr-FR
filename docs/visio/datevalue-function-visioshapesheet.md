---
title: DATEVALUE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Renvoie la valeur de date représentée par datetime ou expression.
ms.openlocfilehash: d5bc1865e76940508ddb67a9b3d2122dc7c43a50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360311"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="65330-103">DATEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="65330-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="65330-104">Renvoie la valeur de date représentée par  _datetime_ ou  _expression_.</span><span class="sxs-lookup"><span data-stu-id="65330-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="65330-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65330-105">Syntax</span></span>

<span data-ttu-id="65330-106">DATEVALUE( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="65330-106">DATEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="65330-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65330-107">Parameters</span></span>

|<span data-ttu-id="65330-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="65330-108">**Name**</span></span>|<span data-ttu-id="65330-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="65330-109">**Required/Optional**</span></span>|<span data-ttu-id="65330-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="65330-110">**Data Type**</span></span>|<span data-ttu-id="65330-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="65330-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="65330-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="65330-112">_datetime_</span></span> <br/> |<span data-ttu-id="65330-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="65330-113">Required</span></span>  <br/> |<span data-ttu-id="65330-114">**String**</span><span class="sxs-lookup"><span data-stu-id="65330-114">**String**</span></span> <br/> |<span data-ttu-id="65330-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="65330-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="65330-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="65330-116">_expression_</span></span> <br/> |<span data-ttu-id="65330-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="65330-117">Required</span></span>  <br/> |<span data-ttu-id="65330-118">**String**</span><span class="sxs-lookup"><span data-stu-id="65330-118">**String**</span></span> <br/> |<span data-ttu-id="65330-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="65330-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="65330-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="65330-120">_lcid_</span></span> <br/> |<span data-ttu-id="65330-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="65330-121">Optional</span></span>  <br/> |<span data-ttu-id="65330-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="65330-122">**Number**</span></span> <br/> |<span data-ttu-id="65330-p101">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="65330-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="65330-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="65330-125">Return value</span></span>

<span data-ttu-id="65330-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="65330-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="65330-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="65330-127">Remarks</span></span>

<span data-ttu-id="65330-128">Tout composant d’heure  *dans l’heure ou*  *l’expression*  est ignoré.</span><span class="sxs-lookup"><span data-stu-id="65330-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="65330-129">Si  *date/heure*  est manquante ou ne peut pas être convertie en un résultat valide, DATEVALUE renvoie une valeur #VALUE!</span><span class="sxs-lookup"><span data-stu-id="65330-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="65330-130">erreur.</span><span class="sxs-lookup"><span data-stu-id="65330-130">error.</span></span> 
  
<span data-ttu-id="65330-131">La valeur renvoyée s’affiche au format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="65330-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="65330-132">La fonction DATEVALUE accepte également une valeur de nombre unique pour  *l’expression,*  où la partie nombre inte du résultat représente les jours depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="65330-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="65330-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="65330-133">Example 1</span></span>

<span data-ttu-id="65330-134">DATEVALUE(NOW( )) + 5 je.</span><span class="sxs-lookup"><span data-stu-id="65330-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="65330-135">Renvoie la date actuelle augmentée de cinq jours.</span><span class="sxs-lookup"><span data-stu-id="65330-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="65330-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="65330-136">Example 2</span></span>

<span data-ttu-id="65330-137">DATEVALUE(« 19/07/1995 12:30 »)</span><span class="sxs-lookup"><span data-stu-id="65330-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="65330-138">Renvoie la date.</span><span class="sxs-lookup"><span data-stu-id="65330-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="65330-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="65330-139">Example 3</span></span>

<span data-ttu-id="65330-140">DATEVALUE("33 mai 1997")</span><span class="sxs-lookup"><span data-stu-id="65330-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="65330-p103">Renvoie une erreur #VALEUR!.</span><span class="sxs-lookup"><span data-stu-id="65330-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="65330-143">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="65330-143">Example 4</span></span>

<span data-ttu-id="65330-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="65330-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="65330-145">Renvoie le 30/05/97.</span><span class="sxs-lookup"><span data-stu-id="65330-145">Returns 5/30/1997.</span></span>
  

