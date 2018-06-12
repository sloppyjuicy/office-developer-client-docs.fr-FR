---
title: DATEVALUE, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251414
localization_priority: Normal
ms.assetid: 514a4053-7729-ec82-c42f-5b780e48cd2a
description: Renvoie la valeur de date représentée par datetime ou expression.
ms.openlocfilehash: 7fcfd625b5e4e3da71a1b160c074401b672e0be7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788429"
---
# <a name="datevalue-function-visioshapesheet"></a><span data-ttu-id="67272-103">DATEVALUE, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="67272-103">DATEVALUE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="67272-104">Renvoie la valeur de date représentée par _datetime_ ou _expression_.</span><span class="sxs-lookup"><span data-stu-id="67272-104">Returns the date value represented by  _datetime_ or  _expression_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="67272-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67272-105">Syntax</span></span>

<span data-ttu-id="67272-106">DATEVALUE (« ** *datetime* ** » | ** *expression* ** [, ** *lcid* **])</span><span class="sxs-lookup"><span data-stu-id="67272-106">DATEVALUE(" ** *datetime* ** "| ** *expression* ** [, ** *lcid* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="67272-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67272-107">Parameters</span></span>

|<span data-ttu-id="67272-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="67272-108">**Name**</span></span>|<span data-ttu-id="67272-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="67272-109">**Required/Optional**</span></span>|<span data-ttu-id="67272-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="67272-110">**Data Type**</span></span>|<span data-ttu-id="67272-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="67272-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="67272-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="67272-112">_datetime_</span></span> <br/> |<span data-ttu-id="67272-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="67272-113">Required</span></span>  <br/> |<span data-ttu-id="67272-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="67272-114">**String**</span></span> <br/> |<span data-ttu-id="67272-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="67272-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="67272-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="67272-116">_expression_</span></span> <br/> |<span data-ttu-id="67272-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="67272-117">Required</span></span>  <br/> |<span data-ttu-id="67272-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="67272-118">**String**</span></span> <br/> |<span data-ttu-id="67272-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="67272-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="67272-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="67272-120">_lcid_</span></span> <br/> |<span data-ttu-id="67272-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="67272-121">Optional</span></span>  <br/> |<span data-ttu-id="67272-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="67272-122">**Number**</span></span> <br/> |<span data-ttu-id="67272-p101">Spécifie l’identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="67272-p101">Specifies the locale identifier to be used in evaluating a non-local datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="67272-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="67272-125">Return value</span></span>

<span data-ttu-id="67272-126">Datetime</span><span class="sxs-lookup"><span data-stu-id="67272-126">Datetime</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67272-127">Note</span><span class="sxs-lookup"><span data-stu-id="67272-127">Remarks</span></span>

<span data-ttu-id="67272-128">Les composants d’heure figurant dans *datetime* ou *expression* sont ignoré.</span><span class="sxs-lookup"><span data-stu-id="67272-128">Any time component in  *datetime*  or  *expression*  is discarded.</span></span> 
  
<span data-ttu-id="67272-129">Si *datetime* est introuvable ou ne peut pas être converti en un résultat valide, DATEVALUE renvoie une #VALUE !</span><span class="sxs-lookup"><span data-stu-id="67272-129">If  *datetime*  is missing or cannot be converted to a valid result, DATEVALUE returns a #VALUE!</span></span> <span data-ttu-id="67272-130">erreur.</span><span class="sxs-lookup"><span data-stu-id="67272-130">error.</span></span> 
  
<span data-ttu-id="67272-131">La valeur renvoyée s’affiche au format de date abrégée défini dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="67272-131">The returned value is displayed using the short date style set by the system's current Regional Settings.</span></span> 
  
<span data-ttu-id="67272-132">La fonction DATEVALUE accepte également une valeur numérique simple pour *expression* où la partie entière du résultat représente les jours écoulés depuis le 30 décembre 1899.</span><span class="sxs-lookup"><span data-stu-id="67272-132">The DATEVALUE function also accepts a single number value for  *expression*  where the integer portion of the result represents the days since December 30, 1899.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="67272-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="67272-133">Example 1</span></span>

<span data-ttu-id="67272-134">DATEVALUE(NOW( )) + 5 je.</span><span class="sxs-lookup"><span data-stu-id="67272-134">DATEVALUE(NOW( ))+5 ed.</span></span>
  
<span data-ttu-id="67272-135">Renvoie la date actuelle augmentée de cinq jours.</span><span class="sxs-lookup"><span data-stu-id="67272-135">Returns the date five days from now.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="67272-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="67272-136">Example 2</span></span>

<span data-ttu-id="67272-137">DATEVALUE("19/07/1995 12:30")</span><span class="sxs-lookup"><span data-stu-id="67272-137">DATEVALUE("7/19/1995 12:30")</span></span>
  
<span data-ttu-id="67272-138">Renvoie la date.</span><span class="sxs-lookup"><span data-stu-id="67272-138">Returns the date.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="67272-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="67272-139">Example 3</span></span>

<span data-ttu-id="67272-140">DATEVALUE("33 mai 1997")</span><span class="sxs-lookup"><span data-stu-id="67272-140">DATEVALUE("May 33, 1997")</span></span>
  
<span data-ttu-id="67272-p103">Renvoie une erreur #VALEUR!.</span><span class="sxs-lookup"><span data-stu-id="67272-p103">Returns a #VALUE! error.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="67272-143">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="67272-143">Example 4</span></span>

<span data-ttu-id="67272-144">DATEVALUE(35580.6337)</span><span class="sxs-lookup"><span data-stu-id="67272-144">DATEVALUE(35580.6337)</span></span>
  
<span data-ttu-id="67272-145">Renvoie le 30/05/97.</span><span class="sxs-lookup"><span data-stu-id="67272-145">Returns 5/30/1997.</span></span>
  

