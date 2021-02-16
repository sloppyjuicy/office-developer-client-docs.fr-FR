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
description: Renvoie la magnitude du vecteur dont la montée est A et dont la run est B, multipliée par les constantes respectives constantA et constantB.
ms.openlocfilehash: 6393c7827e2553ca4948c8b9c51075ca8e4783bd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420457"
---
# <a name="magnitude-function"></a><span data-ttu-id="887f6-103">Fonction MAGNITUDE</span><span class="sxs-lookup"><span data-stu-id="887f6-103">MAGNITUDE Function</span></span>

<span data-ttu-id="887f6-104">Renvoie la magnitude du vecteur dont la montée est  _A_ et dont la run est  _B_, multipliée par les constantes respectives  _constantA_ et  _constantB_.</span><span class="sxs-lookup"><span data-stu-id="887f6-104">Returns the magnitude of the vector whose rise is  _A_ and whose run is  _B_, multiplied by the respective constants  _constantA_ and  _constantB_.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="887f6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="887f6-105">Syntax</span></span>

<span data-ttu-id="887f6-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span><span class="sxs-lookup"><span data-stu-id="887f6-106">MAGNITUDE(\*\* *constantA* \*\*, \*\* *A* \*\*, \*\* *constantB* \*\*, \*\* *B* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="887f6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="887f6-107">Parameters</span></span>

|<span data-ttu-id="887f6-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="887f6-108">**Name**</span></span>|<span data-ttu-id="887f6-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="887f6-109">**Required/Optional**</span></span>|<span data-ttu-id="887f6-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="887f6-110">**Data Type**</span></span>|<span data-ttu-id="887f6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="887f6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="887f6-112">_constantA_</span><span class="sxs-lookup"><span data-stu-id="887f6-112">_constantA_</span></span> <br/> |<span data-ttu-id="887f6-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="887f6-113">Required</span></span>  <br/> |<span data-ttu-id="887f6-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="887f6-114">**Number**</span></span> <br/> |<span data-ttu-id="887f6-115">Constante par laquelle multiplier la hauteur</span><span class="sxs-lookup"><span data-stu-id="887f6-115">The constant by which to multiply the rise.</span></span>  <br/> |
| <span data-ttu-id="887f6-116">_A_</span><span class="sxs-lookup"><span data-stu-id="887f6-116">_A_</span></span> <br/> |<span data-ttu-id="887f6-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="887f6-117">Required</span></span>  <br/> |<span data-ttu-id="887f6-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="887f6-118">**Number**</span></span> <br/> |<span data-ttu-id="887f6-119">Hauteur</span><span class="sxs-lookup"><span data-stu-id="887f6-119">The rise.</span></span>  <br/> |
| <span data-ttu-id="887f6-120">_constantB_</span><span class="sxs-lookup"><span data-stu-id="887f6-120">_constantB_</span></span> <br/> |<span data-ttu-id="887f6-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="887f6-121">Required</span></span>  <br/> |<span data-ttu-id="887f6-122">**Number**</span><span class="sxs-lookup"><span data-stu-id="887f6-122">**Number**</span></span> <br/> |<span data-ttu-id="887f6-123">Constante par laquelle multiplier la longueur</span><span class="sxs-lookup"><span data-stu-id="887f6-123">The constant by which to multiply the run.</span></span>  <br/> |
| <span data-ttu-id="887f6-124">_B_</span><span class="sxs-lookup"><span data-stu-id="887f6-124">_B_</span></span> <br/> |<span data-ttu-id="887f6-125">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="887f6-125">Required</span></span>  <br/> |<span data-ttu-id="887f6-126">**Number**</span><span class="sxs-lookup"><span data-stu-id="887f6-126">**Number**</span></span> <br/> |<span data-ttu-id="887f6-127">Longueur</span><span class="sxs-lookup"><span data-stu-id="887f6-127">The run.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="887f6-128">Remarques</span><span class="sxs-lookup"><span data-stu-id="887f6-128">Remarks</span></span>

<span data-ttu-id="887f6-129">La fonction MAGNITUDE est calculée selon la formule suivante :</span><span class="sxs-lookup"><span data-stu-id="887f6-129">MAGNITUDE is calculated according to the following formula:</span></span>
  
<span data-ttu-id="887f6-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span><span class="sxs-lookup"><span data-stu-id="887f6-130">SQRT((constantA \* A)^2 + (constantB \* B)^2)</span></span>
  
## <a name="example"></a><span data-ttu-id="887f6-131">Exemple</span><span class="sxs-lookup"><span data-stu-id="887f6-131">Example</span></span>

<span data-ttu-id="887f6-132">MAGNITUDE(1; 3; 1; 4)</span><span class="sxs-lookup"><span data-stu-id="887f6-132">MAGNITUDE(1, 3, 1, 4)</span></span> 
  
<span data-ttu-id="887f6-133">Renvoie 5.</span><span class="sxs-lookup"><span data-stu-id="887f6-133">Returns 5.</span></span> 
  

