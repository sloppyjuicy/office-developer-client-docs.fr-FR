---
title: DAYOFYEAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251416
localization_priority: Normal
ms.assetid: 154d76a2-81f5-d8b1-b665-26dbae5da615
description: Renvoie une valeur de type Integer, comprise entre 1 et 366, qui représente le jour séquentiel de l'année dans dateheure ou expression. La fonction DAYOFYEAR utilise le calendrier grégorien.
ms.openlocfilehash: 30c0331a57282baee97e81689b6a8f362581b8f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360291"
---
# <a name="dayofyear-function"></a><span data-ttu-id="69752-104">Fonction DAYOFYEAR</span><span class="sxs-lookup"><span data-stu-id="69752-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="69752-105">Renvoie une valeur de type Integer, comprise entre 1 et 366, qui représente le jour séquentiel de l'année dans _DateHeure_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="69752-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="69752-106">La fonction DAYOFYEAR utilise le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="69752-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="69752-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="69752-107">Syntax</span></span>

<span data-ttu-id="69752-108">DAYOFYEAR ("\* \* *DateTime* \* \*" | \* \* *expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="69752-108">DAYOFYEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="69752-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="69752-109">Parameters</span></span>

|<span data-ttu-id="69752-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="69752-110">**Name**</span></span>|<span data-ttu-id="69752-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="69752-111">**Required/Optional**</span></span>|<span data-ttu-id="69752-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="69752-112">**Data Type**</span></span>|<span data-ttu-id="69752-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="69752-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="69752-114">_structure_</span><span class="sxs-lookup"><span data-stu-id="69752-114">_datetime_</span></span> <br/> |<span data-ttu-id="69752-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="69752-115">Required</span></span>  <br/> |<span data-ttu-id="69752-116">**String**</span><span class="sxs-lookup"><span data-stu-id="69752-116">**String**</span></span> <br/> |<span data-ttu-id="69752-117">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="69752-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="69752-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="69752-118">_expression_</span></span> <br/> |<span data-ttu-id="69752-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="69752-119">Required</span></span>  <br/> |<span data-ttu-id="69752-120">**String**</span><span class="sxs-lookup"><span data-stu-id="69752-120">**String**</span></span> <br/> |<span data-ttu-id="69752-121">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="69752-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="69752-122">_lcid_</span><span class="sxs-lookup"><span data-stu-id="69752-122">_lcid_</span></span> <br/> |<span data-ttu-id="69752-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="69752-123">Optional</span></span>  <br/> |<span data-ttu-id="69752-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="69752-124">**Number**</span></span> <br/> |<span data-ttu-id="69752-p103">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="69752-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="69752-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="69752-127">Return value</span></span>

<span data-ttu-id="69752-128">Entier</span><span class="sxs-lookup"><span data-stu-id="69752-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69752-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="69752-129">Remarks</span></span>

<span data-ttu-id="69752-130">Tous les composants d'heure dans _DateTime_ ou _expression_ ne sont pas pris en même temps.</span><span class="sxs-lookup"><span data-stu-id="69752-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="69752-131">Le résultat est compris entre le 1er janvier et le 31 décembre.</span><span class="sxs-lookup"><span data-stu-id="69752-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="69752-132">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="69752-132">No rounding is done.</span></span> <span data-ttu-id="69752-133">Si l'argument _DateHeure_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="69752-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="69752-134">La fonction DAYOFYEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="69752-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="69752-135">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="69752-135">Example 1</span></span>

<span data-ttu-id="69752-136">DAYOFYEAR("30 mai 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="69752-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="69752-137">Renvoie 150.</span><span class="sxs-lookup"><span data-stu-id="69752-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="69752-138">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="69752-138">Example 2</span></span>

<span data-ttu-id="69752-139">DAYOFYEAR(DATEVALUE("30 mai 1997") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="69752-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="69752-140">Renvoie 157.</span><span class="sxs-lookup"><span data-stu-id="69752-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="69752-141">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="69752-141">Example 3</span></span>

<span data-ttu-id="69752-142">DAYOFYEAR (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="69752-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="69752-143">Renvoie 150.</span><span class="sxs-lookup"><span data-stu-id="69752-143">Returns 150.</span></span>
  

