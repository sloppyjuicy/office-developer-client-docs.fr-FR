---
title: TINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifie la couleur en augmentant sa luminosité de la valeur (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280930"
---
# <a name="tint-function"></a><span data-ttu-id="231c2-103">Fonction TINT</span><span class="sxs-lookup"><span data-stu-id="231c2-103">TINT Function</span></span>

<span data-ttu-id="231c2-104">Modifie la couleur en augmentant sa luminosité de la valeur (positive ou négative) spécifiée dans le paramètre _int_ .</span><span class="sxs-lookup"><span data-stu-id="231c2-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="231c2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="231c2-105">Syntax</span></span>

<span data-ttu-id="231c2-106">TEINTe (\* \* *couleur* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="231c2-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="231c2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="231c2-107">Parameters</span></span>

|<span data-ttu-id="231c2-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="231c2-108">**Name**</span></span>|<span data-ttu-id="231c2-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="231c2-109">**Required/Optional**</span></span>|<span data-ttu-id="231c2-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="231c2-110">**Data Type**</span></span>|<span data-ttu-id="231c2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="231c2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="231c2-112">_color_</span><span class="sxs-lookup"><span data-stu-id="231c2-112">_color_</span></span> <br/> |<span data-ttu-id="231c2-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="231c2-113">Required</span></span>  <br/> |<span data-ttu-id="231c2-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="231c2-114">**Numeric**</span></span> <br/> |<span data-ttu-id="231c2-115">Index de couleurs Microsoft Visio ou valeur RVB de la couleur.</span><span class="sxs-lookup"><span data-stu-id="231c2-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="231c2-116">_int_</span><span class="sxs-lookup"><span data-stu-id="231c2-116">_int_</span></span> <br/> |<span data-ttu-id="231c2-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="231c2-117">Required</span></span>  <br/> |<span data-ttu-id="231c2-118">**Entier**</span><span class="sxs-lookup"><span data-stu-id="231c2-118">**Integer**</span></span> <br/> |<span data-ttu-id="231c2-119">Valeur d’augmentation de la luminosité de la couleur.</span><span class="sxs-lookup"><span data-stu-id="231c2-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="231c2-120">Elle peut être positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="231c2-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="231c2-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="231c2-121">Return value</span></span>

 <span data-ttu-id="231c2-122">**RVB**</span><span class="sxs-lookup"><span data-stu-id="231c2-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="231c2-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="231c2-123">Remarks</span></span>

<span data-ttu-id="231c2-124">Les limites basse et haute de luminosité sont respectivement 0 et 240.</span><span class="sxs-lookup"><span data-stu-id="231c2-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="231c2-125">Il n'y a pas de limite quant à la taille de l'entier que vous pouvez transmettre pour le paramètre _int_ , mais la luminosité ne dépasse jamais ces limites.</span><span class="sxs-lookup"><span data-stu-id="231c2-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

