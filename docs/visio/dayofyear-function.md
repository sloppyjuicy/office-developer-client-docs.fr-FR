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
description: Renvoie un entier, de 1 à 366 qui représente le jour de l’année de datetime ou expression. La fonction DAYOFYEAR utilise le calendrier grégorien.
ms.openlocfilehash: 2fd80a2554c268d276deaa524a9d98eebc6a48d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788454"
---
# <a name="dayofyear-function"></a><span data-ttu-id="dd0a6-104">DAYOFYEAR, fonction</span><span class="sxs-lookup"><span data-stu-id="dd0a6-104">DAYOFYEAR Function</span></span>

<span data-ttu-id="dd0a6-105">Renvoie un entier, de 1 à 366 qui représente le jour de l’année dans les _paramètres datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-105">Returns an integer, 1 to 366, that represents the sequential day of the year in  _datetime_ or  _expression_.</span></span> <span data-ttu-id="dd0a6-106">La fonction DAYOFYEAR utilise le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-106">The DAYOFYEAR function uses the Gregorian calendar.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dd0a6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd0a6-107">Syntax</span></span>

<span data-ttu-id="dd0a6-108">DAYOFYEAR (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="dd0a6-108">DAYOFYEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dd0a6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dd0a6-109">Parameters</span></span>

|<span data-ttu-id="dd0a6-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-110">**Name**</span></span>|<span data-ttu-id="dd0a6-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-111">**Required/Optional**</span></span>|<span data-ttu-id="dd0a6-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-112">**Data Type**</span></span>|<span data-ttu-id="dd0a6-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dd0a6-114">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="dd0a6-114">_datetime_</span></span> <br/> |<span data-ttu-id="dd0a6-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dd0a6-115">Required</span></span>  <br/> |<span data-ttu-id="dd0a6-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-116">**String**</span></span> <br/> |<span data-ttu-id="dd0a6-117">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-117">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="dd0a6-118">_expression_</span><span class="sxs-lookup"><span data-stu-id="dd0a6-118">_expression_</span></span> <br/> |<span data-ttu-id="dd0a6-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="dd0a6-119">Required</span></span>  <br/> |<span data-ttu-id="dd0a6-120">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-120">**String**</span></span> <br/> |<span data-ttu-id="dd0a6-121">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-121">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="dd0a6-122">_LCID_</span><span class="sxs-lookup"><span data-stu-id="dd0a6-122">_lcid_</span></span> <br/> |<span data-ttu-id="dd0a6-123">Facultatif</span><span class="sxs-lookup"><span data-stu-id="dd0a6-123">Optional</span></span>  <br/> |<span data-ttu-id="dd0a6-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="dd0a6-124">**Number**</span></span> <br/> |<span data-ttu-id="dd0a6-p103">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-p103">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dd0a6-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="dd0a6-127">Return value</span></span>

<span data-ttu-id="dd0a6-128">Entier</span><span class="sxs-lookup"><span data-stu-id="dd0a6-128">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dd0a6-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="dd0a6-129">Remarks</span></span>

<span data-ttu-id="dd0a6-130">Les composants d’heure figurant dans _datetime_ ou _expression_ sont ignoré.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-130">Any time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="dd0a6-131">Le résultat correspond au 1er janvier au 31 décembre.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-131">The result corresponds to January 1 to December 31.</span></span> <span data-ttu-id="dd0a6-132">Aucun arrondi n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-132">No rounding is done.</span></span> <span data-ttu-id="dd0a6-133">Si _datetime_ est introuvable ou ne peut pas être interprété comme une date ou heure valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-133">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns an error.</span></span> 
  
<span data-ttu-id="dd0a6-134">La fonction DAYOFYEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-134">The DAYOFYEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dd0a6-135">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="dd0a6-135">Example 1</span></span>

<span data-ttu-id="dd0a6-136">DAYOFYEAR("30 mai 1997 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="dd0a6-136">DAYOFYEAR("May 30, 1997 13:45:24")</span></span>
  
<span data-ttu-id="dd0a6-137">Renvoie 150.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-137">Returns 150.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dd0a6-138">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="dd0a6-138">Example 2</span></span>

<span data-ttu-id="dd0a6-139">DAYOFYEAR(DATEVALUE("30 mai 1997") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="dd0a6-139">DAYOFYEAR(DATEVALUE("May 30, 1997")+7 ed.)</span></span>
  
<span data-ttu-id="dd0a6-140">Renvoie 157.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-140">Returns 157.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dd0a6-141">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="dd0a6-141">Example 3</span></span>

<span data-ttu-id="dd0a6-142">DAYOFYEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="dd0a6-142">DAYOFYEAR(35580.6337)</span></span>
  
<span data-ttu-id="dd0a6-143">Renvoie 150.</span><span class="sxs-lookup"><span data-stu-id="dd0a6-143">Returns 150.</span></span>
  

