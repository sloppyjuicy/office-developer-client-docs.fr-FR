---
title: PAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: Renvoie les coordonnées x, y d’un point dans le système de coordonnées du parent de la forme.
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789221"
---
# <a name="par-function"></a><span data-ttu-id="777f6-103">PAR, fonction</span><span class="sxs-lookup"><span data-stu-id="777f6-103">PAR Function</span></span>

<span data-ttu-id="777f6-104">Renvoie les coordonnées _x, y_ d’un point dans le système de coordonnées du parent de la forme.</span><span class="sxs-lookup"><span data-stu-id="777f6-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="777f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="777f6-105">Syntax</span></span>

<span data-ttu-id="777f6-106">Valeur nominale (** *point* **)</span><span class="sxs-lookup"><span data-stu-id="777f6-106">PAR(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="777f6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="777f6-107">Parameters</span></span>

|<span data-ttu-id="777f6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="777f6-108">**Name**</span></span>|<span data-ttu-id="777f6-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="777f6-109">**Required/Optional**</span></span>|<span data-ttu-id="777f6-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="777f6-110">**Data Type**</span></span>|<span data-ttu-id="777f6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="777f6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="777f6-112">_point_</span><span class="sxs-lookup"><span data-stu-id="777f6-112">_point_</span></span> <br/> |<span data-ttu-id="777f6-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="777f6-113">Required</span></span>  <br/> |<span data-ttu-id="777f6-114">**Numéro,**</span><span class="sxs-lookup"><span data-stu-id="777f6-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="777f6-115">Coordonnées du point dans le système de coordonnées de la forme actuelle</span><span class="sxs-lookup"><span data-stu-id="777f6-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="777f6-116">Note</span><span class="sxs-lookup"><span data-stu-id="777f6-116">Remarks</span></span>

<span data-ttu-id="777f6-117">Dans Microsoft Visio, un point est une valeur single qui représente une paire de *x* et *y* -coordonnées.</span><span class="sxs-lookup"><span data-stu-id="777f6-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="777f6-118">Si la forme est un groupe, son parent est le groupe.</span><span class="sxs-lookup"><span data-stu-id="777f6-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="777f6-119">Si la forme n’est pas dans un groupe, son parent est la page.</span><span class="sxs-lookup"><span data-stu-id="777f6-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="777f6-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="777f6-120">Example</span></span>

<span data-ttu-id="777f6-121">PAR(Pnt(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="777f6-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="777f6-p102">Dans cette expression, PNT convertit un couple de coordonnées de la forme active en un point. La fonction PAR convertit ensuite le point en un couple de coordonnées par rapport au coin inférieur gauche de la page contenant la forme active.</span><span class="sxs-lookup"><span data-stu-id="777f6-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

