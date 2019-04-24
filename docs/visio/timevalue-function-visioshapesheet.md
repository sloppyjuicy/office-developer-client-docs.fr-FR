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
description: Renvoie la valeur de temps représentée par dateheure ou expression, en fonction de la région et des paramètres de langue du système.
ms.openlocfilehash: 61eeafac64ce199eba0f9032c42474d2b44febce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361109"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="e6cd5-103">TIMEVALUE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="e6cd5-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="e6cd5-104">Renvoie la valeur de temps représentée par _DateHeure_ ou _expression_, en fonction de la région et des paramètres de langue du système.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e6cd5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6cd5-105">Syntax</span></span>

<span data-ttu-id="e6cd5-106">TIMEVALUE ("\* \* *DateTime* \* \*" | \* \* *expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="e6cd5-106">TIMEVALUE(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e6cd5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6cd5-107">Parameters</span></span>

|<span data-ttu-id="e6cd5-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-108">**Name**</span></span>|<span data-ttu-id="e6cd5-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-109">**Required/Optional**</span></span>|<span data-ttu-id="e6cd5-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-110">**Data Type**</span></span>|<span data-ttu-id="e6cd5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e6cd5-112">_structure_</span><span class="sxs-lookup"><span data-stu-id="e6cd5-112">_datetime_</span></span> <br/> |<span data-ttu-id="e6cd5-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6cd5-113">Required</span></span>  <br/> |<span data-ttu-id="e6cd5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-114">**String**</span></span> <br/> | <span data-ttu-id="e6cd5-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="e6cd5-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="e6cd5-116">_expression_</span></span> <br/> |<span data-ttu-id="e6cd5-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e6cd5-117">Required</span></span>  <br/> |<span data-ttu-id="e6cd5-118">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-118">**Varies**</span></span> <br/> | <span data-ttu-id="e6cd5-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="e6cd5-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="e6cd5-120">_lcid_</span></span> <br/> |<span data-ttu-id="e6cd5-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="e6cd5-121">Optional</span></span>  <br/> |<span data-ttu-id="e6cd5-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="e6cd5-122">**Number**</span></span> <br/> |<span data-ttu-id="e6cd5-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="e6cd5-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6cd5-125">Remarques</span><span class="sxs-lookup"><span data-stu-id="e6cd5-125">Remarks</span></span>

<span data-ttu-id="e6cd5-126">Tout composant date dans _DateTime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="e6cd5-127">Si l'argument _DateHeure_ est introuvable ou ne peut pas être converti en un résultat valide, cette fonction renvoie une #VALUE!</span><span class="sxs-lookup"><span data-stu-id="e6cd5-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="e6cd5-128">«.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-128">error.</span></span> 
  
<span data-ttu-id="e6cd5-129">La fonction TIMEVALUE accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e6cd5-130">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="e6cd5-130">Example 1</span></span>

<span data-ttu-id="e6cd5-131">TIMEVALUE("6:00")</span><span class="sxs-lookup"><span data-stu-id="e6cd5-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="e6cd5-132">Renvoie la valeur représentant 06:00:00.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e6cd5-133">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="e6cd5-133">Example 2</span></span>

<span data-ttu-id="e6cd5-134">TIMEVALUE("14:30") + 4 he.+ 30 me.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="e6cd5-135">Renvoie la valeur représentant 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e6cd5-136">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="e6cd5-136">Example 3</span></span>

<span data-ttu-id="e6cd5-137">TIMEVALUE("11 h, 1er juillet 1997")</span><span class="sxs-lookup"><span data-stu-id="e6cd5-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="e6cd5-138">Renvoie la valeur représentant 11:00:00.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="e6cd5-139">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="e6cd5-139">Example 4</span></span>

<span data-ttu-id="e6cd5-140">TIMEVALUE (0.6337)</span><span class="sxs-lookup"><span data-stu-id="e6cd5-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="e6cd5-141">Renvoie la valeur représentant 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="e6cd5-142">Exemple 5</span><span class="sxs-lookup"><span data-stu-id="e6cd5-142">Example 5</span></span>

<span data-ttu-id="e6cd5-143">TIMEVALUE ("7:89")</span><span class="sxs-lookup"><span data-stu-id="e6cd5-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="e6cd5-p103">Renvoie une erreur #VALEUR!.</span><span class="sxs-lookup"><span data-stu-id="e6cd5-p103">Returns a #VALUE! error.</span></span>
  

