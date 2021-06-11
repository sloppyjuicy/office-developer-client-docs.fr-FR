---
title: POINTALONGPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430482"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="cdfbd-103">Fonction POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="cdfbd-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="cdfbd-104">Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="cdfbd-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="cdfbd-105">Version Information</span></span>

<span data-ttu-id="cdfbd-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="cdfbd-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cdfbd-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cdfbd-107">Syntax</span></span>

<span data-ttu-id="cdfbd-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="cdfbd-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cdfbd-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cdfbd-109">Parameters</span></span>

|<span data-ttu-id="cdfbd-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-110">**Name**</span></span>|<span data-ttu-id="cdfbd-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-111">**Required/Optional**</span></span>|<span data-ttu-id="cdfbd-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-112">**Data Type**</span></span>|<span data-ttu-id="cdfbd-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cdfbd-114">_section_</span><span class="sxs-lookup"><span data-stu-id="cdfbd-114">_section_</span></span> <br/> |<span data-ttu-id="cdfbd-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cdfbd-115">Required</span></span>  <br/> |<span data-ttu-id="cdfbd-116">**String**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-116">**String**</span></span> <br/> |<span data-ttu-id="cdfbd-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="cdfbd-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="cdfbd-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="cdfbd-118">_travel_</span></span> <br/> |<span data-ttu-id="cdfbd-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cdfbd-119">Required</span></span>  <br/> |<span data-ttu-id="cdfbd-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-120">**Double**</span></span> <br/> |<span data-ttu-id="cdfbd-p101">Pourcentage du chemin parcouru du point de début au point de fin qui identifie le point. La valeur doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="cdfbd-123">_offset_</span><span class="sxs-lookup"><span data-stu-id="cdfbd-123">_offset_</span></span> <br/> |<span data-ttu-id="cdfbd-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="cdfbd-124">Optional</span></span>  <br/> |<span data-ttu-id="cdfbd-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-125">**Double**</span></span> <br/> |<span data-ttu-id="cdfbd-p102">Distance dont le point est décalé par rapport au chemin. Voir la section Remarques pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="cdfbd-128">_segment_</span><span class="sxs-lookup"><span data-stu-id="cdfbd-128">_segment_</span></span> <br/> |<span data-ttu-id="cdfbd-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="cdfbd-129">Optional</span></span>  <br/> |<span data-ttu-id="cdfbd-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-130">**Integer**</span></span> <br/> |<span data-ttu-id="cdfbd-131">Segment de base 1 du chemin sur lequel calculer les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cdfbd-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cdfbd-132">Return value</span></span>

 <span data-ttu-id="cdfbd-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="cdfbd-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cdfbd-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="cdfbd-134">Remarks</span></span>

<span data-ttu-id="cdfbd-135">Si _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF!.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="cdfbd-136">Les  *valeurs de*  décalage positif spécifient des points à gauche du sens de déplacement.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="cdfbd-137">Les  *valeurs de*  décalage négatives spécifient des points à droite de la direction du déplacement.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="cdfbd-138">Un **Point** représente une paire classée de coordonnées géométriques (*x,y*) sous forme de valeur unique.</span><span class="sxs-lookup"><span data-stu-id="cdfbd-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

