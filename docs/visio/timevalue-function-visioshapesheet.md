---
title: TimeValue, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251507
localization_priority: Normal
ms.assetid: 53579e0e-fcec-e745-0207-3861b5efa333
description: Renvoie la valeur d’heure représentée par dateheure ou expression, selon régionales votre système et linguistiques paramètres.
ms.openlocfilehash: e75607d19dc7062af717823c13f580cb44c9406b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789899"
---
# <a name="timevalue-function-visioshapesheet"></a><span data-ttu-id="b7333-103">TimeValue, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="b7333-103">TIMEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="b7333-104">Renvoie la valeur d’heure représentée par les _paramètres datetime_ ou _expression_, selon régionales votre système et linguistiques paramètres.</span><span class="sxs-lookup"><span data-stu-id="b7333-104">Returns the time value represented by  _datetime_ or  _expression_, based on the system's Region and Language settings.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="b7333-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b7333-105">Syntax</span></span>

<span data-ttu-id="b7333-106">TIMEVALUE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="b7333-106">TIMEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b7333-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b7333-107">Parameters</span></span>

|<span data-ttu-id="b7333-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="b7333-108">**Name**</span></span>|<span data-ttu-id="b7333-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="b7333-109">**Required/Optional**</span></span>|<span data-ttu-id="b7333-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="b7333-110">**Data Type**</span></span>|<span data-ttu-id="b7333-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="b7333-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b7333-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="b7333-112">_datetime_</span></span> <br/> |<span data-ttu-id="b7333-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7333-113">Required</span></span>  <br/> |<span data-ttu-id="b7333-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="b7333-114">**String**</span></span> <br/> | <span data-ttu-id="b7333-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="b7333-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="b7333-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="b7333-116">_expression_</span></span> <br/> |<span data-ttu-id="b7333-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="b7333-117">Required</span></span>  <br/> |<span data-ttu-id="b7333-118">**Varie**</span><span class="sxs-lookup"><span data-stu-id="b7333-118">**Varies**</span></span> <br/> | <span data-ttu-id="b7333-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="b7333-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="b7333-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="b7333-120">_lcid_</span></span> <br/> |<span data-ttu-id="b7333-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="b7333-121">Optional</span></span>  <br/> |<span data-ttu-id="b7333-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="b7333-122">**Number**</span></span> <br/> |<span data-ttu-id="b7333-p101">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="b7333-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b7333-125">Note</span><span class="sxs-lookup"><span data-stu-id="b7333-125">Remarks</span></span>

<span data-ttu-id="b7333-126">Le composant date de _datetime_ ou _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="b7333-126">Any date component in  _datetime_ or  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="b7333-127">Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, cette fonction renvoie une #VALUE !</span><span class="sxs-lookup"><span data-stu-id="b7333-127">If  _datetime_ is missing or cannot be converted to a valid result, this function returns a #VALUE!</span></span> <span data-ttu-id="b7333-128">erreur.</span><span class="sxs-lookup"><span data-stu-id="b7333-128">error.</span></span> 
  
<span data-ttu-id="b7333-129">La fonction TIMEVALUE accepte également une valeur numérique simple pour _expression_ où la partie décimale du résultat représente la fraction du jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="b7333-129">The TIMEVALUE function also accepts a single number value for  _expression_ where the decimal portion of the result represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b7333-130">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="b7333-130">Example 1</span></span>

<span data-ttu-id="b7333-131">TIMEVALUE("6:00")</span><span class="sxs-lookup"><span data-stu-id="b7333-131">TIMEVALUE("6:00 AM")</span></span>
  
<span data-ttu-id="b7333-132">Renvoie la valeur représentant 06:00:00.</span><span class="sxs-lookup"><span data-stu-id="b7333-132">Returns the value representing 6:00 AM.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b7333-133">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="b7333-133">Example 2</span></span>

<span data-ttu-id="b7333-134">TIMEVALUE("14:30") + 4 he.+ 30 me.</span><span class="sxs-lookup"><span data-stu-id="b7333-134">TIMEVALUE("14:30")+4 eh.+30 em.</span></span>
  
<span data-ttu-id="b7333-135">Renvoie la valeur représentant 19:00:00.</span><span class="sxs-lookup"><span data-stu-id="b7333-135">Returns the value representing 19:00:00.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b7333-136">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="b7333-136">Example 3</span></span>

<span data-ttu-id="b7333-137">TIMEVALUE("11 h, 1er juillet 1997")</span><span class="sxs-lookup"><span data-stu-id="b7333-137">TIMEVALUE("11 AM, July 1, 1997")</span></span>
  
<span data-ttu-id="b7333-138">Renvoie la valeur représentant 11:00:00.</span><span class="sxs-lookup"><span data-stu-id="b7333-138">Returns the value representing 11:00 AM.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="b7333-139">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="b7333-139">Example 4</span></span>

<span data-ttu-id="b7333-140">TIMEVALUE(0.6337)</span><span class="sxs-lookup"><span data-stu-id="b7333-140">TIMEVALUE(0.6337)</span></span>
  
<span data-ttu-id="b7333-141">Renvoie la valeur représentant 15:12:32.</span><span class="sxs-lookup"><span data-stu-id="b7333-141">Returns the value representing 15:12:32.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="b7333-142">Exemple 5</span><span class="sxs-lookup"><span data-stu-id="b7333-142">Example 5</span></span>

<span data-ttu-id="b7333-143">TIMEVALUE("7:89")</span><span class="sxs-lookup"><span data-stu-id="b7333-143">TIMEVALUE("7:89")</span></span>
  
<span data-ttu-id="b7333-p103">Renvoie une erreur #VALEUR!.</span><span class="sxs-lookup"><span data-stu-id="b7333-p103">Returns a #VALUE! error.</span></span>
  

