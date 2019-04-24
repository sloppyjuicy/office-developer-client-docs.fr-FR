---
title: BLEND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Fusionne deux couleurs dans la proportion spécifiée par le paramètre float.
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303296"
---
# <a name="blend-function"></a><span data-ttu-id="df868-103">Fonction BLEND</span><span class="sxs-lookup"><span data-stu-id="df868-103">BLEND Function</span></span>

<span data-ttu-id="df868-104">Fusionne deux couleurs dans la proportion spécifiée par le paramètre _float_ .</span><span class="sxs-lookup"><span data-stu-id="df868-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="df868-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="df868-105">Syntax</span></span>

<span data-ttu-id="df868-106">BLEND (\* \* *color1* \* \*, \* \* *color2* \* \*, \* \* *float [0, 1]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="df868-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df868-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="df868-107">Parameters</span></span>

|<span data-ttu-id="df868-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="df868-108">**Name**</span></span>|<span data-ttu-id="df868-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="df868-109">**Required/Optional**</span></span>|<span data-ttu-id="df868-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="df868-110">**Data Type**</span></span>|<span data-ttu-id="df868-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="df868-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df868-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="df868-112">_color1_</span></span> <br/> |<span data-ttu-id="df868-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df868-113">Required</span></span>  <br/> |<span data-ttu-id="df868-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="df868-114">**Numeric**</span></span> <br/> |<span data-ttu-id="df868-115">L’index de couleurs Visio ou la valeur RVB de la première couleur.</span><span class="sxs-lookup"><span data-stu-id="df868-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="df868-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="df868-116">_color2_</span></span> <br/> |<span data-ttu-id="df868-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df868-117">Required</span></span>  <br/> |<span data-ttu-id="df868-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="df868-118">**Numeric**</span></span> <br/> |<span data-ttu-id="df868-119">L’index de couleurs Visio ou la valeur RVB de la deuxième couleur.</span><span class="sxs-lookup"><span data-stu-id="df868-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="df868-120">_flotteur [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="df868-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="df868-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="df868-121">Required</span></span>  <br/> |<span data-ttu-id="df868-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="df868-122">**Float**</span></span> <br/> |<span data-ttu-id="df868-123">Proportion de mélange de _color2_ et de _color1_, respectivement.</span><span class="sxs-lookup"><span data-stu-id="df868-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="df868-124">Nombre réel entre 0 et 1 inclus.</span><span class="sxs-lookup"><span data-stu-id="df868-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="df868-125">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="df868-125">Return value</span></span>

 <span data-ttu-id="df868-126">**RVB**</span><span class="sxs-lookup"><span data-stu-id="df868-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="df868-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="df868-127">Remarks</span></span>

<span data-ttu-id="df868-128">La couleur renvoyée est déterminée par les proportions relatives dans lesquelles fusionner _color2_ et _color1_, respectivement, comme spécifié par le paramètre _float_ .</span><span class="sxs-lookup"><span data-stu-id="df868-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="df868-129">Par exemple, si _float_ est 0,25, la couleur renvoyée est composée de 75% de _color1_ et de 25% de _color2_.</span><span class="sxs-lookup"><span data-stu-id="df868-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="df868-130">Une autre façon de penser est que la valeur en _virgule flottante_ correspond au point le long du spectre de couleurs de _color1_ à _color2_.</span><span class="sxs-lookup"><span data-stu-id="df868-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="df868-131">Par conséquent, des nombres plus petits (plus proches __ de zéro) pour les produits flottants produisent des fusions plus proches de la taille de _color1_, tandis que les grands nombres (plus de 1) produisent des fusions plus près de _color2_.</span><span class="sxs-lookup"><span data-stu-id="df868-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

