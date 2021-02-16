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
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo.
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426295"
---
# <a name="polyline-function"></a><span data-ttu-id="99bb2-104">Fonction POLYLINE</span><span class="sxs-lookup"><span data-stu-id="99bb2-104">POLYLINE Function</span></span>

<span data-ttu-id="99bb2-105">Renvoie une polyligne.</span><span class="sxs-lookup"><span data-stu-id="99bb2-105">Returns a polyline.</span></span> <span data-ttu-id="99bb2-106">Cette fonction est utilisée dans la cellule A des lignes de géométrie PolyLineTo.</span><span class="sxs-lookup"><span data-stu-id="99bb2-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="99bb2-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="99bb2-107">Syntax</span></span>

<span data-ttu-id="99bb2-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span><span class="sxs-lookup"><span data-stu-id="99bb2-108">POLYLINE(\*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="99bb2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="99bb2-109">Parameters</span></span>

|<span data-ttu-id="99bb2-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="99bb2-110">**Name**</span></span>|<span data-ttu-id="99bb2-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="99bb2-111">**Required/Optional**</span></span>|<span data-ttu-id="99bb2-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="99bb2-112">**Data Type**</span></span>|<span data-ttu-id="99bb2-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="99bb2-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="99bb2-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="99bb2-114">_xType_</span></span> <br/> |<span data-ttu-id="99bb2-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="99bb2-115">Required</span></span>  <br/> |<span data-ttu-id="99bb2-116">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="99bb2-116">**Boolean**</span></span> <br/> |<span data-ttu-id="99bb2-117">Indique comment interpréter les _données d’entrée x._</span><span class="sxs-lookup"><span data-stu-id="99bb2-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="99bb2-118">Si  _xType est_ 0, les  _données x_ d’entrée sont interprétées comme un pourcentage de la largeur.</span><span class="sxs-lookup"><span data-stu-id="99bb2-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="99bb2-119">Si  _xType est_ 1, les  _données x_ d’entrée sont interprétées comme une coordonnée locale.</span><span class="sxs-lookup"><span data-stu-id="99bb2-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="99bb2-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="99bb2-120">_yType_</span></span> <br/> |<span data-ttu-id="99bb2-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="99bb2-121">Required</span></span>  <br/> |<span data-ttu-id="99bb2-122">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="99bb2-122">**Boolean**</span></span> <br/> |<span data-ttu-id="99bb2-123">Indique comment interpréter les données _d’entrée y._</span><span class="sxs-lookup"><span data-stu-id="99bb2-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="99bb2-124">Si  _yType est_ 0, l’entrée  _y_-data est interprétée comme un pourcentage de height.</span><span class="sxs-lookup"><span data-stu-id="99bb2-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="99bb2-125">Si  _yType est_ 1, l’entrée  _y_-data est interprétée comme une coordonnée locale.</span><span class="sxs-lookup"><span data-stu-id="99bb2-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="99bb2-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="99bb2-126">_x1_</span></span> <br/> |<span data-ttu-id="99bb2-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="99bb2-127">Required</span></span>  <br/> |<span data-ttu-id="99bb2-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="99bb2-128">**Number**</span></span> <br/> | <span data-ttu-id="99bb2-129">Coordonnée _x._</span><span class="sxs-lookup"><span data-stu-id="99bb2-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="99bb2-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="99bb2-130">_y1_</span></span> <br/> |<span data-ttu-id="99bb2-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="99bb2-131">Required</span></span>  <br/> |<span data-ttu-id="99bb2-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="99bb2-132">**Number**</span></span> <br/> |<span data-ttu-id="99bb2-133">Coordonnée _y._</span><span class="sxs-lookup"><span data-stu-id="99bb2-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99bb2-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="99bb2-134">Remarks</span></span>

<span data-ttu-id="99bb2-135">Pour chaque argument  *x,*  il doit y avoir un argument  *y*  ; Sinon, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="99bb2-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="99bb2-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="99bb2-136">Example</span></span>

<span data-ttu-id="99bb2-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="99bb2-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="99bb2-138">Renvoie un rectangle de dimensions Largeur x Hauteur.</span><span class="sxs-lookup"><span data-stu-id="99bb2-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

