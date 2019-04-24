---
title: YEAR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Renvoie une valeur de type Integer qui représente l'année grégorienne dans DateTime ou expression, mise en forme selon le style de date abrégé défini par la région et les paramètres de langue actuels du système.
ms.openlocfilehash: c9bacd34557d365841171bee5c9f4683e6a3d296
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351652"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="a728c-103">YEAR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a728c-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a728c-104">Renvoie une valeur de type Integer qui représente l'année grégorienne dans _DateTime_ ou _expression_, mise en forme selon le style de date abrégé défini par la région et les paramètres de langue actuels du système.</span><span class="sxs-lookup"><span data-stu-id="a728c-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a728c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a728c-105">Syntax</span></span>

<span data-ttu-id="a728c-106">YEAR ("\* \* *DateTime* \* \*" | \* \* *expression* \* \* [, \* \* *LCID* \* \*])</span><span class="sxs-lookup"><span data-stu-id="a728c-106">YEAR(" \*\* *datetime* \*\* "| \*\* *expression* \*\* [, \*\* *lcid* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a728c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a728c-107">Parameters</span></span>

|<span data-ttu-id="a728c-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a728c-108">**Name**</span></span>|<span data-ttu-id="a728c-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a728c-109">**Required/Optional**</span></span>|<span data-ttu-id="a728c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a728c-110">**Data Type**</span></span>|<span data-ttu-id="a728c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a728c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a728c-112">_structure_</span><span class="sxs-lookup"><span data-stu-id="a728c-112">_datetime_</span></span> <br/> |<span data-ttu-id="a728c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a728c-113">Required</span></span>  <br/> |<span data-ttu-id="a728c-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a728c-114">**String**</span></span> <br/> | <span data-ttu-id="a728c-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="a728c-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a728c-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a728c-116">_expression_</span></span> <br/> |<span data-ttu-id="a728c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a728c-117">Required</span></span>  <br/> |<span data-ttu-id="a728c-118">**Réelle**</span><span class="sxs-lookup"><span data-stu-id="a728c-118">**Varies**</span></span> <br/> |<span data-ttu-id="a728c-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="a728c-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a728c-120">_lcid_</span><span class="sxs-lookup"><span data-stu-id="a728c-120">_lcid_</span></span> <br/> |<span data-ttu-id="a728c-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a728c-121">Optional</span></span>  <br/> |<span data-ttu-id="a728c-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a728c-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a728c-123">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale.</span><span class="sxs-lookup"><span data-stu-id="a728c-123">The locale identifier to be used in evaluating a nonlocal datetime.</span></span> <span data-ttu-id="a728c-124">L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="a728c-124">The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a728c-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a728c-125">Return value</span></span>

<span data-ttu-id="a728c-126">Entier</span><span class="sxs-lookup"><span data-stu-id="a728c-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a728c-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="a728c-127">Remarks</span></span>

<span data-ttu-id="a728c-128">Le composant heure de _DateTime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a728c-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a728c-129">Aucun arrondissement n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="a728c-129">No rounding is done.</span></span> <span data-ttu-id="a728c-130">Si l'argument _DateHeure_ est introuvable ou ne peut pas être interprété comme une date ou une heure valide, Year renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="a728c-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="a728c-131">La fonction YEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="a728c-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a728c-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a728c-132">Example 1</span></span>

<span data-ttu-id="a728c-133">YEAR ("10/27/2007 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="a728c-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="a728c-134">Renvoie 2007.</span><span class="sxs-lookup"><span data-stu-id="a728c-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a728c-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a728c-135">Example 2</span></span>

<span data-ttu-id="a728c-136">YEAR(VALEURDATE("25 déc. 2006") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="a728c-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="a728c-137">Renvoie 2007.</span><span class="sxs-lookup"><span data-stu-id="a728c-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a728c-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="a728c-138">Example 3</span></span>

<span data-ttu-id="a728c-139">ANNÉE (35580.6337)</span><span class="sxs-lookup"><span data-stu-id="a728c-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="a728c-140">Renvoie 1997.</span><span class="sxs-lookup"><span data-stu-id="a728c-140">Returns 1997.</span></span>
  

