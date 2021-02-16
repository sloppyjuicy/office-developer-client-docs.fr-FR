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
description: Calcule le secteur d’un rectangle associé à x et y et renvoie un nombre integer de 0 à 4, indiquant le secteur.
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160271"
---
# <a name="rectsect-function"></a><span data-ttu-id="ee1c3-103">Fonction RECTSECT</span><span class="sxs-lookup"><span data-stu-id="ee1c3-103">RECTSECT Function</span></span>

<span data-ttu-id="ee1c3-104">Calcule le secteur d’un rectangle associé à  *x*  et  *y*  et renvoie un nombre integer de 0 à 4, indiquant le secteur.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ee1c3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee1c3-105">Syntax</span></span>

<span data-ttu-id="ee1c3-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span><span class="sxs-lookup"><span data-stu-id="ee1c3-106">RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ee1c3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ee1c3-107">Parameters</span></span>

|<span data-ttu-id="ee1c3-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-108">**Name**</span></span>|<span data-ttu-id="ee1c3-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-109">**Required/Optional**</span></span>|<span data-ttu-id="ee1c3-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-110">**Data Type**</span></span>|<span data-ttu-id="ee1c3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ee1c3-112">_width_</span><span class="sxs-lookup"><span data-stu-id="ee1c3-112">_width_</span></span> <br/> |<span data-ttu-id="ee1c3-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee1c3-113">Required</span></span>  <br/> |<span data-ttu-id="ee1c3-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-114">**String**</span></span> <br/> |<span data-ttu-id="ee1c3-115">Largeur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="ee1c3-116">_height_</span><span class="sxs-lookup"><span data-stu-id="ee1c3-116">_height_</span></span> <br/> |<span data-ttu-id="ee1c3-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee1c3-117">Required</span></span>  <br/> |<span data-ttu-id="ee1c3-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-118">**String**</span></span> <br/> |<span data-ttu-id="ee1c3-119">Hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="ee1c3-120">_x_</span><span class="sxs-lookup"><span data-stu-id="ee1c3-120">_x_</span></span> <br/> |<span data-ttu-id="ee1c3-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee1c3-121">Required</span></span>  <br/> |<span data-ttu-id="ee1c3-122">**String**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-122">**String**</span></span> <br/> |<span data-ttu-id="ee1c3-123">Coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="ee1c3-124">_y_</span><span class="sxs-lookup"><span data-stu-id="ee1c3-124">_y_</span></span> <br/> |<span data-ttu-id="ee1c3-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee1c3-125">Required</span></span>  <br/> |<span data-ttu-id="ee1c3-126">**String**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-126">**String**</span></span> <br/> |<span data-ttu-id="ee1c3-127">Coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="ee1c3-128">_option_</span><span class="sxs-lookup"><span data-stu-id="ee1c3-128">_option_</span></span> <br/> |<span data-ttu-id="ee1c3-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ee1c3-129">Required</span></span>  <br/> |<span data-ttu-id="ee1c3-130">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="ee1c3-130">**Boolean**</span></span> <br/> |<span data-ttu-id="ee1c3-p101">Indique comment les points des diagonales sont traités. Attribuez la valeur 0 pour utiliser les secteurs de gauche et de droite pour les points d’une diagonale. Attribuez la valeur 1 pour utiliser les secteurs du haut et du bas.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee1c3-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee1c3-134">Remarks</span></span>

<span data-ttu-id="ee1c3-135">Considérons un rectangle qui a une  *largeur et*  une  *hauteur,*  et un point (*x,y*) à partir du point central du rectangle.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="ee1c3-136">Tracez des lignes diagonales reliant les coins du rectangle pour le diviser en quatre secteurs avec un point central.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="ee1c3-137">Les secteurs de 0 à 4 représentent respectivement le point central, la droite, le haut, le bas et la gauche.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Les secteurs 0 à 4 représentent respectivement le point central, la droite, le haut, la gauche et le bas](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="ee1c3-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="ee1c3-139">Example</span></span>

<span data-ttu-id="ee1c3-140">RECTSECT(25,4 mm; 50,8 mm; 25,4 mm; -177,8 mm; 0)</span><span class="sxs-lookup"><span data-stu-id="ee1c3-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="ee1c3-141">Renvoie 4.</span><span class="sxs-lookup"><span data-stu-id="ee1c3-141">Returns 4.</span></span> 
  

