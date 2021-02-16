---
title: MINUTE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Renvoie un nombre integer entre 0 et 59 qui représente le composant minutes de date/heure ou d’expression .
ms.openlocfilehash: 35fe1dc8d4026dd6c829a38504d9ba82d64edda2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436565"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="7214c-103">MINUTE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="7214c-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="7214c-104">Renvoie un nombre integer entre 0 et 59 qui représente le composant minutes de  *date/heure*  ou  *d’expression*  .</span><span class="sxs-lookup"><span data-stu-id="7214c-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7214c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7214c-105">Syntax</span></span>

<span data-ttu-id="7214c-106">MINUTE( » *datetime*  « |  *expression*  [,  *lcid*  ])</span><span class="sxs-lookup"><span data-stu-id="7214c-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="7214c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7214c-107">Parameters</span></span>

|<span data-ttu-id="7214c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="7214c-108">**Name**</span></span>|<span data-ttu-id="7214c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="7214c-109">**Required/Optional**</span></span>|<span data-ttu-id="7214c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="7214c-110">**Data Type**</span></span>|<span data-ttu-id="7214c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7214c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="7214c-112">_datetime_</span><span class="sxs-lookup"><span data-stu-id="7214c-112">_datetime_</span></span> <br/> |<span data-ttu-id="7214c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7214c-113">Required</span></span>  <br/> |<span data-ttu-id="7214c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="7214c-114">**String**</span></span> <br/> |<span data-ttu-id="7214c-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="7214c-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="7214c-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="7214c-116">_expression_</span></span> <br/> |<span data-ttu-id="7214c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="7214c-117">Required</span></span>  <br/> |<span data-ttu-id="7214c-118">**String**</span><span class="sxs-lookup"><span data-stu-id="7214c-118">**String**</span></span> <br/> | <span data-ttu-id="7214c-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="7214c-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="7214c-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="7214c-120">_lcid_</span></span> <br/> |<span data-ttu-id="7214c-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="7214c-121">Optional</span></span>  <br/> |<span data-ttu-id="7214c-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="7214c-122">**Number**</span></span> <br/> |<span data-ttu-id="7214c-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="7214c-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="7214c-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="7214c-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="7214c-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="7214c-125">Return value</span></span>

<span data-ttu-id="7214c-126">Entier</span><span class="sxs-lookup"><span data-stu-id="7214c-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7214c-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="7214c-127">Remarks</span></span>

<span data-ttu-id="7214c-128">Le composant date dans  _l’heure et_  _l’expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7214c-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="7214c-129">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="7214c-129">No rounding is done.</span></span> <span data-ttu-id="7214c-130">Si  _la date/heure_ est manquante ou ne peut pas être convertie en un résultat valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="7214c-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="7214c-131">La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="7214c-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="7214c-132">La fonction MINUTE accepte également une valeur de nombre unique pour  _l’expression_ où la partie décimale représente la fraction d’un jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="7214c-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="7214c-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="7214c-133">Example 1</span></span>

<span data-ttu-id="7214c-134">MINUTE(« 7/7/1999 13:45:24 »)</span><span class="sxs-lookup"><span data-stu-id="7214c-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="7214c-135">Renvoie 45.</span><span class="sxs-lookup"><span data-stu-id="7214c-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="7214c-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="7214c-136">Example 2</span></span>

<span data-ttu-id="7214c-137">MINUTE(VALEURHEURE("25 janv. 1999 12:07:45") + 6 me.)</span><span class="sxs-lookup"><span data-stu-id="7214c-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="7214c-138">Renvoie 13.</span><span class="sxs-lookup"><span data-stu-id="7214c-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="7214c-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="7214c-139">Example 3</span></span>

<span data-ttu-id="7214c-140">MINUTE(0,575)</span><span class="sxs-lookup"><span data-stu-id="7214c-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="7214c-141">Renvoie 48.</span><span class="sxs-lookup"><span data-stu-id="7214c-141">Returns 48.</span></span>
  

