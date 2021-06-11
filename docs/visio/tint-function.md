---
title: TINT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406576"
---
# <a name="tint-function"></a><span data-ttu-id="68c41-103">Fonction TINT</span><span class="sxs-lookup"><span data-stu-id="68c41-103">TINT Function</span></span>

<span data-ttu-id="68c41-104">Modifie la couleur en augmentant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int._</span><span class="sxs-lookup"><span data-stu-id="68c41-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="68c41-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68c41-105">Syntax</span></span>

<span data-ttu-id="68c41-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="68c41-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="68c41-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68c41-107">Parameters</span></span>

|<span data-ttu-id="68c41-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="68c41-108">**Name**</span></span>|<span data-ttu-id="68c41-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="68c41-109">**Required/Optional**</span></span>|<span data-ttu-id="68c41-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="68c41-110">**Data Type**</span></span>|<span data-ttu-id="68c41-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="68c41-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="68c41-112">_color_</span><span class="sxs-lookup"><span data-stu-id="68c41-112">_color_</span></span> <br/> |<span data-ttu-id="68c41-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="68c41-113">Required</span></span>  <br/> |<span data-ttu-id="68c41-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="68c41-114">**Numeric**</span></span> <br/> |<span data-ttu-id="68c41-115">Index de couleurs Microsoft Visio ou valeur RVB de la couleur.</span><span class="sxs-lookup"><span data-stu-id="68c41-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="68c41-116">_int_</span><span class="sxs-lookup"><span data-stu-id="68c41-116">_int_</span></span> <br/> |<span data-ttu-id="68c41-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="68c41-117">Required</span></span>  <br/> |<span data-ttu-id="68c41-118">**Entier**</span><span class="sxs-lookup"><span data-stu-id="68c41-118">**Integer**</span></span> <br/> |<span data-ttu-id="68c41-p101">Valeur d’augmentation de la luminosité de la couleur. Elle peut être positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="68c41-p101">The amount by which to increase the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="68c41-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="68c41-121">Return value</span></span>

 <span data-ttu-id="68c41-122">**RVB**</span><span class="sxs-lookup"><span data-stu-id="68c41-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="68c41-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="68c41-123">Remarks</span></span>

<span data-ttu-id="68c41-124">Les limites basse et haute de luminosité sont respectivement 0 et 240.</span><span class="sxs-lookup"><span data-stu-id="68c41-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="68c41-125">Il n’y a aucune limite sur la taille de l’nombre integer que vous pouvez transmettre pour le paramètre  _int,_ mais la luminosité ne dépasse jamais ces limites.</span><span class="sxs-lookup"><span data-stu-id="68c41-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

