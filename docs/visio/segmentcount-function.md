---
title: SEGMENTCOUNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Renvoie le nombre de segments qui constituent le chemin.
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789622"
---
# <a name="segmentcount-function"></a><span data-ttu-id="20fdc-103">SEGMENTCOUNT, fonction</span><span class="sxs-lookup"><span data-stu-id="20fdc-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="20fdc-104">Renvoie le nombre de segments qui constituent le chemin.</span><span class="sxs-lookup"><span data-stu-id="20fdc-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="20fdc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="20fdc-105">Syntax</span></span>

<span data-ttu-id="20fdc-106">SEGMENTCOUNT (** *pathRef* **)</span><span class="sxs-lookup"><span data-stu-id="20fdc-106">SEGMENTCOUNT(** *pathRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="20fdc-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="20fdc-107">Parameters</span></span>

|<span data-ttu-id="20fdc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="20fdc-108">**Name**</span></span>|<span data-ttu-id="20fdc-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="20fdc-109">**Required/Optional**</span></span>|<span data-ttu-id="20fdc-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="20fdc-110">**Data Type**</span></span>|<span data-ttu-id="20fdc-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="20fdc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="20fdc-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="20fdc-112">_pathRef_</span></span> <br/> |<span data-ttu-id="20fdc-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="20fdc-113">Required</span></span>  <br/> |<span data-ttu-id="20fdc-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="20fdc-114">**Integer**</span></span> <br/> |<span data-ttu-id="20fdc-115">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="20fdc-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="20fdc-116">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="20fdc-116">Return value</span></span>

<span data-ttu-id="20fdc-117">Entier</span><span class="sxs-lookup"><span data-stu-id="20fdc-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20fdc-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="20fdc-118">Remarks</span></span>

<span data-ttu-id="20fdc-119">Le total des segments renvoyés ne tient pas compte des déviations de trait.</span><span class="sxs-lookup"><span data-stu-id="20fdc-119">Line jumps are not included in the total number of segments returned.</span></span>
  

