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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424496"
---
# <a name="segmentcount-function"></a><span data-ttu-id="bdbc5-103">Fonction SEGMENTCOUNT</span><span class="sxs-lookup"><span data-stu-id="bdbc5-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="bdbc5-104">Renvoie le nombre de segments qui constituent le chemin.</span><span class="sxs-lookup"><span data-stu-id="bdbc5-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bdbc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bdbc5-105">Syntax</span></span>

<span data-ttu-id="bdbc5-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span><span class="sxs-lookup"><span data-stu-id="bdbc5-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bdbc5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bdbc5-107">Parameters</span></span>

|<span data-ttu-id="bdbc5-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="bdbc5-108">**Name**</span></span>|<span data-ttu-id="bdbc5-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="bdbc5-109">**Required/Optional**</span></span>|<span data-ttu-id="bdbc5-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="bdbc5-110">**Data Type**</span></span>|<span data-ttu-id="bdbc5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="bdbc5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bdbc5-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="bdbc5-112">_pathRef_</span></span> <br/> |<span data-ttu-id="bdbc5-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bdbc5-113">Required</span></span>  <br/> |<span data-ttu-id="bdbc5-114">**Entier**</span><span class="sxs-lookup"><span data-stu-id="bdbc5-114">**Integer**</span></span> <br/> |<span data-ttu-id="bdbc5-115">Section Geometry qui représente le chemin, spécifiée par une référence à sa cellule Path (par exemple Geometry1.Path).</span><span class="sxs-lookup"><span data-stu-id="bdbc5-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bdbc5-116">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="bdbc5-116">Return value</span></span>

<span data-ttu-id="bdbc5-117">Entier</span><span class="sxs-lookup"><span data-stu-id="bdbc5-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bdbc5-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="bdbc5-118">Remarks</span></span>

<span data-ttu-id="bdbc5-119">Le total des segments renvoyés ne tient pas compte des déviations de trait.</span><span class="sxs-lookup"><span data-stu-id="bdbc5-119">Line jumps are not included in the total number of segments returned.</span></span>
  

