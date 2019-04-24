---
title: TIME Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Renvoie l'heure représentée par les heures, les minutes et les secondes.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280996"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="3143d-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="3143d-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="3143d-104">Renvoie l'heure représentée par les _heures_, les _minutes_et les _secondes_.</span><span class="sxs-lookup"><span data-stu-id="3143d-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3143d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3143d-105">Syntax</span></span>

<span data-ttu-id="3143d-106">HEURE (\* \* *heure* \* \*, \* \* *minute* \* \*, \* \* *seconde* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3143d-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3143d-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3143d-107">Parameters</span></span>

|<span data-ttu-id="3143d-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3143d-108">**Name**</span></span>|<span data-ttu-id="3143d-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3143d-109">**Required/Optional**</span></span>|<span data-ttu-id="3143d-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3143d-110">**Data Type**</span></span>|<span data-ttu-id="3143d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3143d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3143d-112">_h/24_</span><span class="sxs-lookup"><span data-stu-id="3143d-112">_hour_</span></span> <br/> |<span data-ttu-id="3143d-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3143d-113">Required</span></span>  <br/> |<span data-ttu-id="3143d-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3143d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="3143d-115">Composant heure</span><span class="sxs-lookup"><span data-stu-id="3143d-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="3143d-116">_précédente_</span><span class="sxs-lookup"><span data-stu-id="3143d-116">_minute_</span></span> <br/> |<span data-ttu-id="3143d-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3143d-117">Required</span></span>  <br/> |<span data-ttu-id="3143d-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3143d-118">**Numeric**</span></span> <br/> |<span data-ttu-id="3143d-119">Composant minute</span><span class="sxs-lookup"><span data-stu-id="3143d-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="3143d-120">_seconde_</span><span class="sxs-lookup"><span data-stu-id="3143d-120">_second_</span></span> <br/> |<span data-ttu-id="3143d-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3143d-121">Required</span></span>  <br/> |<span data-ttu-id="3143d-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="3143d-122">**Numeric**</span></span> <br/> |<span data-ttu-id="3143d-123">Composant seconde</span><span class="sxs-lookup"><span data-stu-id="3143d-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3143d-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3143d-124">Return value</span></span>

<span data-ttu-id="3143d-125">Numérique</span><span class="sxs-lookup"><span data-stu-id="3143d-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="3143d-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="3143d-126">Example 1</span></span>

<span data-ttu-id="3143d-127">HEURE (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="3143d-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="3143d-128">Renvoie la valeur représentant 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="3143d-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3143d-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="3143d-129">Example 2</span></span>

<span data-ttu-id="3143d-130">FORMAT (durée (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="3143d-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="3143d-131">Renvoie la valeur représentant 15:30.</span><span class="sxs-lookup"><span data-stu-id="3143d-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="3143d-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="3143d-132">Example 3</span></span>

<span data-ttu-id="3143d-133">TIME(15;30;30) + 8 he.</span><span class="sxs-lookup"><span data-stu-id="3143d-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="3143d-134">Renvoie la valeur représentant 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="3143d-134">Returns the value representing 23:30:30.</span></span>
  

