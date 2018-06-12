---
title: DISTTOPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788501"
---
# <a name="disttopath-function"></a><span data-ttu-id="01e9f-103">DISTTOPATH, fonction</span><span class="sxs-lookup"><span data-stu-id="01e9f-103">DISTTOPATH Function</span></span>

<span data-ttu-id="01e9f-104">Renvoie la distance la plus courte entre le point représenté par les coordonnées spécifiées et un point du chemin.</span><span class="sxs-lookup"><span data-stu-id="01e9f-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="01e9f-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="01e9f-105">Version Information</span></span>

<span data-ttu-id="01e9f-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="01e9f-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="01e9f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="01e9f-107">Syntax</span></span>

<span data-ttu-id="01e9f-108">DISTTOPATH (** *section* **, ** *x* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="01e9f-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="01e9f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="01e9f-109">Parameters</span></span>

|<span data-ttu-id="01e9f-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="01e9f-110">**Name**</span></span>|<span data-ttu-id="01e9f-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="01e9f-111">**Required/Optional**</span></span>|<span data-ttu-id="01e9f-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="01e9f-112">**Data Type**</span></span>|<span data-ttu-id="01e9f-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="01e9f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="01e9f-114">_section_</span><span class="sxs-lookup"><span data-stu-id="01e9f-114">_section_</span></span> <br/> |<span data-ttu-id="01e9f-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="01e9f-115">Required</span></span>  <br/> |<span data-ttu-id="01e9f-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="01e9f-116">**String**</span></span> <br/> |<span data-ttu-id="01e9f-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="01e9f-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="01e9f-118">_x_</span><span class="sxs-lookup"><span data-stu-id="01e9f-118">_x_</span></span> <br/> |<span data-ttu-id="01e9f-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="01e9f-119">Required</span></span>  <br/> |<span data-ttu-id="01e9f-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="01e9f-120">**Double**</span></span> <br/> |<span data-ttu-id="01e9f-121">_X_-coordonnées du point.</span><span class="sxs-lookup"><span data-stu-id="01e9f-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="01e9f-122">_y_</span><span class="sxs-lookup"><span data-stu-id="01e9f-122">_y_</span></span> <br/> |<span data-ttu-id="01e9f-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="01e9f-123">Required</span></span>  <br/> |<span data-ttu-id="01e9f-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="01e9f-124">**Double**</span></span> <br/> |<span data-ttu-id="01e9f-125">La valeur _y_-coordonnées du point.</span><span class="sxs-lookup"><span data-stu-id="01e9f-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="01e9f-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="01e9f-126">Return value</span></span>

 <span data-ttu-id="01e9f-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="01e9f-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="01e9f-128">Note</span><span class="sxs-lookup"><span data-stu-id="01e9f-128">Remarks</span></span>

<span data-ttu-id="01e9f-129">Microsoft Visio renvoie #REF !</span><span class="sxs-lookup"><span data-stu-id="01e9f-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="01e9f-130">Si la _section_ n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="01e9f-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="01e9f-131">La valeur renvoyée est positive si le point se situe à gauche par rapport au sens de déplacement, et négative s’il se situe à droite.</span><span class="sxs-lookup"><span data-stu-id="01e9f-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

