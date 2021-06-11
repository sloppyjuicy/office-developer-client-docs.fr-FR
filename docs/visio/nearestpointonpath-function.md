---
title: NEARESTPOINTONPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407332"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="11095-103">Fonction NEARESTPOINTONPATH</span><span class="sxs-lookup"><span data-stu-id="11095-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="11095-104">Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="11095-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="11095-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="11095-105">Version Information</span></span>

<span data-ttu-id="11095-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="11095-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="11095-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11095-107">Syntax</span></span>

<span data-ttu-id="11095-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span><span class="sxs-lookup"><span data-stu-id="11095-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="11095-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11095-109">Parameters</span></span>

|<span data-ttu-id="11095-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="11095-110">**Name**</span></span>|<span data-ttu-id="11095-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="11095-111">**Required/Optional**</span></span>|<span data-ttu-id="11095-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="11095-112">**Data Type**</span></span>|<span data-ttu-id="11095-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="11095-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="11095-114">_section_</span><span class="sxs-lookup"><span data-stu-id="11095-114">_section_</span></span> <br/> |<span data-ttu-id="11095-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="11095-115">Required</span></span>  <br/> |<span data-ttu-id="11095-116">**String**</span><span class="sxs-lookup"><span data-stu-id="11095-116">**String**</span></span> <br/> |<span data-ttu-id="11095-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="11095-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="11095-118">_x_</span><span class="sxs-lookup"><span data-stu-id="11095-118">_x_</span></span> <br/> |<span data-ttu-id="11095-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="11095-119">Required</span></span>  <br/> |<span data-ttu-id="11095-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="11095-120">**Double**</span></span> <br/> |<span data-ttu-id="11095-121">Coordonnée  _x_ du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="11095-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="11095-122">_y_</span><span class="sxs-lookup"><span data-stu-id="11095-122">_y_</span></span> <br/> |<span data-ttu-id="11095-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="11095-123">Required</span></span>  <br/> |<span data-ttu-id="11095-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="11095-124">**Double**</span></span> <br/> |<span data-ttu-id="11095-125">Coordonnée  _y_ du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="11095-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="11095-126">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="11095-126">Return value</span></span>

 <span data-ttu-id="11095-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="11095-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="11095-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="11095-128">Remarks</span></span>

<span data-ttu-id="11095-129">Si _la section_ n’existe pas, Microsoft Visio renvoie #REF!.</span><span class="sxs-lookup"><span data-stu-id="11095-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

