---
title: YEAR, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251513
localization_priority: Normal
ms.assetid: acc136ef-9946-7c12-a467-9ded732a3549
description: Renvoie un entier représentant l’année grégorien de datetime ou expression, la mise en forme selon le style de format de date abrégée défini par les paramètres de langue et de région actuelles du système.
ms.openlocfilehash: aaa183730440857d8d283912f4afeb3117ef737f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790092"
---
# <a name="year-function-visioshapesheet"></a><span data-ttu-id="105da-103">YEAR, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="105da-103">YEAR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="105da-104">Renvoie un entier représentant l’année grégorien dans _datetime_ ou _expression de_mise en forme selon le style de format de date abrégée défini par les paramètres de langue et de région actuelles du système.</span><span class="sxs-lookup"><span data-stu-id="105da-104">Returns an integer that represents the Gregorian year in  _datetime_ or  _expression_, formatted according to the short date style set by the system's current Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="105da-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="105da-105">Syntax</span></span>

<span data-ttu-id="105da-106">ANNÉE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="105da-106">YEAR(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="105da-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="105da-107">Parameters</span></span>

|<span data-ttu-id="105da-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="105da-108">**Name**</span></span>|<span data-ttu-id="105da-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="105da-109">**Required/Optional**</span></span>|<span data-ttu-id="105da-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="105da-110">**Data Type**</span></span>|<span data-ttu-id="105da-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="105da-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="105da-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="105da-112">_datetime_</span></span> <br/> |<span data-ttu-id="105da-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="105da-113">Required</span></span>  <br/> |<span data-ttu-id="105da-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="105da-114">**String**</span></span> <br/> | <span data-ttu-id="105da-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="105da-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="105da-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="105da-116">_expression_</span></span> <br/> |<span data-ttu-id="105da-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="105da-117">Required</span></span>  <br/> |<span data-ttu-id="105da-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="105da-118">**Varies**</span></span> <br/> |<span data-ttu-id="105da-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="105da-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="105da-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="105da-120">_lcid_</span></span> <br/> |<span data-ttu-id="105da-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="105da-121">Optional</span></span>  <br/> |<span data-ttu-id="105da-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="105da-122">**Numeric**</span></span> <br/> |<span data-ttu-id="105da-p101">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="105da-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="105da-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="105da-125">Return value</span></span>

<span data-ttu-id="105da-126">Entier</span><span class="sxs-lookup"><span data-stu-id="105da-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="105da-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="105da-127">Remarks</span></span>

<span data-ttu-id="105da-128">Le composant heure de _datetime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="105da-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="105da-129">Aucun arrondi n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="105da-129">No rounding is done.</span></span> <span data-ttu-id="105da-130">Si _datetime_ est introuvable ou ne peut pas être interprété comme une date valide ou une heure, année renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="105da-130">If  _datetime_ is missing or cannot be interpreted as a valid date or time, YEAR returns an error.</span></span> 
  
<span data-ttu-id="105da-131">La fonction YEAR accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="105da-131">The YEAR function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="105da-132">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="105da-132">Example 1</span></span>

<span data-ttu-id="105da-133">YEAR("27/10/2007 13:45:24 PM")</span><span class="sxs-lookup"><span data-stu-id="105da-133">YEAR("10/27/2007 13:45:24")</span></span>
  
<span data-ttu-id="105da-134">Renvoie 2007.</span><span class="sxs-lookup"><span data-stu-id="105da-134">Returns 2007.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="105da-135">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="105da-135">Example 2</span></span>

<span data-ttu-id="105da-136">YEAR(VALEURDATE("25 déc. 2006") + 7 je.)</span><span class="sxs-lookup"><span data-stu-id="105da-136">YEAR(DATEVALUE("Dec. 25, 2006") + 7 ed.)</span></span>
  
<span data-ttu-id="105da-137">Renvoie 2007.</span><span class="sxs-lookup"><span data-stu-id="105da-137">Returns 2007.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="105da-138">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="105da-138">Example 3</span></span>

<span data-ttu-id="105da-139">YEAR(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="105da-139">YEAR(35580.6337)</span></span>
  
<span data-ttu-id="105da-140">Renvoie 1997.</span><span class="sxs-lookup"><span data-stu-id="105da-140">Returns 1997.</span></span>
  

