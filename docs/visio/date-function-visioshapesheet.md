---
title: Fonction DATE (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Renvoie la date représentée par année, mois et jour formatée en fonction de la date abrégée défini dans les paramètres régionaux du système. Les valeurs de l’année, mois et jour conformes au calendrier grégorien.
ms.openlocfilehash: 7a19d97f70f9314ecdbd2228078e1e18b1ac9146
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788435"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="0a672-104">Fonction DATE (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="0a672-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="0a672-105">Renvoie la date représentée par *année, mois* et *jour* formatée en fonction de la date abrégée défini dans les paramètres régionaux du système.</span><span class="sxs-lookup"><span data-stu-id="0a672-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="0a672-106">Les valeurs de *l’année*, *mois* et *jour* conformes au calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="0a672-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0a672-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a672-107">Syntax</span></span>

<span data-ttu-id="0a672-108">DATE (** *année* **, ** *mois* **, ** *jour* **)</span><span class="sxs-lookup"><span data-stu-id="0a672-108">DATE(** *year* **, ** *month* **, ** *day* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0a672-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a672-109">Parameters</span></span>

|<span data-ttu-id="0a672-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="0a672-110">**Name**</span></span>|<span data-ttu-id="0a672-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="0a672-111">**Required/Optional**</span></span>|<span data-ttu-id="0a672-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="0a672-112">**Data Type**</span></span>|<span data-ttu-id="0a672-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="0a672-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0a672-114">_year_</span><span class="sxs-lookup"><span data-stu-id="0a672-114">_year_</span></span> <br/> |<span data-ttu-id="0a672-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a672-115">Required</span></span>  <br/> |<span data-ttu-id="0a672-116">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a672-116">**Integer**</span></span> <br/> |<span data-ttu-id="0a672-117">Année</span><span class="sxs-lookup"><span data-stu-id="0a672-117">The year.</span></span>  <br/> |
| <span data-ttu-id="0a672-118">_Mois_</span><span class="sxs-lookup"><span data-stu-id="0a672-118">_month_</span></span> <br/> |<span data-ttu-id="0a672-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a672-119">Required</span></span>  <br/> |<span data-ttu-id="0a672-120">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a672-120">**Integer**</span></span> <br/> |<span data-ttu-id="0a672-121">Mois</span><span class="sxs-lookup"><span data-stu-id="0a672-121">The month.</span></span>  <br/> |
| <span data-ttu-id="0a672-122">_day_</span><span class="sxs-lookup"><span data-stu-id="0a672-122">_day_</span></span> <br/> |<span data-ttu-id="0a672-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="0a672-123">Required</span></span>  <br/> |<span data-ttu-id="0a672-124">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0a672-124">**Integer**</span></span> <br/> |<span data-ttu-id="0a672-125">Jour</span><span class="sxs-lookup"><span data-stu-id="0a672-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="0a672-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="0a672-126">Example 1</span></span>

<span data-ttu-id="0a672-127">DATE(1999;6;7)</span><span class="sxs-lookup"><span data-stu-id="0a672-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="0a672-128">Renvoie la valeur représentant le 07/06/99.</span><span class="sxs-lookup"><span data-stu-id="0a672-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="0a672-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="0a672-129">Example 2</span></span>

<span data-ttu-id="0a672-130">DATE(1999;6;7) + 4 je.</span><span class="sxs-lookup"><span data-stu-id="0a672-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="0a672-131">Renvoie la valeur représentant 11/06/99.</span><span class="sxs-lookup"><span data-stu-id="0a672-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="0a672-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="0a672-132">Example 3</span></span>

<span data-ttu-id="0a672-133">FORMAT(DATE(1999;10;14);"C")</span><span class="sxs-lookup"><span data-stu-id="0a672-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="0a672-134">Renvoie la valeur représentant le mardi 14 octobre 1999.</span><span class="sxs-lookup"><span data-stu-id="0a672-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

