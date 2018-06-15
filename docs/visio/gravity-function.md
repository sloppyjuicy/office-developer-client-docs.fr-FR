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
description: Calcule l’angle correct d’un bloc de texte de la rotation de la rotation de la forme indiquée empêcher le texte d’activation de haut en bas.
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19788733"
---
# <a name="gravity-function"></a><span data-ttu-id="c235d-103">GRAVITY, fonction</span><span class="sxs-lookup"><span data-stu-id="c235d-103">GRAVITY Function</span></span>

<span data-ttu-id="c235d-104">Calcule l’angle correct d’un bloc de texte de la rotation de la rotation de la forme indiquée empêcher le texte d’activation de haut en bas.</span><span class="sxs-lookup"><span data-stu-id="c235d-104">Calculates a text block's correct angle of rotation for the indicated shape rotation to prevent the text from turning upside down.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c235d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c235d-105">Syntax</span></span>

<span data-ttu-id="c235d-106">GRAVITY (** *angle* **, [** *limit1* **], [** *limit2* **])</span><span class="sxs-lookup"><span data-stu-id="c235d-106">GRAVITY(** *angle* **,[ ** *limit1* ** ],[ ** *limit2* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c235d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c235d-107">Parameters</span></span>

|<span data-ttu-id="c235d-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c235d-108">**Name**</span></span>|<span data-ttu-id="c235d-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c235d-109">**Required/Optional**</span></span>|<span data-ttu-id="c235d-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c235d-110">**Data Type**</span></span>|<span data-ttu-id="c235d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c235d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c235d-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="c235d-112">_angle_</span></span> <br/> |<span data-ttu-id="c235d-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c235d-113">Required</span></span>  <br/> |<span data-ttu-id="c235d-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="c235d-114">**String**</span></span> <br/> | <span data-ttu-id="c235d-115">Angle de la forme.</span><span class="sxs-lookup"><span data-stu-id="c235d-115">The shape's angle.</span></span>  <br/> |
| <span data-ttu-id="c235d-116">_limit1_</span><span class="sxs-lookup"><span data-stu-id="c235d-116">_limit1_</span></span> <br/> |<span data-ttu-id="c235d-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c235d-117">Optional</span></span>  <br/> |<span data-ttu-id="c235d-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="c235d-118">**String**</span></span> <br/> |<span data-ttu-id="c235d-p101">Première limite de rotation. La valeur par défaut est 90 degrés.</span><span class="sxs-lookup"><span data-stu-id="c235d-p101">First limit of rotation. Default is 90 degrees.</span></span>  <br/> |
| <span data-ttu-id="c235d-121">_limit2_</span><span class="sxs-lookup"><span data-stu-id="c235d-121">_limit2_</span></span> <br/> |<span data-ttu-id="c235d-122">Facultatif</span><span class="sxs-lookup"><span data-stu-id="c235d-122">Optional</span></span>  <br/> |<span data-ttu-id="c235d-123">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="c235d-123">**String**</span></span> <br/> |<span data-ttu-id="c235d-p102">Deuxième limite de rotation. La valeur par défaut est 270 degrés.</span><span class="sxs-lookup"><span data-stu-id="c235d-p102">Second limit of rotation. Default is 270 degrees.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c235d-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="c235d-126">Return value</span></span>

<span data-ttu-id="c235d-127">Chaîne</span><span class="sxs-lookup"><span data-stu-id="c235d-127">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c235d-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="c235d-128">Remarks</span></span>

<span data-ttu-id="c235d-129">La fonction GRAVITY est généralement utilisée dans la cellule AngleTexte.</span><span class="sxs-lookup"><span data-stu-id="c235d-129">The GRAVITY function is usually used in the TxtAngle cell.</span></span> 
  
<span data-ttu-id="c235d-130">La valeur renvoyée est 180 degrés si _angle_ est compris entre les valeurs spécifiées _dans limit1_ et _limit2_; dans le cas contraire, la valeur renvoyée est 0 degré.</span><span class="sxs-lookup"><span data-stu-id="c235d-130">The value returned is 180 degrees if  _angle_ is between the values specified by  _limit1_ and  _limit2_; otherwise the value returned is 0 degrees.</span></span>
  
<span data-ttu-id="c235d-p103">Tous les arguments sont automatiquement normalisés par la fonction à des valeurs comprises entre 0 et 360 degrés. Si un argument ne précise pas d’unités, les radians sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="c235d-p103">All of the arguments are automatically normalized between 0 and 360 degrees by the function. If an argument does not specify units, radians are assumed.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c235d-133">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="c235d-133">Example 1</span></span>

<span data-ttu-id="c235d-134">GRAVITY(Angle)</span><span class="sxs-lookup"><span data-stu-id="c235d-134">GRAVITY(Angle)</span></span>
  
<span data-ttu-id="c235d-135">Renvoie 180 degrés si *angle* est compris entre 90 et 270 degrés ; Sinon, renvoie 0 degré.</span><span class="sxs-lookup"><span data-stu-id="c235d-135">Returns 180 degrees if  *angle*  is between 90 and 270 degrees; otherwise, returns 0 degrees.</span></span> 
  
## <a name="example-2"></a><span data-ttu-id="c235d-136">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="c235d-136">Example 2</span></span>

<span data-ttu-id="c235d-137">GRAVITY(2)</span><span class="sxs-lookup"><span data-stu-id="c235d-137">GRAVITY(2)</span></span>
  
<span data-ttu-id="c235d-138">Renvoie 180 degrés, car 2 radians est compris entre 90 et 270 degrés.</span><span class="sxs-lookup"><span data-stu-id="c235d-138">Returns 180 degrees, because 2 radians is between 90 and 270 degrees.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c235d-139">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="c235d-139">Example 3</span></span>

<span data-ttu-id="c235d-140">GRAVITY(100 deg, 110 deg, 290 deg)</span><span class="sxs-lookup"><span data-stu-id="c235d-140">GRAVITY(100 deg, 110 deg, 290 deg)</span></span>
  
<span data-ttu-id="c235d-141">Renvoie 0 degré.</span><span class="sxs-lookup"><span data-stu-id="c235d-141">Returns 0 degrees.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="c235d-142">Exemple 4</span><span class="sxs-lookup"><span data-stu-id="c235d-142">Example 4</span></span>

<span data-ttu-id="c235d-143">GRAVITY(100 deg, 290 deg, 110 deg)</span><span class="sxs-lookup"><span data-stu-id="c235d-143">GRAVITY(100 deg, 290 deg, 110 deg)</span></span>
  
<span data-ttu-id="c235d-144">Renvoie 0 degré.</span><span class="sxs-lookup"><span data-stu-id="c235d-144">Returns 0 degrees.</span></span>
  

