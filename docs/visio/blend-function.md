---
title: BLEND, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Mélange deux couleurs dans les proportions spécifiées par le paramètre float.
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788145"
---
# <a name="blend-function"></a><span data-ttu-id="8d7b9-103">BLEND, fonction</span><span class="sxs-lookup"><span data-stu-id="8d7b9-103">BLEND Function</span></span>

<span data-ttu-id="8d7b9-104">Mélange deux couleurs dans les proportions spécifiées par le paramètre _float_ .</span><span class="sxs-lookup"><span data-stu-id="8d7b9-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d7b9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d7b9-105">Syntax</span></span>

<span data-ttu-id="8d7b9-106">BLEND (** *color1* **, ** *color2* **, ** *float [0,1]* **)</span><span class="sxs-lookup"><span data-stu-id="8d7b9-106">BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8d7b9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d7b9-107">Parameters</span></span>

|<span data-ttu-id="8d7b9-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-108">**Name**</span></span>|<span data-ttu-id="8d7b9-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-109">**Required/Optional**</span></span>|<span data-ttu-id="8d7b9-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-110">**Data Type**</span></span>|<span data-ttu-id="8d7b9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8d7b9-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="8d7b9-112">_color1_</span></span> <br/> |<span data-ttu-id="8d7b9-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8d7b9-113">Required</span></span>  <br/> |<span data-ttu-id="8d7b9-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8d7b9-115">L’index de couleurs Visio ou la valeur RVB de la première couleur.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="8d7b9-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="8d7b9-116">_color2_</span></span> <br/> |<span data-ttu-id="8d7b9-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8d7b9-117">Required</span></span>  <br/> |<span data-ttu-id="8d7b9-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8d7b9-119">L’index de couleurs Visio ou la valeur RVB de la deuxième couleur.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="8d7b9-120">_float [0,1]_</span><span class="sxs-lookup"><span data-stu-id="8d7b9-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="8d7b9-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8d7b9-121">Required</span></span>  <br/> |<span data-ttu-id="8d7b9-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-122">**Float**</span></span> <br/> |<span data-ttu-id="8d7b9-123">La proportion de fusion _color2_ et _color1_, respectivement.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="8d7b9-124">Nombre réel entre 0 et 1 (inclus).</span><span class="sxs-lookup"><span data-stu-id="8d7b9-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8d7b9-125">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8d7b9-125">Return value</span></span>

 <span data-ttu-id="8d7b9-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="8d7b9-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8d7b9-127">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d7b9-127">Remarks</span></span>

<span data-ttu-id="8d7b9-128">La couleur renvoyée est déterminée par les proportions mélange _color2_ et _color1_, respectivement, comme spécifié par le paramètre _float_ .</span><span class="sxs-lookup"><span data-stu-id="8d7b9-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="8d7b9-129">Par exemple, si _float_ est 0.25, la couleur renvoyée est composée de 75 % des _color1_ et de 25 % de _color2_.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="8d7b9-130">Une autre manière de penser est que la valeur de _type float_ correspondant au point le long du spectre de _color1_ à _color2_.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="8d7b9-131">Par conséquent, plus petits numéros (de la plus proche de zéro) pour _float_ produit fusion rapprocher à _color1_, tandis que les numéros plus grande (plus proche de 1) produire dégradés rapprocher en _color2_.</span><span class="sxs-lookup"><span data-stu-id="8d7b9-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

