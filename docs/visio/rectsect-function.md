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
description: Calcule le secteur d'un rectangle associé à x et y et renvoie un entier compris entre 0 et 4 indiquant le secteur.
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360027"
---
# <a name="rectsect-function"></a><span data-ttu-id="870df-103">Fonction RECTSECT</span><span class="sxs-lookup"><span data-stu-id="870df-103">RECTSECT Function</span></span>

<span data-ttu-id="870df-104">Calcule le secteur d'un rectangle associé à *x* et *y* et renvoie un entier compris entre 0 et 4 indiquant le secteur.</span><span class="sxs-lookup"><span data-stu-id="870df-104">Calculates the sector of a rectangle associated with  *x*  and  *y*  and returns an integer 0 to 4, indicating the sector.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="870df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="870df-105">Syntax</span></span>

<span data-ttu-id="870df-106">RECTSECT (\* \* *largeur* \* \*, \* \* *hauteur* \* \*, \* \* *x* \* \*, \* \* *y* \* \*, \* \* *option* \* \*)</span><span class="sxs-lookup"><span data-stu-id="870df-106">RECTSECT(\*\* *width* \*\*, \*\* *height* \*\*, \*\* *x* \*\*, \*\* *y* \*\*, \*\* *option* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="870df-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="870df-107">Parameters</span></span>

|<span data-ttu-id="870df-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="870df-108">**Name**</span></span>|<span data-ttu-id="870df-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="870df-109">**Required/Optional**</span></span>|<span data-ttu-id="870df-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="870df-110">**Data Type**</span></span>|<span data-ttu-id="870df-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="870df-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="870df-112">_width_</span><span class="sxs-lookup"><span data-stu-id="870df-112">_width_</span></span> <br/> |<span data-ttu-id="870df-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="870df-113">Required</span></span>  <br/> |<span data-ttu-id="870df-114">**String**</span><span class="sxs-lookup"><span data-stu-id="870df-114">**String**</span></span> <br/> |<span data-ttu-id="870df-115">Largeur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="870df-115">Width of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="870df-116">_height_</span><span class="sxs-lookup"><span data-stu-id="870df-116">_height_</span></span> <br/> |<span data-ttu-id="870df-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="870df-117">Required</span></span>  <br/> |<span data-ttu-id="870df-118">**String**</span><span class="sxs-lookup"><span data-stu-id="870df-118">**String**</span></span> <br/> |<span data-ttu-id="870df-119">Hauteur du rectangle.</span><span class="sxs-lookup"><span data-stu-id="870df-119">Height of the rectangle.</span></span>  <br/> |
| <span data-ttu-id="870df-120">_x_</span><span class="sxs-lookup"><span data-stu-id="870df-120">_x_</span></span> <br/> |<span data-ttu-id="870df-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="870df-121">Required</span></span>  <br/> |<span data-ttu-id="870df-122">**String**</span><span class="sxs-lookup"><span data-stu-id="870df-122">**String**</span></span> <br/> |<span data-ttu-id="870df-123">Coordonnée x.</span><span class="sxs-lookup"><span data-stu-id="870df-123">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="870df-124">_y_</span><span class="sxs-lookup"><span data-stu-id="870df-124">_y_</span></span> <br/> |<span data-ttu-id="870df-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="870df-125">Required</span></span>  <br/> |<span data-ttu-id="870df-126">**String**</span><span class="sxs-lookup"><span data-stu-id="870df-126">**String**</span></span> <br/> |<span data-ttu-id="870df-127">Coordonnée y.</span><span class="sxs-lookup"><span data-stu-id="870df-127">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="870df-128">_option_</span><span class="sxs-lookup"><span data-stu-id="870df-128">_option_</span></span> <br/> |<span data-ttu-id="870df-129">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="870df-129">Required</span></span>  <br/> |<span data-ttu-id="870df-130">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="870df-130">**Boolean**</span></span> <br/> |<span data-ttu-id="870df-p101">Indique comment les points des diagonales sont traités. Attribuez la valeur 0 pour utiliser les secteurs de gauche et de droite pour les points d’une diagonale. Attribuez la valeur 1 pour utiliser les secteurs du haut et du bas.</span><span class="sxs-lookup"><span data-stu-id="870df-p101">Specifies how points that fall on the diagonals are treated. Set the value to 0 to use the left and right sectors for points on a diagonal. Set the value to 1 to use the top and bottom sectors for points on a diagonal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="870df-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="870df-134">Remarks</span></span>

<span data-ttu-id="870df-135">Imaginez un rectangle qui a une *largeur* et une *hauteur* , et un point (*x, y*) à partir du centre du rectangle.</span><span class="sxs-lookup"><span data-stu-id="870df-135">Consider a rectangle that has a  *width*  and a  *height*  , and a point (*x,y*) from the center point of the rectangle.</span></span> <span data-ttu-id="870df-136">Tracez des lignes diagonales reliant les coins du rectangle pour le diviser en quatre secteurs avec un point central.</span><span class="sxs-lookup"><span data-stu-id="870df-136">Draw diagonal lines through the corners of the rectangle to divide it into four sectors and a center point.</span></span> <span data-ttu-id="870df-137">Les secteurs de 0 à 4 représentent respectivement le point central, la droite, le haut, le bas et la gauche.</span><span class="sxs-lookup"><span data-stu-id="870df-137">The sectors 0 through 4 represent the center-point, right, top, left, and bottom respectively.</span></span> 
  
![Les secteurs 0 à 4 représentent respectivement le point central, droit, supérieur, gauche et inférieur](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a><span data-ttu-id="870df-139">Exemple</span><span class="sxs-lookup"><span data-stu-id="870df-139">Example</span></span>

<span data-ttu-id="870df-140">RECTSECT(25,4 mm; 50,8 mm; 25,4 mm; -177,8 mm; 0)</span><span class="sxs-lookup"><span data-stu-id="870df-140">RECTSECT(1 in, 2 in, 1 in, -7 in, 0)</span></span> 
  
<span data-ttu-id="870df-141">Renvoie 4.</span><span class="sxs-lookup"><span data-stu-id="870df-141">Returns 4.</span></span> 
  

