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
description: Renvoie un entier compris entre 1 et 7, représentant le jour de la semaine dans dateheure ou expression.
ms.openlocfilehash: 7c5d467d8c6ff14b99b64b8b0462d21d0b769998
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404805"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="40072-103">WEEKDAY Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="40072-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="40072-104">Renvoie un entier compris entre 1 et 7, représentant le jour de la semaine dans _DateHeure_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="40072-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="40072-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="40072-105">Syntax</span></span>

<span data-ttu-id="40072-106">WEEKDAY ("\* \* *DateTime* \* \*" | \* \* *expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="40072-106">WEEKDAY(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="40072-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="40072-107">Parameters</span></span>

|<span data-ttu-id="40072-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="40072-108">**Name**</span></span>|<span data-ttu-id="40072-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="40072-109">**Required/Optional**</span></span>|<span data-ttu-id="40072-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="40072-110">**Data Type**</span></span>|<span data-ttu-id="40072-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="40072-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="40072-112">_structure_</span><span class="sxs-lookup"><span data-stu-id="40072-112">_datetime_</span></span> <br/> |<span data-ttu-id="40072-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="40072-113">Required</span></span>  <br/> |<span data-ttu-id="40072-114">**String**</span><span class="sxs-lookup"><span data-stu-id="40072-114">**String**</span></span> <br/> | <span data-ttu-id="40072-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="40072-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="40072-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="40072-116">_expression_</span></span> <br/> |<span data-ttu-id="40072-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="40072-117">Required</span></span>  <br/> |<span data-ttu-id="40072-118">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="40072-118">**Varies**</span></span> <br/> |<span data-ttu-id="40072-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="40072-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="40072-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="40072-120">_lcid_</span></span> <br/> |<span data-ttu-id="40072-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="40072-121">Optional</span></span>  <br/> |<span data-ttu-id="40072-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="40072-122">**Numeric**</span></span> <br/> |<span data-ttu-id="40072-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="40072-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="40072-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="40072-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="40072-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="40072-125">Return value</span></span>

<span data-ttu-id="40072-126">Entier</span><span class="sxs-lookup"><span data-stu-id="40072-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="40072-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="40072-127">Remarks</span></span>

<span data-ttu-id="40072-128">Le composant heure de _DateTime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="40072-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="40072-129">Le résultat est compris entre lundi (1) et dimanche (7).</span><span class="sxs-lookup"><span data-stu-id="40072-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="40072-130">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="40072-130">No rounding is done.</span></span> <span data-ttu-id="40072-131">Si l'argument _DateHeure_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, la fonction renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="40072-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="40072-132">«.</span><span class="sxs-lookup"><span data-stu-id="40072-132">error.</span></span> 
  
<span data-ttu-id="40072-133">La fonction WEEKDAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="40072-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="40072-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="40072-134">Example 1</span></span>

<span data-ttu-id="40072-135">WEEKDAY("30 mai 1999")</span><span class="sxs-lookup"><span data-stu-id="40072-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="40072-136">Renvoie 7.</span><span class="sxs-lookup"><span data-stu-id="40072-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="40072-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="40072-137">Example 2</span></span>

<span data-ttu-id="40072-138">WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)</span><span class="sxs-lookup"><span data-stu-id="40072-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="40072-139">Renvoie 2.</span><span class="sxs-lookup"><span data-stu-id="40072-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="40072-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="40072-140">Example 3</span></span>

<span data-ttu-id="40072-141">JOUR DE LA SEMAINE (35880.6337)</span><span class="sxs-lookup"><span data-stu-id="40072-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="40072-142">Renvoie 4.</span><span class="sxs-lookup"><span data-stu-id="40072-142">Returns 4.</span></span>
  

