---
title: RECTSECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: Calcule le secteur d’un rectangle associé à x et y et renvoie un entier compris entre 0 et 4 indiquant le secteur.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160271"
---
# <a name="rectsect-function"></a><span data-ttu-id="de2ca-103">Fonction RECTSECT</span><span class="sxs-lookup"><span data-stu-id="de2ca-103">RECTSECT Function</span></span>

<span data-ttu-id="de2ca-104">Calcule le secteur d’un rectangle associé à *x* et *y* et renvoie un entier compris entre 0 et 4 indiquant le secteur.</span><span class="sxs-lookup"><span data-stu-id="de2ca-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="de2ca-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de2ca-105">Syntax</span></span>

<span data-ttu-id="de2ca-106">RECTSECT (***largeur***, ***hauteur***, ***x***, ***y***, ***option*** )</span><span class="sxs-lookup"><span data-stu-id="de2ca-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="de2ca-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="de2ca-107">Parameters</span></span>

|<span data-ttu-id="de2ca-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="de2ca-108">**Name**</span></span>|<span data-ttu-id="de2ca-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="de2ca-109">**Required/Optional**</span></span>|<span data-ttu-id="de2ca-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="de2ca-110">**Data Type**</span></span>|<span data-ttu-id="de2ca-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="de2ca-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="de2ca-112">_width_</span><span class="sxs-lookup"><span data-stu-id="de2ca-112">_width_</span></span> <br/> |<span data-ttu-id="de2ca-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="de2ca-113">Required</span></span>  <br/> |<span data-ttu-id="de2ca-114">**String**</span><span class="sxs-lookup"><span data-stu-id="de2ca-114">**String**</span></span> <br/> |<span data-ttu-id="de2ca-115">Largeur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="de2ca-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="de2ca-116">_height_</span><span class="sxs-lookup"><span data-stu-id="de2ca-116">_height_</span></span> <br/> |<span data-ttu-id="de2ca-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="de2ca-117">Required</span></span>  <br/> |<span data-ttu-id="de2ca-118">**String**</span><span class="sxs-lookup"><span data-stu-id="de2ca-118">**String**</span></span> <br/> |<span data-ttu-id="de2ca-119">Hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="de2ca-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="de2ca-120">_x_</span><span class="sxs-lookup"><span data-stu-id="de2ca-120">_x_</span></span> <br/> |<span data-ttu-id="de2ca-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="de2ca-121">Required</span></span>  <br/> |<span data-ttu-id="de2ca-122">**String**</span><span class="sxs-lookup"><span data-stu-id="de2ca-122">**String**</span></span> <br/> |<span data-ttu-id="de2ca-123">Coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="de2ca-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="de2ca-124">_y_</span><span class="sxs-lookup"><span data-stu-id="de2ca-124">_y_</span></span> <br/> |<span data-ttu-id="de2ca-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="de2ca-125">Required</span></span>  <br/> |<span data-ttu-id="de2ca-126">**String**</span><span class="sxs-lookup"><span data-stu-id="de2ca-126">**String**</span></span> <br/> |<span data-ttu-id="de2ca-127">Coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="de2ca-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="de2ca-128">_option_</span><span class="sxs-lookup"><span data-stu-id="de2ca-128">_option_</span></span> <br/> |<span data-ttu-id="de2ca-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="de2ca-129">Required</span></span>  <br/> |<span data-ttu-id="de2ca-130">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="de2ca-130">**Boolean**</span></span> <br/> |<span data-ttu-id="de2ca-p101">Indique comment les points des diagonales sont traités. Attribuez la valeur 0 pour utiliser les secteurs de gauche et de droite pour les points d’une diagonale. Attribuez la valeur 1 pour utiliser les secteurs du haut et du bas.</span><span class="sxs-lookup"><span data-stu-id="de2ca-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de2ca-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="de2ca-134">Remarks</span></span>

<span data-ttu-id="de2ca-135">Imaginez un rectangle qui a une *largeur* et une *hauteur* , et un point (*x, y*) à partir du centre du rectangle.</span><span class="sxs-lookup"><span data-stu-id="de2ca-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="de2ca-136">Tracez des lignes diagonales reliant les coins du rectangle pour le diviser en quatre secteurs avec un point central.</span><span class="sxs-lookup"><span data-stu-id="de2ca-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="de2ca-137">Les secteurs de 0 à 4 représentent respectivement le point central, la droite, le haut, le bas et la gauche.</span><span class="sxs-lookup"><span data-stu-id="de2ca-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Les secteurs 0 à 4 représentent respectivement le point central, droit, supérieur, gauche et inférieur](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="de2ca-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="de2ca-139">Example</span></span>

<span data-ttu-id="de2ca-140">RECTSECT(25,4 mm; 50,8 mm; 25,4 mm; -177,8 mm; 0)</span><span class="sxs-lookup"><span data-stu-id="de2ca-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="de2ca-141">Renvoie 4.</span><span class="sxs-lookup"><span data-stu-id="de2ca-141">Returns 4.</span></span> 
  

