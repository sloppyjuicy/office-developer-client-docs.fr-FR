---
title: MAGNITUDE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251461
localization_priority: Normal
ms.assetid: 9f443687-9861-5f51-94c4-f056805f736b
description: Renvoie l’ampleur du vecteur dont la hauteur est A et dont est B, multiplié par respectifs constantes constanteA et constanteB.
ms.openlocfilehash: f4c428b8b381af58958dab66a71ddd0bcaf715c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789058"
---
# <a name="magnitude-function"></a><span data-ttu-id="765ab-103">MAGNITUDE, fonction</span><span class="sxs-lookup"><span data-stu-id="765ab-103">MAGNITUDE Function</span></span>

<span data-ttu-id="765ab-104">Renvoie l’ampleur du vecteur dont la hauteur est _A_ et dont est _B_multipliée par les constantes respectives _constanteA_ et _constanteB_.</span><span class="sxs-lookup"><span data-stu-id="765ab-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="765ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="765ab-105">Syntax</span></span>

<span data-ttu-id="765ab-106">MAGNITUDE (** *constanteA* **, ** *A* **, ** *constanteB* **, ** *B* **)</span><span class="sxs-lookup"><span data-stu-id="765ab-106">MAGNITUDE(** *constantA* **, ** *A* **, ** *constantB* **, ** *B* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="765ab-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="765ab-107">Parameters</span></span>

|<span data-ttu-id="765ab-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="765ab-108">**Name**</span></span>|<span data-ttu-id="765ab-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="765ab-109">**Required/Optional**</span></span>|<span data-ttu-id="765ab-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="765ab-110">**Data Type**</span></span>|<span data-ttu-id="765ab-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="765ab-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="765ab-112">_constanteA_</span><span class="sxs-lookup"><span data-stu-id="765ab-112">_constantA_</span></span> <br/> |<span data-ttu-id="765ab-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="765ab-113">Required</span></span>  <br/> |<span data-ttu-id="765ab-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="765ab-114">**Number**</span></span> <br/> |<span data-ttu-id="765ab-115">Constante par laquelle multiplier la hauteur</span><span class="sxs-lookup"><span data-stu-id="765ab-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="765ab-116">_A_</span><span class="sxs-lookup"><span data-stu-id="765ab-116">_A_</span></span> <br/> |<span data-ttu-id="765ab-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="765ab-117">Required</span></span>  <br/> |<span data-ttu-id="765ab-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="765ab-118">**Number**</span></span> <br/> |<span data-ttu-id="765ab-119">Hauteur</span><span class="sxs-lookup"><span data-stu-id="765ab-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="765ab-120">_constanteB_</span><span class="sxs-lookup"><span data-stu-id="765ab-120">_constantB_</span></span> <br/> |<span data-ttu-id="765ab-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="765ab-121">Required</span></span>  <br/> |<span data-ttu-id="765ab-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="765ab-122">**Number**</span></span> <br/> |<span data-ttu-id="765ab-123">Constante par laquelle multiplier la longueur</span><span class="sxs-lookup"><span data-stu-id="765ab-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="765ab-124">_B_</span><span class="sxs-lookup"><span data-stu-id="765ab-124">_B_</span></span> <br/> |<span data-ttu-id="765ab-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="765ab-125">Required</span></span>  <br/> |<span data-ttu-id="765ab-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="765ab-126">**Number**</span></span> <br/> |<span data-ttu-id="765ab-127">Longueur</span><span class="sxs-lookup"><span data-stu-id="765ab-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="765ab-128">Note</span><span class="sxs-lookup"><span data-stu-id="765ab-128">Remarks</span></span>

<span data-ttu-id="765ab-129">La fonction MAGNITUDE est calculée selon la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="765ab-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="765ab-130">SQRT ((constanteA \* A) ^ 2 + (constanteB \* B) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="765ab-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="765ab-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="765ab-131">Example</span></span>

<span data-ttu-id="765ab-132">MAGNITUDE(1; 3; 1; 4)</span><span class="sxs-lookup"><span data-stu-id="765ab-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="765ab-133">Renvoie 5.</span><span class="sxs-lookup"><span data-stu-id="765ab-133">Returns 5.</span></span> 
  

