---
title: NEARESTPOINTONPATH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789158"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="2caa6-103">NEARESTPOINTONPATH, fonction</span><span class="sxs-lookup"><span data-stu-id="2caa6-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="2caa6-104">Renvoie le pourcentage de la distance le long du chemin du point le plus proche des coordonnées spécifiées, sous la forme d’une valeur comprise entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="2caa6-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="2caa6-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="2caa6-105">Version Information</span></span>

<span data-ttu-id="2caa6-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="2caa6-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2caa6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2caa6-107">Syntax</span></span>

<span data-ttu-id="2caa6-108">NEARESTPOINTONPATH (** *section* **, ** *x* **, ** *y* **)</span><span class="sxs-lookup"><span data-stu-id="2caa6-108">NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2caa6-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2caa6-109">Parameters</span></span>

|<span data-ttu-id="2caa6-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2caa6-110">**Name**</span></span>|<span data-ttu-id="2caa6-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="2caa6-111">**Required/Optional**</span></span>|<span data-ttu-id="2caa6-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="2caa6-112">**Data Type**</span></span>|<span data-ttu-id="2caa6-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="2caa6-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2caa6-114">_section_</span><span class="sxs-lookup"><span data-stu-id="2caa6-114">_section_</span></span> <br/> |<span data-ttu-id="2caa6-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2caa6-115">Required</span></span>  <br/> |<span data-ttu-id="2caa6-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="2caa6-116">**String**</span></span> <br/> |<span data-ttu-id="2caa6-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="2caa6-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="2caa6-118">_x_</span><span class="sxs-lookup"><span data-stu-id="2caa6-118">_x_</span></span> <br/> |<span data-ttu-id="2caa6-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2caa6-119">Required</span></span>  <br/> |<span data-ttu-id="2caa6-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="2caa6-120">**Double**</span></span> <br/> |<span data-ttu-id="2caa6-121">_X_-coordonnées du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="2caa6-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="2caa6-122">_y_</span><span class="sxs-lookup"><span data-stu-id="2caa6-122">_y_</span></span> <br/> |<span data-ttu-id="2caa6-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="2caa6-123">Required</span></span>  <br/> |<span data-ttu-id="2caa6-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="2caa6-124">**Double**</span></span> <br/> |<span data-ttu-id="2caa6-125">La valeur _y_-coordonnées du point spécifié.</span><span class="sxs-lookup"><span data-stu-id="2caa6-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="2caa6-126">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="2caa6-126">Return value</span></span>

 <span data-ttu-id="2caa6-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="2caa6-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2caa6-128">Note</span><span class="sxs-lookup"><span data-stu-id="2caa6-128">Remarks</span></span>

<span data-ttu-id="2caa6-129">Si la _section_ n’existe pas, Microsoft Visio renvoie #REF !.</span><span class="sxs-lookup"><span data-stu-id="2caa6-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

