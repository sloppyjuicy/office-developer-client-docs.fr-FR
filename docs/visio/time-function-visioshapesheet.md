---
title: TIME, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251506
localization_priority: Normal
ms.assetid: 2e662230-0760-5f43-52dc-927f499715f6
description: Renvoie l’heure en heure, minute et seconde.
ms.openlocfilehash: 4390e0cdccf0ae7798d5ada4329a28f72566ecac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789913"
---
# <a name="time-function-visioshapesheet"></a><span data-ttu-id="8cc64-103">TIME, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8cc64-103">TIME Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8cc64-104">Renvoie l’heure en _heure_, _minute_et _seconde_.</span><span class="sxs-lookup"><span data-stu-id="8cc64-104">Returns the time represented by  _hour_,  _minute_, and  _second_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="8cc64-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8cc64-105">Syntax</span></span>

<span data-ttu-id="8cc64-106">TEMPS (** *heure* **, ** *minute* **, ** *deuxième* **)</span><span class="sxs-lookup"><span data-stu-id="8cc64-106">TIME(** *hour* **, ** *minute* **, ** *second* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8cc64-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8cc64-107">Parameters</span></span>

|<span data-ttu-id="8cc64-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="8cc64-108">**Name**</span></span>|<span data-ttu-id="8cc64-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8cc64-109">**Required/Optional**</span></span>|<span data-ttu-id="8cc64-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8cc64-110">**Data Type**</span></span>|<span data-ttu-id="8cc64-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8cc64-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8cc64-112">_heure_</span><span class="sxs-lookup"><span data-stu-id="8cc64-112">_hour_</span></span> <br/> |<span data-ttu-id="8cc64-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8cc64-113">Required</span></span>  <br/> |<span data-ttu-id="8cc64-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8cc64-114">**Numeric**</span></span> <br/> |<span data-ttu-id="8cc64-115">Composant heure</span><span class="sxs-lookup"><span data-stu-id="8cc64-115">The hour component.</span></span>  <br/> |
| <span data-ttu-id="8cc64-116">_minute_</span><span class="sxs-lookup"><span data-stu-id="8cc64-116">_minute_</span></span> <br/> |<span data-ttu-id="8cc64-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8cc64-117">Required</span></span>  <br/> |<span data-ttu-id="8cc64-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8cc64-118">**Numeric**</span></span> <br/> |<span data-ttu-id="8cc64-119">Composant minute</span><span class="sxs-lookup"><span data-stu-id="8cc64-119">The minute comonent.</span></span>  <br/> |
| <span data-ttu-id="8cc64-120">_seconde_</span><span class="sxs-lookup"><span data-stu-id="8cc64-120">_second_</span></span> <br/> |<span data-ttu-id="8cc64-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8cc64-121">Required</span></span>  <br/> |<span data-ttu-id="8cc64-122">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="8cc64-122">**Numeric**</span></span> <br/> |<span data-ttu-id="8cc64-123">Composant seconde</span><span class="sxs-lookup"><span data-stu-id="8cc64-123">The second component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="8cc64-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="8cc64-124">Return value</span></span>

<span data-ttu-id="8cc64-125">Numérique</span><span class="sxs-lookup"><span data-stu-id="8cc64-125">Numeric</span></span>
  
## <a name="example-1"></a><span data-ttu-id="8cc64-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="8cc64-126">Example 1</span></span>

<span data-ttu-id="8cc64-127">TIME(15;30;30)</span><span class="sxs-lookup"><span data-stu-id="8cc64-127">TIME(15,30,30)</span></span>
  
<span data-ttu-id="8cc64-128">Renvoie la valeur représentant 15:30:30.</span><span class="sxs-lookup"><span data-stu-id="8cc64-128">Returns the value representing 15:30:30.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8cc64-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="8cc64-129">Example 2</span></span>

<span data-ttu-id="8cc64-130">FORMAT(TIME(15;30;30),"HH:mm")</span><span class="sxs-lookup"><span data-stu-id="8cc64-130">FORMAT(TIME(15,30,30),"HH:mm")</span></span>
  
<span data-ttu-id="8cc64-131">Renvoie la valeur représentant 15:30.</span><span class="sxs-lookup"><span data-stu-id="8cc64-131">Returns the value representing 15:30.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8cc64-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="8cc64-132">Example 3</span></span>

<span data-ttu-id="8cc64-133">TIME(15;30;30) + 8 he.</span><span class="sxs-lookup"><span data-stu-id="8cc64-133">TIME(15,30,30) + 8 eh.</span></span>
  
<span data-ttu-id="8cc64-134">Renvoie la valeur représentant 23:30:30.</span><span class="sxs-lookup"><span data-stu-id="8cc64-134">Returns the value representing 23:30:30.</span></span>
  

