---
title: TONE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le paramètre int.
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434374"
---
# <a name="tone-function"></a><span data-ttu-id="9a370-103">Fonction TONE</span><span class="sxs-lookup"><span data-stu-id="9a370-103">TONE Function</span></span>

<span data-ttu-id="9a370-104">Modifie la couleur en réduisant sa saturation par la quantité spécifiée dans le _paramètre int._</span><span class="sxs-lookup"><span data-stu-id="9a370-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9a370-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9a370-105">Syntax</span></span>

<span data-ttu-id="9a370-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span><span class="sxs-lookup"><span data-stu-id="9a370-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9a370-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9a370-107">Parameters</span></span>

|<span data-ttu-id="9a370-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="9a370-108">**Name**</span></span>|<span data-ttu-id="9a370-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="9a370-109">**Required/Optional**</span></span>|<span data-ttu-id="9a370-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="9a370-110">**Data Type**</span></span>|<span data-ttu-id="9a370-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="9a370-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9a370-112">_color_</span><span class="sxs-lookup"><span data-stu-id="9a370-112">_color_</span></span> <br/> |<span data-ttu-id="9a370-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9a370-113">Required</span></span>  <br/> |<span data-ttu-id="9a370-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="9a370-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9a370-115">Index de couleurs Microsoft Visio ou valeur RVB de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9a370-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="9a370-116">_int_</span><span class="sxs-lookup"><span data-stu-id="9a370-116">_int_</span></span> <br/> |<span data-ttu-id="9a370-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9a370-117">Required</span></span>  <br/> |<span data-ttu-id="9a370-118">**Entier**</span><span class="sxs-lookup"><span data-stu-id="9a370-118">**Integer**</span></span> <br/> |<span data-ttu-id="9a370-119">Valeur de diminution de la saturation de la couleur.</span><span class="sxs-lookup"><span data-stu-id="9a370-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="9a370-120">Elle peut être positive ou négative.</span><span class="sxs-lookup"><span data-stu-id="9a370-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="9a370-121">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9a370-121">Return value</span></span>

 <span data-ttu-id="9a370-122">**RVB**</span><span class="sxs-lookup"><span data-stu-id="9a370-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9a370-123">Remarques</span><span class="sxs-lookup"><span data-stu-id="9a370-123">Remarks</span></span>

<span data-ttu-id="9a370-124">Les limites basse et haute de saturation sont respectivement 0 et 240.</span><span class="sxs-lookup"><span data-stu-id="9a370-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="9a370-125">Il n’y a aucune limite sur la taille de l’nombre integer que vous pouvez transmettre pour le paramètre  _int,_ mais la saturation ne dépasse jamais ces limites.</span><span class="sxs-lookup"><span data-stu-id="9a370-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

