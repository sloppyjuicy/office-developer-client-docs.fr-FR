---
title: DISTTOPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427016"
---
# <a name="disttopath-function"></a><span data-ttu-id="c92cd-103">Fonction DISTTOPATH</span><span class="sxs-lookup"><span data-stu-id="c92cd-103">DISTTOPATH Function</span></span>

<span data-ttu-id="c92cd-104">Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.</span><span class="sxs-lookup"><span data-stu-id="c92cd-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="c92cd-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="c92cd-105">Version Information</span></span>

<span data-ttu-id="c92cd-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="c92cd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c92cd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c92cd-107">Syntax</span></span>

<span data-ttu-id="c92cd-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="c92cd-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c92cd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c92cd-109">Parameters</span></span>

|<span data-ttu-id="c92cd-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c92cd-110">**Name**</span></span>|<span data-ttu-id="c92cd-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c92cd-111">**Required/Optional**</span></span>|<span data-ttu-id="c92cd-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c92cd-112">**Data Type**</span></span>|<span data-ttu-id="c92cd-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="c92cd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c92cd-114">_section_</span><span class="sxs-lookup"><span data-stu-id="c92cd-114">_section_</span></span> <br/> |<span data-ttu-id="c92cd-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92cd-115">Required</span></span>  <br/> |<span data-ttu-id="c92cd-116">**String**</span><span class="sxs-lookup"><span data-stu-id="c92cd-116">**String**</span></span> <br/> |<span data-ttu-id="c92cd-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="c92cd-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="c92cd-118">_x_</span><span class="sxs-lookup"><span data-stu-id="c92cd-118">_x_</span></span> <br/> |<span data-ttu-id="c92cd-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92cd-119">Required</span></span>  <br/> |<span data-ttu-id="c92cd-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="c92cd-120">**Double**</span></span> <br/> |<span data-ttu-id="c92cd-121">Coordonnée  _x_ du point.</span><span class="sxs-lookup"><span data-stu-id="c92cd-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="c92cd-122">_y_</span><span class="sxs-lookup"><span data-stu-id="c92cd-122">_y_</span></span> <br/> |<span data-ttu-id="c92cd-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c92cd-123">Required</span></span>  <br/> |<span data-ttu-id="c92cd-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="c92cd-124">**Double**</span></span> <br/> |<span data-ttu-id="c92cd-125">Coordonnée  _y_ du point.</span><span class="sxs-lookup"><span data-stu-id="c92cd-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c92cd-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="c92cd-126">Return value</span></span>

 <span data-ttu-id="c92cd-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="c92cd-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c92cd-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="c92cd-128">Remarks</span></span>

<span data-ttu-id="c92cd-129">Microsoft Visio renvoie #REF!</span><span class="sxs-lookup"><span data-stu-id="c92cd-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="c92cd-130">si  _la section_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="c92cd-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="c92cd-131">La valeur renvoyée est positive si le point se situe à gauche par rapport au sens de déplacement, et négative s’il se situe à droite.</span><span class="sxs-lookup"><span data-stu-id="c92cd-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

