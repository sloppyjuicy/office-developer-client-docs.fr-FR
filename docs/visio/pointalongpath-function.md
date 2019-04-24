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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348257"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="a3624-103">Fonction POINTALONGPATH</span><span class="sxs-lookup"><span data-stu-id="a3624-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="a3624-104">Renvoie les coordonnées d’un point du chemin, ou d’un décalage par rapport à ce chemin.</span><span class="sxs-lookup"><span data-stu-id="a3624-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a3624-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="a3624-105">Version Information</span></span>

<span data-ttu-id="a3624-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a3624-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a3624-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a3624-107">Syntax</span></span>

<span data-ttu-id="a3624-108">POINTALONGPATH (\* \* *section* \* \*, \* \* *voyages* \* \* \* \* *[, décalage]* \* \* \* \* *[, segment]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a3624-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a3624-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a3624-109">Parameters</span></span>

|<span data-ttu-id="a3624-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a3624-110">**Name**</span></span>|<span data-ttu-id="a3624-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a3624-111">**Required/Optional**</span></span>|<span data-ttu-id="a3624-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a3624-112">**Data Type**</span></span>|<span data-ttu-id="a3624-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="a3624-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a3624-114">_section_</span><span class="sxs-lookup"><span data-stu-id="a3624-114">_section_</span></span> <br/> |<span data-ttu-id="a3624-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3624-115">Required</span></span>  <br/> |<span data-ttu-id="a3624-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a3624-116">**String**</span></span> <br/> |<span data-ttu-id="a3624-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="a3624-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="a3624-118">_poche_</span><span class="sxs-lookup"><span data-stu-id="a3624-118">_travel_</span></span> <br/> |<span data-ttu-id="a3624-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a3624-119">Required</span></span>  <br/> |<span data-ttu-id="a3624-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="a3624-120">**Double**</span></span> <br/> |<span data-ttu-id="a3624-121">Pourcentage du chemin parcouru du point de début au point de fin qui identifie le point.</span><span class="sxs-lookup"><span data-stu-id="a3624-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="a3624-122">La valeur doit être comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="a3624-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="a3624-123">_compensé_</span><span class="sxs-lookup"><span data-stu-id="a3624-123">_offset_</span></span> <br/> |<span data-ttu-id="a3624-124">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a3624-124">Optional</span></span>  <br/> |<span data-ttu-id="a3624-125">**Double**</span><span class="sxs-lookup"><span data-stu-id="a3624-125">**Double**</span></span> <br/> |<span data-ttu-id="a3624-126">Distance dont le point est décalé par rapport au chemin.</span><span class="sxs-lookup"><span data-stu-id="a3624-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="a3624-127">Voir la section Remarques pour plus d’informations.</span><span class="sxs-lookup"><span data-stu-id="a3624-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="a3624-128">_segment_</span><span class="sxs-lookup"><span data-stu-id="a3624-128">_segment_</span></span> <br/> |<span data-ttu-id="a3624-129">Facultatif</span><span class="sxs-lookup"><span data-stu-id="a3624-129">Optional</span></span>  <br/> |<span data-ttu-id="a3624-130">**Integer**</span><span class="sxs-lookup"><span data-stu-id="a3624-130">**Integer**</span></span> <br/> |<span data-ttu-id="a3624-131">Segment de base 1 du chemin sur lequel calculer les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="a3624-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a3624-132">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a3624-132">Return value</span></span>

 <span data-ttu-id="a3624-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="a3624-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a3624-134">Remarques</span><span class="sxs-lookup"><span data-stu-id="a3624-134">Remarks</span></span>

<span data-ttu-id="a3624-135">Si la _section_ ou le _segment_ n'existe pas, Microsoft Visio renvoie #REF!.</span><span class="sxs-lookup"><span data-stu-id="a3624-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="a3624-136">Les valeurs de *décalage* positives spécifient les points à gauche du sens de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a3624-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="a3624-137">Les valeurs de *décalage* négatives spécifient les points à droite du sens de déplacement.</span><span class="sxs-lookup"><span data-stu-id="a3624-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="a3624-138">Un **Point** représente une paire classée de coordonnées géométriques (*x,y*) sous forme de valeur unique.</span><span class="sxs-lookup"><span data-stu-id="a3624-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

