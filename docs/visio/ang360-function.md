---
title: ANG360, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: Normalise la plage d’un angle.
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160299"
---
# <a name="ang360-function"></a><span data-ttu-id="c89d0-103">Fonction ANG360</span><span class="sxs-lookup"><span data-stu-id="c89d0-103">ANG360 Function</span></span>

<span data-ttu-id="c89d0-104">Normalise la plage d’un angle sur 0 \< = résultat \< 2pi radians (0 \< = résultat \< 360 degrés).</span><span class="sxs-lookup"><span data-stu-id="c89d0-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c89d0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c89d0-105">Syntax</span></span>

<span data-ttu-id="c89d0-106">ANG360 (***angle*** )</span><span class="sxs-lookup"><span data-stu-id="c89d0-106">ANG360(***angle*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c89d0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c89d0-107">Parameters</span></span>

|<span data-ttu-id="c89d0-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c89d0-108">**Name**</span></span>|<span data-ttu-id="c89d0-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c89d0-109">**Required/Optional**</span></span>|<span data-ttu-id="c89d0-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c89d0-110">**Data Type**</span></span>|<span data-ttu-id="c89d0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c89d0-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c89d0-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="c89d0-112">_angle_</span></span> <br/> |<span data-ttu-id="c89d0-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c89d0-113">Required</span></span>  <br/> |<span data-ttu-id="c89d0-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="c89d0-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c89d0-115">Angle à normaliser.</span><span class="sxs-lookup"><span data-stu-id="c89d0-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c89d0-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="c89d0-116">Remarks</span></span>

<span data-ttu-id="c89d0-117">Si *angle* n’est pas spécifié à l’aide d’unités angulaires, il est interprété comme des radians.</span><span class="sxs-lookup"><span data-stu-id="c89d0-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="c89d0-118">Si *angle* ne peut pas être converti en valeur, une #VALUE !</span><span class="sxs-lookup"><span data-stu-id="c89d0-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="c89d0-119">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c89d0-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c89d0-120">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="c89d0-120">Example 1</span></span>

<span data-ttu-id="c89d0-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="c89d0-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="c89d0-122">Renvoie 35 deg</span><span class="sxs-lookup"><span data-stu-id="c89d0-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c89d0-123">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="c89d0-123">Example 2</span></span>

<span data-ttu-id="c89d0-124">ANG360(-9,8 rad)</span><span class="sxs-lookup"><span data-stu-id="c89d0-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="c89d0-125">Renvoie 2,7664 rad</span><span class="sxs-lookup"><span data-stu-id="c89d0-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c89d0-126">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="c89d0-126">Example 3</span></span>

<span data-ttu-id="c89d0-127">ANG360 (45)</span><span class="sxs-lookup"><span data-stu-id="c89d0-127">ANG360(45)</span></span>
  
<span data-ttu-id="c89d0-128">Renvoie 58,31 deg (1,0177 rad)</span><span class="sxs-lookup"><span data-stu-id="c89d0-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

