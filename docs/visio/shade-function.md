---
title: SHADE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Modifie la couleur en réduisant sa luminosité par la quantité (positive ou négative) spécifiée dans le paramètre int.
ms.openlocfilehash: b31b4c49a823ace3f6474b94ba3737791928520d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326595"
---
# <a name="shade-function"></a><span data-ttu-id="77f88-103">Fonction SHADE</span><span class="sxs-lookup"><span data-stu-id="77f88-103">SHADE Function</span></span>

<span data-ttu-id="77f88-104">Modifie la couleur en réduisant sa luminosité par la quantité (positive ou négative) spécifiée dans le _paramètre int._</span><span class="sxs-lookup"><span data-stu-id="77f88-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="77f88-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="77f88-105">Syntax</span></span>

<span data-ttu-id="77f88-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="77f88-106">SHADE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="77f88-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="77f88-107">Parameters</span></span>

|<span data-ttu-id="77f88-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="77f88-108">**Name**</span></span>|<span data-ttu-id="77f88-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="77f88-109">**Required/Optional**</span></span>|<span data-ttu-id="77f88-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="77f88-110">**Data Type**</span></span>|<span data-ttu-id="77f88-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="77f88-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="77f88-112">_color_</span><span class="sxs-lookup"><span data-stu-id="77f88-112">_color_</span></span> <br/> |<span data-ttu-id="77f88-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="77f88-113">Required</span></span>  <br/> |<span data-ttu-id="77f88-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="77f88-114">**Numeric**</span></span> <br/> |<span data-ttu-id="77f88-115">Index de couleurs Microsoft Visio ou valeur RVB de la couleur.</span><span class="sxs-lookup"><span data-stu-id="77f88-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="77f88-116">_int_</span><span class="sxs-lookup"><span data-stu-id="77f88-116">_int_</span></span> <br/> |<span data-ttu-id="77f88-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="77f88-117">Required</span></span>  <br/> |<span data-ttu-id="77f88-118">**Entier**</span><span class="sxs-lookup"><span data-stu-id="77f88-118">**Integer**</span></span> <br/> |<span data-ttu-id="77f88-119">Valeur de diminution de la luminosité de la couleur.</span><span class="sxs-lookup"><span data-stu-id="77f88-119">The amount by which to decrease the luminosity of the color.</span></span> <span data-ttu-id="77f88-120">Elle peut être positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="77f88-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="77f88-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="77f88-121">Return value</span></span>

 <span data-ttu-id="77f88-122">**RVB**</span><span class="sxs-lookup"><span data-stu-id="77f88-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77f88-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="77f88-123">Remarks</span></span>

<span data-ttu-id="77f88-124">Les limites basse et haute de luminosité sont respectivement 0 et 240.</span><span class="sxs-lookup"><span data-stu-id="77f88-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="77f88-125">Il n’y a aucune limite sur la taille de l’nombre integer que vous pouvez transmettre pour le paramètre  _int,_ mais la luminosité ne dépasse jamais ces limites.</span><span class="sxs-lookup"><span data-stu-id="77f88-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![Limites supérieures et inférieures de luminosité](media/image199_ZA10173627.gif)
  

