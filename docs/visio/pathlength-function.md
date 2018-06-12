---
title: PATHLENGTH, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: Renvoie la longueur du chemin défini dans la section Geometry spécifiée.
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789227"
---
# <a name="pathlength-function"></a><span data-ttu-id="3299c-103">PATHLENGTH, fonction</span><span class="sxs-lookup"><span data-stu-id="3299c-103">PATHLENGTH Function</span></span>

<span data-ttu-id="3299c-104">Renvoie la longueur du chemin défini dans la section Geometry spécifiée.</span><span class="sxs-lookup"><span data-stu-id="3299c-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="3299c-105">Informations de version</span><span class="sxs-lookup"><span data-stu-id="3299c-105">Version Information</span></span>

<span data-ttu-id="3299c-106">Version ajoutée : Visio 2010</span><span class="sxs-lookup"><span data-stu-id="3299c-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3299c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3299c-107">Syntax</span></span>

<span data-ttu-id="3299c-108">PATHLENGTH (** *section* ** ** *[, segment]* **)</span><span class="sxs-lookup"><span data-stu-id="3299c-108">PATHLENGTH(** *section* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3299c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3299c-109">Parameters</span></span>

|<span data-ttu-id="3299c-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="3299c-110">**Name**</span></span>|<span data-ttu-id="3299c-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3299c-111">**Required/Optional**</span></span>|<span data-ttu-id="3299c-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3299c-112">**Data Type**</span></span>|<span data-ttu-id="3299c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="3299c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3299c-114">_section_</span><span class="sxs-lookup"><span data-stu-id="3299c-114">_section_</span></span> <br/> |<span data-ttu-id="3299c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3299c-115">Required</span></span>  <br/> |<span data-ttu-id="3299c-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="3299c-116">**String**</span></span> <br/> |<span data-ttu-id="3299c-117">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="3299c-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="3299c-118">_segment_</span><span class="sxs-lookup"><span data-stu-id="3299c-118">_segment_</span></span> <br/> |<span data-ttu-id="3299c-119">Facultatif</span><span class="sxs-lookup"><span data-stu-id="3299c-119">Optional</span></span>  <br/> |<span data-ttu-id="3299c-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="3299c-120">**Integer**</span></span> <br/> |<span data-ttu-id="3299c-121">Segment de base 1 du chemin à mesurer.</span><span class="sxs-lookup"><span data-stu-id="3299c-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3299c-122">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="3299c-122">Return value</span></span>

 <span data-ttu-id="3299c-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="3299c-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3299c-124">Note</span><span class="sxs-lookup"><span data-stu-id="3299c-124">Remarks</span></span>

<span data-ttu-id="3299c-125">Si la _section_ ou _segment_ n’existe pas, Microsoft Visio renvoie #REF !.</span><span class="sxs-lookup"><span data-stu-id="3299c-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="3299c-126">Si vous incluez une valeur de _segment_ , PATHLENGTH renvoie la longueur de ce segment uniquement.</span><span class="sxs-lookup"><span data-stu-id="3299c-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

