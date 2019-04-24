---
title: SEGMENTCOUNT, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: Renvoie le nombre de segments qui constituent le chemin.
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326039"
---
# <a name="segmentcount-function"></a><span data-ttu-id="75e12-103">Fonction SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="75e12-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="75e12-104">Renvoie le nombre de segments qui constituent le chemin.</span><span class="sxs-lookup"><span data-stu-id="75e12-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="75e12-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="75e12-105">Syntax</span></span>

<span data-ttu-id="75e12-106">SEGMENTCOUNT (\* \* *pathRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="75e12-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="75e12-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="75e12-107">Parameters</span></span>

|<span data-ttu-id="75e12-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="75e12-108">**Name**</span></span>|<span data-ttu-id="75e12-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="75e12-109">**Required/Optional**</span></span>|<span data-ttu-id="75e12-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="75e12-110">**Data Type**</span></span>|<span data-ttu-id="75e12-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="75e12-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="75e12-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="75e12-112">_pathRef_</span></span> <br/> |<span data-ttu-id="75e12-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="75e12-113">Required</span></span>  <br/> |<span data-ttu-id="75e12-114">**Entier**</span><span class="sxs-lookup"><span data-stu-id="75e12-114">**Integer**</span></span> <br/> |<span data-ttu-id="75e12-115">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="75e12-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="75e12-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="75e12-116">Return value</span></span>

<span data-ttu-id="75e12-117">Entier</span><span class="sxs-lookup"><span data-stu-id="75e12-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="75e12-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="75e12-118">Remarks</span></span>

<span data-ttu-id="75e12-119">Le total des segments renvoyés ne tient pas compte des déviations de trait.</span><span class="sxs-lookup"><span data-stu-id="75e12-119">Line jumps are not included in the total number of segments returned.</span></span>
  

