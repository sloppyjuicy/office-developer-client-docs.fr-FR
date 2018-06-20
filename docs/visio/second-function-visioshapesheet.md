---
title: DEUXIÈME fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251495
localization_priority: Normal
ms.assetid: 22005976-37c0-d2be-8e34-8aee8458e4be
description: Renvoie un entier, 0 et 59, représentant le composant secondes de datetime ou expression.
ms.openlocfilehash: 5f0a3e87763bd4ea5436afe221e12477e9186356
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789600"
---
# <a name="second-function-visioshapesheet"></a><span data-ttu-id="a47ed-103">DEUXIÈME fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a47ed-103">SECOND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a47ed-104">Renvoie un entier, 0 et 59, représentant le composant secondes de _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="a47ed-104">Returns an integer, 0 to 59, that represents the seconds component of  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a47ed-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a47ed-105">Syntax</span></span>

<span data-ttu-id="a47ed-106">DEUXIÈME (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="a47ed-106">SECOND(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a47ed-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a47ed-107">Parameters</span></span>

|<span data-ttu-id="a47ed-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a47ed-108">**Name**</span></span>|<span data-ttu-id="a47ed-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a47ed-109">**Required/Optional**</span></span>|<span data-ttu-id="a47ed-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a47ed-110">**Data Type**</span></span>|<span data-ttu-id="a47ed-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a47ed-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a47ed-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="a47ed-112">_datetime_</span></span> <br/> |<span data-ttu-id="a47ed-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a47ed-113">Required</span></span>  <br/> |<span data-ttu-id="a47ed-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a47ed-114">**String**</span></span> <br/> |<span data-ttu-id="a47ed-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="a47ed-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a47ed-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a47ed-116">_expression_</span></span> <br/> |<span data-ttu-id="a47ed-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a47ed-117">Required</span></span>  <br/> |<span data-ttu-id="a47ed-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a47ed-118">**String**</span></span> <br/> | <span data-ttu-id="a47ed-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="a47ed-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a47ed-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="a47ed-120">_lcid_</span></span> <br/> |<span data-ttu-id="a47ed-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a47ed-121">Optional</span></span>  <br/> |<span data-ttu-id="a47ed-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a47ed-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a47ed-123">L’identificateur de paramètres régionaux à utiliser lors de l’évaluation non locaux _datetime_.</span><span class="sxs-lookup"><span data-stu-id="a47ed-123">The locale identifier to be used in evaluating a nonlocal  _datetime_.</span></span> <span data-ttu-id="a47ed-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête système.</span><span class="sxs-lookup"><span data-stu-id="a47ed-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a47ed-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a47ed-125">Return value</span></span>

<span data-ttu-id="a47ed-126">Entier</span><span class="sxs-lookup"><span data-stu-id="a47ed-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a47ed-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="a47ed-127">Remarks</span></span>

<span data-ttu-id="a47ed-128">Le composant date de _datetime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a47ed-128">The date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a47ed-129">Aucun arrondi n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="a47ed-129">No rounding is done.</span></span> <span data-ttu-id="a47ed-130">Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, cette fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="a47ed-130">If  _datetime_ is missing or cannot be converted to a valid result, this function returns an error.</span></span> 
  
<span data-ttu-id="a47ed-131">La fonction SECOND accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="a47ed-131">The SECOND function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a47ed-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a47ed-132">Example 1</span></span>

<span data-ttu-id="a47ed-133">SECOND("30/05/1997 13:45:32")</span><span class="sxs-lookup"><span data-stu-id="a47ed-133">SECOND("05/30/1997 13:45:32")</span></span>
  
<span data-ttu-id="a47ed-134">Renvoie 32.</span><span class="sxs-lookup"><span data-stu-id="a47ed-134">Returns 32.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a47ed-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a47ed-135">Example 2</span></span>

<span data-ttu-id="a47ed-136">SECOND(TIMEVALUE("30 mai 1996 12:07:45") + 7 se.)</span><span class="sxs-lookup"><span data-stu-id="a47ed-136">SECOND(TIMEVALUE("May 30, 1996 12:07:45") + 7 es.)</span></span>
  
<span data-ttu-id="a47ed-137">Renvoie 52.</span><span class="sxs-lookup"><span data-stu-id="a47ed-137">Returns 52.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a47ed-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="a47ed-138">Example 3</span></span>

<span data-ttu-id="a47ed-139">SECOND(0.6337)</span><span class="sxs-lookup"><span data-stu-id="a47ed-139">SECOND(0.6337)</span></span>
  
<span data-ttu-id="a47ed-140">Renvoie 32.</span><span class="sxs-lookup"><span data-stu-id="a47ed-140">Returns 32.</span></span>
  

