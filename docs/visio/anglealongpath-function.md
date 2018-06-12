---
title: ANGLEALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788043"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="90667-103">ANGLEALONGPATH, fonction</span><span class="sxs-lookup"><span data-stu-id="90667-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="90667-104">Renvoie l’angle de la tangente du chemin à un point donné.</span><span class="sxs-lookup"><span data-stu-id="90667-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="90667-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="90667-105">Version Information</span></span>

<span data-ttu-id="90667-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="90667-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="90667-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="90667-107">Syntax</span></span>

<span data-ttu-id="90667-108">ANGLEALONGPATH (** *section* **, ** *voyage* ** ** *[, segment]* **)</span><span class="sxs-lookup"><span data-stu-id="90667-108">ANGLEALONGPATH(** *section* **, ** *travel* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="90667-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="90667-109">Parameters</span></span>

|<span data-ttu-id="90667-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="90667-110">**Name**</span></span>|<span data-ttu-id="90667-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="90667-111">**Required/Optional**</span></span>|<span data-ttu-id="90667-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="90667-112">**Data Type**</span></span>|<span data-ttu-id="90667-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="90667-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="90667-114">_section_</span><span class="sxs-lookup"><span data-stu-id="90667-114">_section_</span></span> <br/> |<span data-ttu-id="90667-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="90667-115">Required</span></span>  <br/> |<span data-ttu-id="90667-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="90667-116">**String**</span></span> <br/> |<span data-ttu-id="90667-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="90667-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="90667-118">_frais de déplacement_</span><span class="sxs-lookup"><span data-stu-id="90667-118">_travel_</span></span> <br/> |<span data-ttu-id="90667-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="90667-119">Required</span></span>  <br/> |<span data-ttu-id="90667-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="90667-120">**Double**</span></span> <br/> |<span data-ttu-id="90667-p101">Pourcentage le long du chemin du point de début au point de fin. La valeur doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="90667-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="90667-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="90667-123">_segment_</span></span> <br/> |<span data-ttu-id="90667-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="90667-124">Optional</span></span>  <br/> |<span data-ttu-id="90667-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="90667-125">**Integer**</span></span> <br/> |<span data-ttu-id="90667-126">Segment de base 1 du chemin sur lequel calculer l’angle de la tangente.</span><span class="sxs-lookup"><span data-stu-id="90667-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="90667-127">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="90667-127">Return value</span></span>

 <span data-ttu-id="90667-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="90667-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="90667-129">Note</span><span class="sxs-lookup"><span data-stu-id="90667-129">Remarks</span></span>

<span data-ttu-id="90667-130">Si vous incluez une valeur de _segment_ , ANGLEALONGPATH renvoie la valeur de ce segment uniquement.</span><span class="sxs-lookup"><span data-stu-id="90667-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="90667-131">Si vous incluez une valeur de _segment_ , ANGLEALONGPATH détermine le point de la tangente à l’aide de _déplacement_ pour calculer le pourcentage le long de _segment_du.</span><span class="sxs-lookup"><span data-stu-id="90667-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="90667-132">Si la _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF !.</span><span class="sxs-lookup"><span data-stu-id="90667-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

