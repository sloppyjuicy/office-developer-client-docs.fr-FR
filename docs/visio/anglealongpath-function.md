---
title: ANGLEALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: Renvoie l’angle de la tangente du chemin à un point donné.
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407325"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="57feb-103">Fonction ANGLEALONGPATH</span><span class="sxs-lookup"><span data-stu-id="57feb-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="57feb-104">Renvoie l’angle de la tangente du chemin à un point donné.</span><span class="sxs-lookup"><span data-stu-id="57feb-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="57feb-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="57feb-105">Version Information</span></span>

<span data-ttu-id="57feb-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="57feb-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="57feb-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="57feb-107">Syntax</span></span>

<span data-ttu-id="57feb-108">ANGLEALONGPATH (\* \* *section* \* \*, \* \* *voyages* \* \* \* \* *[, segment]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="57feb-108">ANGLEALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="57feb-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="57feb-109">Parameters</span></span>

|<span data-ttu-id="57feb-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="57feb-110">**Name**</span></span>|<span data-ttu-id="57feb-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="57feb-111">**Required/Optional**</span></span>|<span data-ttu-id="57feb-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="57feb-112">**Data Type**</span></span>|<span data-ttu-id="57feb-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="57feb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="57feb-114">_section_</span><span class="sxs-lookup"><span data-stu-id="57feb-114">_section_</span></span> <br/> |<span data-ttu-id="57feb-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="57feb-115">Required</span></span>  <br/> |<span data-ttu-id="57feb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="57feb-116">**String**</span></span> <br/> |<span data-ttu-id="57feb-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="57feb-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="57feb-118">_poche_</span><span class="sxs-lookup"><span data-stu-id="57feb-118">_travel_</span></span> <br/> |<span data-ttu-id="57feb-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="57feb-119">Required</span></span>  <br/> |<span data-ttu-id="57feb-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="57feb-120">**Double**</span></span> <br/> |<span data-ttu-id="57feb-121">Pourcentage le long du chemin du point de début au point de fin.</span><span class="sxs-lookup"><span data-stu-id="57feb-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="57feb-122">La valeur doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="57feb-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="57feb-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="57feb-123">_segment_</span></span> <br/> |<span data-ttu-id="57feb-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="57feb-124">Optional</span></span>  <br/> |<span data-ttu-id="57feb-125">**Integer**</span><span class="sxs-lookup"><span data-stu-id="57feb-125">**Integer**</span></span> <br/> |<span data-ttu-id="57feb-126">Segment de base 1 du chemin sur lequel calculer l’angle de la tangente.</span><span class="sxs-lookup"><span data-stu-id="57feb-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="57feb-127">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="57feb-127">Return value</span></span>

 <span data-ttu-id="57feb-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="57feb-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="57feb-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="57feb-129">Remarks</span></span>

<span data-ttu-id="57feb-130">Si vous incluez une valeur de _segment_ , ANGLEALONGPATH renvoie la valeur de ce segment uniquement.</span><span class="sxs-lookup"><span data-stu-id="57feb-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="57feb-131">Si vous incluez une valeur de _segment_ , ANGLEALONGPATH détermine le point de la tangente à l'aide de _voyages_ pour calculer le pourcentage de percertification le long du _segment_.</span><span class="sxs-lookup"><span data-stu-id="57feb-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="57feb-132">Si l'une des _sections_ ou le _segment_ n'existe pas, Microsoft Visio renvoie #REF!.</span><span class="sxs-lookup"><span data-stu-id="57feb-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

