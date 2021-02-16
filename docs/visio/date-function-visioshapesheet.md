---
title: DATE Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251412
localization_priority: Normal
ms.assetid: 2b6c5375-c543-ff2f-f20a-6d92fd65717a
description: Renvoie la date représentée par l’année, le mois et le jour formatés en fonction du style de date courte dans les paramètres régionaux du système. Les valeurs de l’année, du mois et du jour reflètent le calendrier grégorien.
ms.openlocfilehash: 0175c1f06ec3dbdf89774759546c65994d38105e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360332"
---
# <a name="date-function-visioshapesheet"></a><span data-ttu-id="59a2d-104">DATE Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="59a2d-104">DATE Function (VisioShapeSheet)</span></span>

<span data-ttu-id="59a2d-105">Renvoie la date représentée par l’année, le *mois* et le jour formatés en fonction du style de date courte dans les paramètres régionaux du système. </span><span class="sxs-lookup"><span data-stu-id="59a2d-105">Returns the date represented by  *year, month,*  and  *day*  formatted according to the short date style in the system's Regional Settings.</span></span> <span data-ttu-id="59a2d-106">Les valeurs  *de l’année,* *du mois*  et du  *jour*  reflètent le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="59a2d-106">The values for  *year*, *month*  , and  *day*  reflect the Gregorian calendar.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="59a2d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59a2d-107">Syntax</span></span>

<span data-ttu-id="59a2d-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span><span class="sxs-lookup"><span data-stu-id="59a2d-108">DATE(\*\* *year* \*\*, \*\* *month* \*\*, \*\* *day* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="59a2d-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59a2d-109">Parameters</span></span>

|<span data-ttu-id="59a2d-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="59a2d-110">**Name**</span></span>|<span data-ttu-id="59a2d-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="59a2d-111">**Required/Optional**</span></span>|<span data-ttu-id="59a2d-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="59a2d-112">**Data Type**</span></span>|<span data-ttu-id="59a2d-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="59a2d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="59a2d-114">_year_</span><span class="sxs-lookup"><span data-stu-id="59a2d-114">_year_</span></span> <br/> |<span data-ttu-id="59a2d-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="59a2d-115">Required</span></span>  <br/> |<span data-ttu-id="59a2d-116">**Entier**</span><span class="sxs-lookup"><span data-stu-id="59a2d-116">**Integer**</span></span> <br/> |<span data-ttu-id="59a2d-117">Année</span><span class="sxs-lookup"><span data-stu-id="59a2d-117">The year.</span></span>  <br/> |
| <span data-ttu-id="59a2d-118">_Mois_</span><span class="sxs-lookup"><span data-stu-id="59a2d-118">_month_</span></span> <br/> |<span data-ttu-id="59a2d-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="59a2d-119">Required</span></span>  <br/> |<span data-ttu-id="59a2d-120">**Entier**</span><span class="sxs-lookup"><span data-stu-id="59a2d-120">**Integer**</span></span> <br/> |<span data-ttu-id="59a2d-121">Mois</span><span class="sxs-lookup"><span data-stu-id="59a2d-121">The month.</span></span>  <br/> |
| <span data-ttu-id="59a2d-122">_day_</span><span class="sxs-lookup"><span data-stu-id="59a2d-122">_day_</span></span> <br/> |<span data-ttu-id="59a2d-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="59a2d-123">Required</span></span>  <br/> |<span data-ttu-id="59a2d-124">**Entier**</span><span class="sxs-lookup"><span data-stu-id="59a2d-124">**Integer**</span></span> <br/> |<span data-ttu-id="59a2d-125">Jour</span><span class="sxs-lookup"><span data-stu-id="59a2d-125">The day.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="59a2d-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="59a2d-126">Example 1</span></span>

<span data-ttu-id="59a2d-127">DATE(1999,6,7)</span><span class="sxs-lookup"><span data-stu-id="59a2d-127">DATE(1999,6,7)</span></span>
  
<span data-ttu-id="59a2d-128">Renvoie la valeur représentant le 07/06/99.</span><span class="sxs-lookup"><span data-stu-id="59a2d-128">Returns the value representing 6/7/1999.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="59a2d-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="59a2d-129">Example 2</span></span>

<span data-ttu-id="59a2d-130">DATE(1999;6;7) + 4 je.</span><span class="sxs-lookup"><span data-stu-id="59a2d-130">DATE(1999,6,7) + 4 ed.</span></span>
  
<span data-ttu-id="59a2d-131">Renvoie la valeur représentant 11/06/99.</span><span class="sxs-lookup"><span data-stu-id="59a2d-131">Returns the value representing 6/11/1999.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="59a2d-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="59a2d-132">Example 3</span></span>

<span data-ttu-id="59a2d-133">FORMAT(DATE(1999,10,14),"C »)</span><span class="sxs-lookup"><span data-stu-id="59a2d-133">FORMAT(DATE(1999,10,14),"C")</span></span>
  
<span data-ttu-id="59a2d-134">Renvoie la valeur représentant le mardi 14 octobre 1999.</span><span class="sxs-lookup"><span data-stu-id="59a2d-134">Returns the value representing Tuesday, October 14, 1999.</span></span>
  

