---
title: BOUNDINGBOXRECT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1f66d2b2-ec9e-cd58-7642-96850fe4589e
description: Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.
ms.openlocfilehash: 0018118eb0991fe9dc1da0eb000566b69d8a4b4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418070"
---
# <a name="boundingboxrect-function"></a><span data-ttu-id="aaa03-103">Fonction BOUNDINGBOXRECT</span><span class="sxs-lookup"><span data-stu-id="aaa03-103">BOUNDINGBOXRECT Function</span></span>

<span data-ttu-id="aaa03-104">Renvoie les coordonnées du bord spécifié du cadre englobant de la forme.</span><span class="sxs-lookup"><span data-stu-id="aaa03-104">Returns the coordinate of the specified edge of the shape's bounding box.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="aaa03-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="aaa03-105">Version Information</span></span>

<span data-ttu-id="aaa03-106">Version ajoutée : Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="aaa03-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aaa03-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aaa03-107">Syntax</span></span>

<span data-ttu-id="aaa03-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span><span class="sxs-lookup"><span data-stu-id="aaa03-108">BOUNDINGBOXRECT(\*\* *Index* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aaa03-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aaa03-109">Parameters</span></span>

|<span data-ttu-id="aaa03-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="aaa03-110">**Name**</span></span>|<span data-ttu-id="aaa03-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="aaa03-111">**Required/Optional**</span></span>|<span data-ttu-id="aaa03-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="aaa03-112">**Data Type**</span></span>|<span data-ttu-id="aaa03-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="aaa03-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aaa03-114">_Index_</span><span class="sxs-lookup"><span data-stu-id="aaa03-114">_Index_</span></span> <br/> |<span data-ttu-id="aaa03-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aaa03-115">Required</span></span>  <br/> |<span data-ttu-id="aaa03-116">**Entier**</span><span class="sxs-lookup"><span data-stu-id="aaa03-116">**Integer**</span></span> <br/> |<span data-ttu-id="aaa03-117">Bord du cadre englobant de la forme pour lequel récupérer les coordonnées.</span><span class="sxs-lookup"><span data-stu-id="aaa03-117">The edge of the shape's bounding box for which to get the coordinate.</span></span> <span data-ttu-id="aaa03-118">Voir la section Remarques pour les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="aaa03-118">See Remarks for possible values.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aaa03-119">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="aaa03-119">Return value</span></span>

 <span data-ttu-id="aaa03-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="aaa03-120">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aaa03-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="aaa03-121">Remarks</span></span>

 <span data-ttu-id="aaa03-122">*Index*  peut être l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="aaa03-122">*Index*  can be one of the following values.</span></span> 
  
|<span data-ttu-id="aaa03-123">**Élément**</span><span class="sxs-lookup"><span data-stu-id="aaa03-123">**Item**</span></span>|<span data-ttu-id="aaa03-124">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="aaa03-124">**Value**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aaa03-125">Bord gauche</span><span class="sxs-lookup"><span data-stu-id="aaa03-125">Left edge</span></span>  <br/> |<span data-ttu-id="aaa03-126">0</span><span class="sxs-lookup"><span data-stu-id="aaa03-126">0</span></span>  <br/> |
|<span data-ttu-id="aaa03-127">Bord droit</span><span class="sxs-lookup"><span data-stu-id="aaa03-127">Right edge</span></span>  <br/> |<span data-ttu-id="aaa03-128">1 </span><span class="sxs-lookup"><span data-stu-id="aaa03-128">1</span></span>  <br/> |
|<span data-ttu-id="aaa03-129">Bord supérieur</span><span class="sxs-lookup"><span data-stu-id="aaa03-129">Top edge</span></span>  <br/> |<span data-ttu-id="aaa03-130">2 </span><span class="sxs-lookup"><span data-stu-id="aaa03-130">2</span></span>  <br/> |
|<span data-ttu-id="aaa03-131">Bord inférieur</span><span class="sxs-lookup"><span data-stu-id="aaa03-131">Bottom edge</span></span>  <br/> |<span data-ttu-id="aaa03-132">3 </span><span class="sxs-lookup"><span data-stu-id="aaa03-132">3</span></span>  <br/> |
   
<span data-ttu-id="aaa03-133">Si la forme a un parent, la valeur de retour se trouve dans le système de coordonnées de ce parent.</span><span class="sxs-lookup"><span data-stu-id="aaa03-133">If the shape has a parent, the return value is in the coordinate system of that parent.</span></span>
  

