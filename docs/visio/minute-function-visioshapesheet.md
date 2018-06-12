---
title: Fonction MINUTE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251464
localization_priority: Normal
ms.assetid: 5a90cb16-7eef-8876-8e25-408787b16f58
description: Renvoie un entier compris entre 0 et 59 représentant le composant des minutes de datetime ou expression.
ms.openlocfilehash: 7c35ec15f2cebd95bb09924ca94f20630c862360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789151"
---
# <a name="minute-function-visioshapesheet"></a><span data-ttu-id="89b01-103">Fonction MINUTE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="89b01-103">MINUTE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="89b01-104">Renvoie un entier compris entre 0 et 59 représentant le composant des minutes de *datetime* ou *expression* .</span><span class="sxs-lookup"><span data-stu-id="89b01-104">Returns an integer from 0 to 59 that represents the minutes component of  *datetime*  or  *expression*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="89b01-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="89b01-105">Syntax</span></span>

<span data-ttu-id="89b01-106">MINUTE (« *datetime* » |  *expression*  [, *lcid* ])</span><span class="sxs-lookup"><span data-stu-id="89b01-106">MINUTE(" *datetime*  "|  *expression*  [,  *lcid*  ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="89b01-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="89b01-107">Parameters</span></span>

|<span data-ttu-id="89b01-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="89b01-108">**Name**</span></span>|<span data-ttu-id="89b01-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="89b01-109">**Required/Optional**</span></span>|<span data-ttu-id="89b01-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="89b01-110">**Data Type**</span></span>|<span data-ttu-id="89b01-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="89b01-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="89b01-112">_DateTime_</span><span class="sxs-lookup"><span data-stu-id="89b01-112">_datetime_</span></span> <br/> |<span data-ttu-id="89b01-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="89b01-113">Required</span></span>  <br/> |<span data-ttu-id="89b01-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="89b01-114">**String**</span></span> <br/> |<span data-ttu-id="89b01-115">Toute chaîne communément reconnue comme date et heure ou comme référence à une cellule contenant une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="89b01-115">Any string commonly recognized as a date and time or a reference to a cell containing a date and time.</span></span>  <br/> |
| <span data-ttu-id="89b01-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="89b01-116">_expression_</span></span> <br/> |<span data-ttu-id="89b01-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="89b01-117">Required</span></span>  <br/> |<span data-ttu-id="89b01-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="89b01-118">**String**</span></span> <br/> | <span data-ttu-id="89b01-119">Toute expression qui génère une date et une heure.</span><span class="sxs-lookup"><span data-stu-id="89b01-119">Any expression that yields a date and time.</span></span>  <br/> |
| <span data-ttu-id="89b01-120">_LCID_</span><span class="sxs-lookup"><span data-stu-id="89b01-120">_lcid_</span></span> <br/> |<span data-ttu-id="89b01-121">Facultatif</span><span class="sxs-lookup"><span data-stu-id="89b01-121">Optional</span></span>  <br/> |<span data-ttu-id="89b01-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="89b01-122">**Number**</span></span> <br/> |<span data-ttu-id="89b01-p101">Identificateur de paramètres régionaux à utiliser pour l’évaluation d’une valeur de date et d’heure non locale. L’identificateur de paramètres régionaux est un nombre décrit dans les fichiers d’en-tête du système.</span><span class="sxs-lookup"><span data-stu-id="89b01-p101">The locale identifier to be used in evaluating a nonlocal datetime. The locale identifier is a number described in the system header files.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="89b01-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="89b01-125">Return value</span></span>

<span data-ttu-id="89b01-126">Entier</span><span class="sxs-lookup"><span data-stu-id="89b01-126">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="89b01-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="89b01-127">Remarks</span></span>

<span data-ttu-id="89b01-128">Le composant date de _datetime_ et _expression_ est ignoré.</span><span class="sxs-lookup"><span data-stu-id="89b01-128">The date component in  _datetime_ and  _expression_ is discarded.</span></span> 
  
<span data-ttu-id="89b01-129">Aucun arrondi n’est effectué.</span><span class="sxs-lookup"><span data-stu-id="89b01-129">No rounding is done.</span></span> <span data-ttu-id="89b01-130">Si _datetime_ est introuvable ou ne peut pas être converti en un résultat valide, la fonction renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="89b01-130">If  _datetime_ is missing or cannot be converted to a valid result, the function returns an error.</span></span> 
  
<span data-ttu-id="89b01-131">La valeur renvoyée est formatée selon le format horaire défini dans les paramètres régionaux actuels de votre système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="89b01-131">The returned value is formatted according to the time style set by the system's current Regional Settings.</span></span>
  
<span data-ttu-id="89b01-132">La fonction MINUTE accepte également une valeur numérique simple pour _expression_ où la partie décimale représente la fraction du jour depuis minuit.</span><span class="sxs-lookup"><span data-stu-id="89b01-132">The MINUTE function also accepts a single number value for  _expression_ where the decimal portion represents the fraction of a day since midnight.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="89b01-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="89b01-133">Example 1</span></span>

<span data-ttu-id="89b01-134">MINUTE("07/07/1999 13:45:24")</span><span class="sxs-lookup"><span data-stu-id="89b01-134">MINUTE("7/7/1999 13:45:24")</span></span>
  
<span data-ttu-id="89b01-135">Renvoie 45.</span><span class="sxs-lookup"><span data-stu-id="89b01-135">Returns 45.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="89b01-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="89b01-136">Example 2</span></span>

<span data-ttu-id="89b01-137">MINUTE(VALEURHEURE("25 janv. 1999 12:07:45") + 6 me.)</span><span class="sxs-lookup"><span data-stu-id="89b01-137">MINUTE(TIMEVALUE("Jan. 25, 1999 12:07:45")+6 em.)</span></span>
  
<span data-ttu-id="89b01-138">Renvoie 13.</span><span class="sxs-lookup"><span data-stu-id="89b01-138">Returns 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="89b01-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="89b01-139">Example 3</span></span>

<span data-ttu-id="89b01-140">MINUTE(0.575)</span><span class="sxs-lookup"><span data-stu-id="89b01-140">MINUTE(0.575)</span></span>
  
<span data-ttu-id="89b01-141">Renvoie 48.</span><span class="sxs-lookup"><span data-stu-id="89b01-141">Returns 48.</span></span>
  

