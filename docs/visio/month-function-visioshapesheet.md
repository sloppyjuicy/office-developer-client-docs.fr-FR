---
title: MONTH Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251467
localization_priority: Normal
ms.assetid: e099dbb3-c591-d934-5cfd-7728b10bd8dc
description: Renvoie un integer de 1 à 12 qui représente un mois.
ms.openlocfilehash: 71ecc7992839c871780e9b703377db37279246e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431973"
---
# <a name="month-function-visioshapesheet"></a><span data-ttu-id="33d71-103">MONTH Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="33d71-103">MONTH Function (VisioShapeSheet)</span></span>

<span data-ttu-id="33d71-104">Renvoie un integer de 1 à 12 qui représente un mois.</span><span class="sxs-lookup"><span data-stu-id="33d71-104">Returns an integer from 1 to 12 that represents a month.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="33d71-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="33d71-105">Syntax</span></span>

<span data-ttu-id="33d71-106">MONTH( » \*\* *datetime* \*\* « | \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="33d71-106">MONTH(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="33d71-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="33d71-107">Parameters</span></span>

|<span data-ttu-id="33d71-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="33d71-108">**Name**</span></span>|<span data-ttu-id="33d71-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="33d71-109">**Required/Optional**</span></span>|<span data-ttu-id="33d71-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="33d71-110">**Data Type**</span></span>|<span data-ttu-id="33d71-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="33d71-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="33d71-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="33d71-112">_datetime_</span></span> <br/> |<span data-ttu-id="33d71-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="33d71-113">Required</span></span>  <br/> |<span data-ttu-id="33d71-114">**String**</span><span class="sxs-lookup"><span data-stu-id="33d71-114">**String**</span></span> <br/> |<span data-ttu-id="33d71-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="33d71-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="33d71-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="33d71-116">_expression_</span></span> <br/> |<span data-ttu-id="33d71-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="33d71-117">Required</span></span>  <br/> |<span data-ttu-id="33d71-118">**String**</span><span class="sxs-lookup"><span data-stu-id="33d71-118">**String**</span></span> <br/> | <span data-ttu-id="33d71-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="33d71-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="33d71-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="33d71-120">_lcid_</span></span> <br/> |<span data-ttu-id="33d71-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="33d71-121">Optional</span></span>  <br/> |<span data-ttu-id="33d71-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="33d71-122">**Number**</span></span> <br/> |<span data-ttu-id="33d71-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="33d71-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="33d71-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="33d71-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="33d71-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="33d71-125">Return value</span></span>

<span data-ttu-id="33d71-126">Entier</span><span class="sxs-lookup"><span data-stu-id="33d71-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="33d71-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="33d71-127">Remarks</span></span>

<span data-ttu-id="33d71-128">Le composant d’heure  _de date/heure_  _ou d’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="33d71-128">The time component of  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="33d71-p102">Aucun arrondissement n’est effectué. Si la chaîne d’entrée est introuvable ou ne peut pas être convertie en un résultat valide, la fonction MONTH renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="33d71-p102">No rounding is done. If the input string is missing or cannot be converted to a valid result, the MONTH function returns an error.</span></span>
  
<span data-ttu-id="33d71-131">La valeur renvoyée est formatée selon le format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="33d71-131">The returned value is formatted according to the short date style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="33d71-132">La fonction MONTH accepte également une valeur de nombre unique pour  _l’expression,_ où la partie nombre inte du résultat représente le nombre de jours depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="33d71-132">The MONTH function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="33d71-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="33d71-133">Example 1</span></span>

<span data-ttu-id="33d71-134">MONTH("30 mai 1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="33d71-134">MONTH("May 30, 1999 13:45:24")</span></span>
  
<span data-ttu-id="33d71-135">Renvoie 5.</span><span class="sxs-lookup"><span data-stu-id="33d71-135">Returns 5.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="33d71-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="33d71-136">Example 2</span></span>

<span data-ttu-id="33d71-137">MONTH(VALEURDATE("30 mai 1999") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="33d71-137">MONTH(DATEVALUE("May 30, 1999")+7 ed.)</span></span>
  
<span data-ttu-id="33d71-138">Renvoie 6.</span><span class="sxs-lookup"><span data-stu-id="33d71-138">Returns 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="33d71-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="33d71-139">Example 3</span></span>

<span data-ttu-id="33d71-140">MONTH(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="33d71-140">MONTH(35580.6337)</span></span>
  
<span data-ttu-id="33d71-141">Renvoie 5.</span><span class="sxs-lookup"><span data-stu-id="33d71-141">Returns 5.</span></span>
  

