---
title: TONE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifie la couleur en diminuant sa saturation de la valeur spécifiée dans le paramètre int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335685"
---
# <a name="tone-function"></a><span data-ttu-id="5ebb0-103">Fonction TONE</span><span class="sxs-lookup"><span data-stu-id="5ebb0-103">TONE Function</span></span>

<span data-ttu-id="5ebb0-104">Modifie la couleur en diminuant sa saturation de la valeur spécifiée dans le paramètre _int_ .</span><span class="sxs-lookup"><span data-stu-id="5ebb0-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5ebb0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5ebb0-105">Syntax</span></span>

<span data-ttu-id="5ebb0-106">TON (\* \* *couleur* \* \*, \* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5ebb0-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5ebb0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5ebb0-107">Parameters</span></span>

|<span data-ttu-id="5ebb0-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-108">**Name**</span></span>|<span data-ttu-id="5ebb0-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-109">**Required/Optional**</span></span>|<span data-ttu-id="5ebb0-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-110">**Data Type**</span></span>|<span data-ttu-id="5ebb0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5ebb0-112">_color_</span><span class="sxs-lookup"><span data-stu-id="5ebb0-112">_color_</span></span> <br/> |<span data-ttu-id="5ebb0-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5ebb0-113">Required</span></span>  <br/> |<span data-ttu-id="5ebb0-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-114">**Numeric**</span></span> <br/> |<span data-ttu-id="5ebb0-115">Index de couleurs Microsoft Visio ou valeur RVB de la couleur.</span><span class="sxs-lookup"><span data-stu-id="5ebb0-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="5ebb0-116">_int_</span><span class="sxs-lookup"><span data-stu-id="5ebb0-116">_int_</span></span> <br/> |<span data-ttu-id="5ebb0-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5ebb0-117">Required</span></span>  <br/> |<span data-ttu-id="5ebb0-118">**Entier**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-118">**Integer**</span></span> <br/> |<span data-ttu-id="5ebb0-119">Valeur de diminution de la saturation de la couleur.</span><span class="sxs-lookup"><span data-stu-id="5ebb0-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="5ebb0-120">Elle peut être positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="5ebb0-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5ebb0-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="5ebb0-121">Return value</span></span>

 <span data-ttu-id="5ebb0-122">**RVB**</span><span class="sxs-lookup"><span data-stu-id="5ebb0-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5ebb0-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ebb0-123">Remarks</span></span>

<span data-ttu-id="5ebb0-124">Les limites basse et haute de saturation sont respectivement 0 et 240.</span><span class="sxs-lookup"><span data-stu-id="5ebb0-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="5ebb0-125">Il n'y a pas de limite quant à la taille de l'entier que vous pouvez transmettre pour le paramètre _int_ , mais la saturation ne dépasse jamais ces limites.</span><span class="sxs-lookup"><span data-stu-id="5ebb0-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

