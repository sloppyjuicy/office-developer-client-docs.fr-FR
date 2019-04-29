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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414472"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="8b407-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8b407-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8b407-104">Renvoie l'heure représentée par les _heures_, les _minutes_et les _secondes_.</span><span class="sxs-lookup"><span data-stu-id="8b407-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8b407-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b407-105">Syntax</span></span>

<span data-ttu-id="8b407-106">HEURE (\* \* *heure* \* \*, \* \* *minute* \* \*, \* \* *seconde* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8b407-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8b407-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b407-107">Parameters</span></span>

|<span data-ttu-id="8b407-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8b407-108">**Name**</span></span>|<span data-ttu-id="8b407-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8b407-109">**Required/Optional**</span></span>|<span data-ttu-id="8b407-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8b407-110">**Data Type**</span></span>|<span data-ttu-id="8b407-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8b407-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8b407-112">_h/24_</span><span class="sxs-lookup"><span data-stu-id="8b407-112">_hour_</span></span> <br/> |<span data-ttu-id="8b407-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8b407-113">Required</span></span>  <br/> |<span data-ttu-id="8b407-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8b407-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8b407-115">Composant heure</span><span class="sxs-lookup"><span data-stu-id="8b407-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="8b407-116">_précédente_</span><span class="sxs-lookup"><span data-stu-id="8b407-116">_minute_</span></span> <br/> |<span data-ttu-id="8b407-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8b407-117">Required</span></span>  <br/> |<span data-ttu-id="8b407-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8b407-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8b407-119">Composant minute</span><span class="sxs-lookup"><span data-stu-id="8b407-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="8b407-120">_seconde_</span><span class="sxs-lookup"><span data-stu-id="8b407-120">_second_</span></span> <br/> |<span data-ttu-id="8b407-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8b407-121">Required</span></span>  <br/> |<span data-ttu-id="8b407-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8b407-122">**Numeric**</span></span> <br/> |<span data-ttu-id="8b407-123">Composant seconde</span><span class="sxs-lookup"><span data-stu-id="8b407-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8b407-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="8b407-124">Return value</span></span>

<span data-ttu-id="8b407-125">Numérique</span><span class="sxs-lookup"><span data-stu-id="8b407-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="8b407-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="8b407-126">Example 1</span></span>

<span data-ttu-id="8b407-127">HEURE (15, 30, 30)</span><span class="sxs-lookup"><span data-stu-id="8b407-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="8b407-128">Renvoie la valeur représentant 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="8b407-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8b407-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="8b407-129">Example 2</span></span>

<span data-ttu-id="8b407-130">FORMAT (durée (15, 30, 30), "HH: mm")</span><span class="sxs-lookup"><span data-stu-id="8b407-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="8b407-131">Renvoie la valeur représentant 15:30.</span><span class="sxs-lookup"><span data-stu-id="8b407-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8b407-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="8b407-132">Example 3</span></span>

<span data-ttu-id="8b407-133">TIME(15;30;30) + 8 he.</span><span class="sxs-lookup"><span data-stu-id="8b407-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="8b407-134">Renvoie la valeur représentant 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="8b407-134">Returns the value representing 23:30:30.</span></span>
  

