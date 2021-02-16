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
description: Renvoie l’heure représentée par heure, minute et seconde.
ms.openlocfilehash: f5be55d7e63a70d15da49c68b924cc5b03c5ca88
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414472"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="a8a44-103">TIME Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a8a44-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a8a44-104">Renvoie l’heure représentée par  _l’heure,_  _la minute_ et la  _seconde_.</span><span class="sxs-lookup"><span data-stu-id="a8a44-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a8a44-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a8a44-105">Syntax</span></span>

<span data-ttu-id="a8a44-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a8a44-106">TIME(\*\* *hour* \*\*, \*\* *minute* \*\*, \*\* *second* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a8a44-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a8a44-107">Parameters</span></span>

|<span data-ttu-id="a8a44-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a8a44-108">**Name**</span></span>|<span data-ttu-id="a8a44-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a8a44-109">**Required/Optional**</span></span>|<span data-ttu-id="a8a44-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a8a44-110">**Data Type**</span></span>|<span data-ttu-id="a8a44-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8a44-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a8a44-112">_hour_</span><span class="sxs-lookup"><span data-stu-id="a8a44-112">_hour_</span></span> <br/> |<span data-ttu-id="a8a44-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8a44-113">Required</span></span>  <br/> |<span data-ttu-id="a8a44-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a8a44-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a8a44-115">Composant heure</span><span class="sxs-lookup"><span data-stu-id="a8a44-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="a8a44-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="a8a44-116">_minute_</span></span> <br/> |<span data-ttu-id="a8a44-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8a44-117">Required</span></span>  <br/> |<span data-ttu-id="a8a44-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a8a44-118">**Numeric**</span></span> <br/> |<span data-ttu-id="a8a44-119">Composant minute</span><span class="sxs-lookup"><span data-stu-id="a8a44-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="a8a44-120">_second_</span><span class="sxs-lookup"><span data-stu-id="a8a44-120">_second_</span></span> <br/> |<span data-ttu-id="a8a44-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8a44-121">Required</span></span>  <br/> |<span data-ttu-id="a8a44-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="a8a44-122">**Numeric**</span></span> <br/> |<span data-ttu-id="a8a44-123">Composant seconde</span><span class="sxs-lookup"><span data-stu-id="a8a44-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a8a44-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="a8a44-124">Return value</span></span>

<span data-ttu-id="a8a44-125">Numérique</span><span class="sxs-lookup"><span data-stu-id="a8a44-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="a8a44-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="a8a44-126">Example 1</span></span>

<span data-ttu-id="a8a44-127">TIME(15,30,30)</span><span class="sxs-lookup"><span data-stu-id="a8a44-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="a8a44-128">Renvoie la valeur représentant 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="a8a44-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a8a44-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="a8a44-129">Example 2</span></span>

<span data-ttu-id="a8a44-130">FORMAT(TIME(15,30,30),"HH:mm »)</span><span class="sxs-lookup"><span data-stu-id="a8a44-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="a8a44-131">Renvoie la valeur représentant 15:30.</span><span class="sxs-lookup"><span data-stu-id="a8a44-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="a8a44-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="a8a44-132">Example 3</span></span>

<span data-ttu-id="a8a44-133">TIME(15;30;30) + 8 he.</span><span class="sxs-lookup"><span data-stu-id="a8a44-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="a8a44-134">Renvoie la valeur représentant 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="a8a44-134">Returns the value representing 23:30:30.</span></span>
  

