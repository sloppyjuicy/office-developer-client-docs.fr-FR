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
description: Renvoie une polyligne. Cette fonction est utilisée dans la cellule A de PolyligneVers géométrie.
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789258"
---
# <a name="polyline-function"></a><span data-ttu-id="e30d7-104">POLYLINE, fonction</span><span class="sxs-lookup"><span data-stu-id="e30d7-104">POLYLINE Function</span></span>

<span data-ttu-id="e30d7-105">Renvoie une polyligne.</span><span class="sxs-lookup"><span data-stu-id="e30d7-105">Returns a polyline.</span></span> <span data-ttu-id="e30d7-106">Cette fonction est utilisée dans la cellule A de PolyligneVers géométrie.</span><span class="sxs-lookup"><span data-stu-id="e30d7-106">This function is used in the A cell of PolyLineTo geometry rows.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e30d7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e30d7-107">Syntax</span></span>

<span data-ttu-id="e30d7-108">POLYLINE (** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span><span class="sxs-lookup"><span data-stu-id="e30d7-108">POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e30d7-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e30d7-109">Parameters</span></span>

|<span data-ttu-id="e30d7-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e30d7-110">**Name**</span></span>|<span data-ttu-id="e30d7-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="e30d7-111">**Required/Optional**</span></span>|<span data-ttu-id="e30d7-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="e30d7-112">**Data Type**</span></span>|<span data-ttu-id="e30d7-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="e30d7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e30d7-114">_xType_</span><span class="sxs-lookup"><span data-stu-id="e30d7-114">_xType_</span></span> <br/> |<span data-ttu-id="e30d7-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e30d7-115">Required</span></span>  <br/> |<span data-ttu-id="e30d7-116">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e30d7-116">**Boolean**</span></span> <br/> |<span data-ttu-id="e30d7-117">Spécifie comment interpréter les données _x_ entrées.</span><span class="sxs-lookup"><span data-stu-id="e30d7-117">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="e30d7-118">Si _xType_ a la valeur 0, l’entrée _x_-données sont interprétées comme un pourcentage de largeur.</span><span class="sxs-lookup"><span data-stu-id="e30d7-118">If  _xType_ is 0, the input  _x_-data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="e30d7-119">Si _xType_ a la valeur 1, l’entrée _x_-données sont interprétées comme une coordonnée locale.</span><span class="sxs-lookup"><span data-stu-id="e30d7-119">If  _xType_ is 1, the input  _x_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="e30d7-120">_yType_</span><span class="sxs-lookup"><span data-stu-id="e30d7-120">_yType_</span></span> <br/> |<span data-ttu-id="e30d7-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e30d7-121">Required</span></span>  <br/> |<span data-ttu-id="e30d7-122">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="e30d7-122">**Boolean**</span></span> <br/> |<span data-ttu-id="e30d7-123">Spécifie comment interpréter les _y_-saisie.</span><span class="sxs-lookup"><span data-stu-id="e30d7-123">Specifies how to interpret the  _y_-input data.</span></span> <span data-ttu-id="e30d7-124">Si _yType_ a la valeur 0, l’entrée _y_-données sont interprétées comme un pourcentage de hauteur.</span><span class="sxs-lookup"><span data-stu-id="e30d7-124">If  _yType_ is 0, the input  _y_-data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="e30d7-125">Si _yType_ a la valeur 1, l’entrée _y_-données sont interprétées comme une coordonnée locale.</span><span class="sxs-lookup"><span data-stu-id="e30d7-125">If  _yType_ is 1, the input  _y_-data is interpreted as a local coordinate.</span></span>  <br/> |
| <span data-ttu-id="e30d7-126">_x1_</span><span class="sxs-lookup"><span data-stu-id="e30d7-126">_x1_</span></span> <br/> |<span data-ttu-id="e30d7-127">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e30d7-127">Required</span></span>  <br/> |<span data-ttu-id="e30d7-128">**Number**</span><span class="sxs-lookup"><span data-stu-id="e30d7-128">**Number**</span></span> <br/> | <span data-ttu-id="e30d7-129">_X_-coordonner.</span><span class="sxs-lookup"><span data-stu-id="e30d7-129">An  _x_-coordinate.</span></span>  <br/> |
| <span data-ttu-id="e30d7-130">_y1_</span><span class="sxs-lookup"><span data-stu-id="e30d7-130">_y1_</span></span> <br/> |<span data-ttu-id="e30d7-131">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="e30d7-131">Required</span></span>  <br/> |<span data-ttu-id="e30d7-132">**Number**</span><span class="sxs-lookup"><span data-stu-id="e30d7-132">**Number**</span></span> <br/> |<span data-ttu-id="e30d7-133">_Y_-coordonner.</span><span class="sxs-lookup"><span data-stu-id="e30d7-133">A  _y_-coordinate.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e30d7-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="e30d7-134">Remarks</span></span>

<span data-ttu-id="e30d7-135">Pour chaque argument *x* , il doit exister un argument *y* ; dans le cas contraire, une erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="e30d7-135">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e30d7-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="e30d7-136">Example</span></span>

<span data-ttu-id="e30d7-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="e30d7-137">POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0)</span></span> 
  
<span data-ttu-id="e30d7-138">Renvoie un rectangle de dimensions Largeur x Hauteur.</span><span class="sxs-lookup"><span data-stu-id="e30d7-138">Returns a rectangle of dimensions Width x Height.</span></span> 
  

