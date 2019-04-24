---
title: POLYLINE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie de PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348278"
---
# <a name="polyline-function"></a><span data-ttu-id="42cc6-104">Fonction POLYLINE</span><span class="sxs-lookup"><span data-stu-id="42cc6-104">POLYLINE Function</span></span>

<span data-ttu-id="42cc6-105">Renvoie une polyligne.</span><span class="sxs-lookup"><span data-stu-id="42cc6-105">Returns a polyline.</span></span> <span data-ttu-id="42cc6-106">Cette fonction est utilisée dans la cellule A des lignes de géométrie de PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="42cc6-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="42cc6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="42cc6-107">Syntax</span></span>

<span data-ttu-id="42cc6-108">PolyLINE (\* \* *xtype* \* \*, \* \* *yType* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*...)</span><span class="sxs-lookup"><span data-stu-id="42cc6-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="42cc6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="42cc6-109">Parameters</span></span>

|<span data-ttu-id="42cc6-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="42cc6-110">**Name**</span></span>|<span data-ttu-id="42cc6-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="42cc6-111">**Required/Optional**</span></span>|<span data-ttu-id="42cc6-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="42cc6-112">**Data Type**</span></span>|<span data-ttu-id="42cc6-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="42cc6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="42cc6-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="42cc6-114">_xType_</span></span> <br/> |<span data-ttu-id="42cc6-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="42cc6-115">Required</span></span>  <br/> |<span data-ttu-id="42cc6-116">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="42cc6-116">**Boolean**</span></span> <br/> |<span data-ttu-id="42cc6-117">Indique comment interpréter les données _x_ d'entrée.</span><span class="sxs-lookup"><span data-stu-id="42cc6-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="42cc6-118">Si _xtype_ a la valeur 0, les données _x_d'entrée sont interprétées comme un pourcentage de la largeur.</span><span class="sxs-lookup"><span data-stu-id="42cc6-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="42cc6-119">Si _xtype_ a la 1, les données _x_d'entrée sont interprétées comme une coordonnée locale.</span><span class="sxs-lookup"><span data-stu-id="42cc6-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="42cc6-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="42cc6-120">_yType_</span></span> <br/> |<span data-ttu-id="42cc6-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="42cc6-121">Required</span></span>  <br/> |<span data-ttu-id="42cc6-122">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="42cc6-122">**Boolean**</span></span> <br/> |<span data-ttu-id="42cc6-123">Indique comment interpréter les données de l'entrée _y_.</span><span class="sxs-lookup"><span data-stu-id="42cc6-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="42cc6-124">Si _yType_ a la valeur 0, les données _y_entrées sont interprétées comme un pourcentage de la hauteur.</span><span class="sxs-lookup"><span data-stu-id="42cc6-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="42cc6-125">Si _yType_ a la valeurs 1, les données _y_entrées sont interprétées comme une coordonnée locale.</span><span class="sxs-lookup"><span data-stu-id="42cc6-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="42cc6-126">_mâle_</span><span class="sxs-lookup"><span data-stu-id="42cc6-126">_x1_</span></span> <br/> |<span data-ttu-id="42cc6-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="42cc6-127">Required</span></span>  <br/> |<span data-ttu-id="42cc6-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="42cc6-128">**Number**</span></span> <br/> | <span data-ttu-id="42cc6-129">Coordonnée _x_.</span><span class="sxs-lookup"><span data-stu-id="42cc6-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="42cc6-130">_Y1_</span><span class="sxs-lookup"><span data-stu-id="42cc6-130">_y1_</span></span> <br/> |<span data-ttu-id="42cc6-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="42cc6-131">Required</span></span>  <br/> |<span data-ttu-id="42cc6-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="42cc6-132">**Number**</span></span> <br/> |<span data-ttu-id="42cc6-133">Coordonnée _y_.</span><span class="sxs-lookup"><span data-stu-id="42cc6-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="42cc6-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="42cc6-134">Remarks</span></span>

<span data-ttu-id="42cc6-135">Pour chaque argument *x* , il doit y avoir un argument *y* ; Sinon, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="42cc6-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="42cc6-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="42cc6-136">Example</span></span>

<span data-ttu-id="42cc6-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="42cc6-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="42cc6-138">Renvoie un rectangle de dimensions Largeur x Hauteur.</span><span class="sxs-lookup"><span data-stu-id="42cc6-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

