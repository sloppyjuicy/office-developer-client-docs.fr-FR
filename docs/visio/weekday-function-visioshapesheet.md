---
title: WEEKDAY, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251512
localization_priority: Normal
ms.assetid: f2625ef8-3bdb-5a8d-48b9-149be0592533
description: Renvoie un entier, de 1 à 7, représentant le jour de datetime ou expression.
ms.openlocfilehash: decc89c93d175b357cdfe2b8377d04517b92ccab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790035"
---
# <a name="weekday-function-visioshapesheet"></a><span data-ttu-id="a0c31-103">WEEKDAY, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a0c31-103">WEEKDAY Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a0c31-104">Renvoie un entier, de 1 à 7, représentant le jour de la semaine dans _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="a0c31-104">Returns an integer, 1 to 7, representing the weekday in  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a0c31-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a0c31-105">Syntax</span></span>

<span data-ttu-id="a0c31-106">WEEKDAY (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="a0c31-106">WEEKDAY(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a0c31-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a0c31-107">Parameters</span></span>

|<span data-ttu-id="a0c31-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="a0c31-108">**Name**</span></span>|<span data-ttu-id="a0c31-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a0c31-109">**Required/Optional**</span></span>|<span data-ttu-id="a0c31-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a0c31-110">**Data Type**</span></span>|<span data-ttu-id="a0c31-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a0c31-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a0c31-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="a0c31-112">_datetime_</span></span> <br/> |<span data-ttu-id="a0c31-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a0c31-113">Required</span></span>  <br/> |<span data-ttu-id="a0c31-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="a0c31-114">**String**</span></span> <br/> | <span data-ttu-id="a0c31-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="a0c31-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="a0c31-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="a0c31-116">_expression_</span></span> <br/> |<span data-ttu-id="a0c31-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a0c31-117">Required</span></span>  <br/> |<span data-ttu-id="a0c31-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="a0c31-118">**Varies**</span></span> <br/> |<span data-ttu-id="a0c31-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="a0c31-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="a0c31-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="a0c31-120">_lcid_</span></span> <br/> |<span data-ttu-id="a0c31-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a0c31-121">Optional</span></span>  <br/> |<span data-ttu-id="a0c31-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a0c31-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a0c31-p101">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="a0c31-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a0c31-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="a0c31-125">Return value</span></span>

<span data-ttu-id="a0c31-126">Entier</span><span class="sxs-lookup"><span data-stu-id="a0c31-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0c31-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="a0c31-127">Remarks</span></span>

<span data-ttu-id="a0c31-128">Le composant heure de _datetime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="a0c31-128">The time component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="a0c31-129">Le résultat correspond au lundi (1) et dimanche (7).</span><span class="sxs-lookup"><span data-stu-id="a0c31-129">The result corresponds to Monday (1) through Sunday (7).</span></span> <span data-ttu-id="a0c31-130">Aucun arrondi n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="a0c31-130">No rounding is done.</span></span> <span data-ttu-id="a0c31-131">Si _datetime_ est introuvable ou ne peut pas être interprété comme une date ou heure valide, la fonction retourne un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="a0c31-131">If  _datetime_ is missing or cannot be interpreted as a valid date or time, the function returns a #VALUE!</span></span> <span data-ttu-id="a0c31-132">erreur.</span><span class="sxs-lookup"><span data-stu-id="a0c31-132">error.</span></span> 
  
<span data-ttu-id="a0c31-133">La fonction WEEKDAY accepte également une valeur numérique simple pour _expression_ où la partie entière du résultat représente le nombre de jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="a0c31-133">The WEEKDAY function also accepts a single number value for  _expression_ where the integer portion of the result represents the number of days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="a0c31-134">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a0c31-134">Example 1</span></span>

<span data-ttu-id="a0c31-135">WEEKDAY("30 mai 1999")</span><span class="sxs-lookup"><span data-stu-id="a0c31-135">WEEKDAY("May 30, 1999")</span></span>
  
<span data-ttu-id="a0c31-136">Renvoie 7.</span><span class="sxs-lookup"><span data-stu-id="a0c31-136">Returns 7.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a0c31-137">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a0c31-137">Example 2</span></span>

<span data-ttu-id="a0c31-138">WEEKDAY(VALEURDATE("30 mai 1999") + 2 je.)</span><span class="sxs-lookup"><span data-stu-id="a0c31-138">WEEKDAY(DATEVALUE("May 30, 1999")+2 ed.)</span></span>
  
<span data-ttu-id="a0c31-139">Renvoie 2.</span><span class="sxs-lookup"><span data-stu-id="a0c31-139">Returns 2.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a0c31-140">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="a0c31-140">Example 3</span></span>

<span data-ttu-id="a0c31-141">WEEKDAY(35880.6337)</span><span class="sxs-lookup"><span data-stu-id="a0c31-141">WEEKDAY(35880.6337)</span></span>
  
<span data-ttu-id="a0c31-142">Renvoie 4.</span><span class="sxs-lookup"><span data-stu-id="a0c31-142">Returns 4.</span></span>
  

