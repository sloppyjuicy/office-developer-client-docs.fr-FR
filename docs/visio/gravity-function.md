---
title: GRAVITY, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: Calcule l'angle de rotation correct d'un bloc de texte pour la rotation de forme indiquée de sorte que le texte ne soit pas renversé.
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360185"
---
# <a name="gravity-function"></a><span data-ttu-id="14200-103">Fonction GRAVITY</span><span class="sxs-lookup"><span data-stu-id="14200-103">GRAVITY Function</span></span>

<span data-ttu-id="14200-104">Calcule l'angle de rotation correct d'un bloc de texte pour la rotation de forme indiquée de sorte que le texte ne soit pas renversé.</span><span class="sxs-lookup"><span data-stu-id="14200-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="14200-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14200-105">Syntax</span></span>

<span data-ttu-id="14200-106">Gravité (\* \* *angle* \* *, [* \* *limite1* \* *], [* \* *limit2* \* \*])</span><span class="sxs-lookup"><span data-stu-id="14200-106">GRAVITY(\*\* *angle* \*\*,[ \*\* *limit1* \*\* ],[ \*\* *limit2* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="14200-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14200-107">Parameters</span></span>

|<span data-ttu-id="14200-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="14200-108">**Name**</span></span>|<span data-ttu-id="14200-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="14200-109">**Required/Optional**</span></span>|<span data-ttu-id="14200-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="14200-110">**Data Type**</span></span>|<span data-ttu-id="14200-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="14200-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="14200-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="14200-112">_angle_</span></span> <br/> |<span data-ttu-id="14200-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="14200-113">Required</span></span>  <br/> |<span data-ttu-id="14200-114">**String**</span><span class="sxs-lookup"><span data-stu-id="14200-114">**String**</span></span> <br/> | <span data-ttu-id="14200-115">Angle de la forme.</span><span class="sxs-lookup"><span data-stu-id="14200-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="14200-116">_limite1_</span><span class="sxs-lookup"><span data-stu-id="14200-116">_limit1_</span></span> <br/> |<span data-ttu-id="14200-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="14200-117">Optional</span></span>  <br/> |<span data-ttu-id="14200-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="14200-118">**String**</span></span> <br/> |<span data-ttu-id="14200-119">Première limite de rotation.</span><span class="sxs-lookup"><span data-stu-id="14200-119">First limit of rotation.</span></span> <span data-ttu-id="14200-120">La valeur par défaut est 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="14200-120">Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="14200-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="14200-121">_limit2_</span></span> <br/> |<span data-ttu-id="14200-122">Facultatif</span><span class="sxs-lookup"><span data-stu-id="14200-122">Optional</span></span>  <br/> |<span data-ttu-id="14200-123">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="14200-123">**String**</span></span> <br/> |<span data-ttu-id="14200-124">Deuxième limite de rotation.</span><span class="sxs-lookup"><span data-stu-id="14200-124">Second limit of rotation.</span></span> <span data-ttu-id="14200-125">La valeur par défaut est 270 degrés.</span><span class="sxs-lookup"><span data-stu-id="14200-125">Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="14200-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="14200-126">Return value</span></span>

<span data-ttu-id="14200-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="14200-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="14200-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="14200-128">Remarks</span></span>

<span data-ttu-id="14200-129">La fonction GRAVITY est généralement utilisée dans la cellule AngleTexte.</span><span class="sxs-lookup"><span data-stu-id="14200-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="14200-130">La valeur renvoyée est 180 degrees si _angle_ est compris entre les valeurs spécifiées par _limite1_ et _limit2_; Sinon, la valeur renvoyée est 0 degré.</span><span class="sxs-lookup"><span data-stu-id="14200-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="14200-131">Tous les arguments sont automatiquement normalisés par la fonction à des valeurs comprises entre 0 et 360 degrés.</span><span class="sxs-lookup"><span data-stu-id="14200-131">All of the arguments are automatically normalized between 0 and 360 degrees by the function.</span></span> <span data-ttu-id="14200-132">Si un argument ne précise pas d’unités, les radians sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="14200-132">If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="14200-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="14200-133">Example 1</span></span>

<span data-ttu-id="14200-134">GRAVITÉ (angle)</span><span class="sxs-lookup"><span data-stu-id="14200-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="14200-135">Renvoie 180 degrés si *angle* est compris entre 90 et 270 degrés; Sinon, renvoie 0 degré.</span><span class="sxs-lookup"><span data-stu-id="14200-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="14200-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="14200-136">Example 2</span></span>

<span data-ttu-id="14200-137">GRAVITÉ (2)</span><span class="sxs-lookup"><span data-stu-id="14200-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="14200-138">Renvoie 180 degrés, car 2 radians est compris entre 90 et 270 degrés.</span><span class="sxs-lookup"><span data-stu-id="14200-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="14200-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="14200-139">Example 3</span></span>

<span data-ttu-id="14200-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="14200-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="14200-141">Renvoie 0 degré.</span><span class="sxs-lookup"><span data-stu-id="14200-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="14200-142">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="14200-142">Example 4</span></span>

<span data-ttu-id="14200-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="14200-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="14200-144">Renvoie 0 degré.</span><span class="sxs-lookup"><span data-stu-id="14200-144">Returns 0 degrees.</span></span>
  

