---
title: ASIN, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: Renvoie l'arcsinus d'un nombre, par exemple, l'angle dont le sinus est nombre.
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432820"
---
# <a name="asin-function"></a><span data-ttu-id="71302-103">Fonction ASIN</span><span class="sxs-lookup"><span data-stu-id="71302-103">ASIN Function</span></span>

<span data-ttu-id="71302-104">Renvoie l'arcsinus d'un nombre, par exemple, l'angle dont le sinus est *nombre* .</span><span class="sxs-lookup"><span data-stu-id="71302-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="71302-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="71302-105">Syntax</span></span>

<span data-ttu-id="71302-106">ASIN (\* \* *nombre* \* \*)</span><span class="sxs-lookup"><span data-stu-id="71302-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="71302-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="71302-107">Parameters</span></span>

|<span data-ttu-id="71302-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="71302-108">**Name**</span></span>|<span data-ttu-id="71302-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="71302-109">**Required/Optional**</span></span>|<span data-ttu-id="71302-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="71302-110">**Data Type**</span></span>|<span data-ttu-id="71302-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="71302-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="71302-112">_number_</span><span class="sxs-lookup"><span data-stu-id="71302-112">_number_</span></span> <br/> |<span data-ttu-id="71302-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="71302-113">Required</span></span>  <br/> |<span data-ttu-id="71302-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="71302-114">**Numeric**</span></span> <br/> |<span data-ttu-id="71302-115">Sinus de l’angle.</span><span class="sxs-lookup"><span data-stu-id="71302-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71302-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="71302-116">Remarks</span></span>

<span data-ttu-id="71302-117">La valeur d'entrée doit être comprise entre-1 < = *nombre* < = 1, ou une #NUM!</span><span class="sxs-lookup"><span data-stu-id="71302-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="71302-118">est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="71302-118">error is returned.</span></span> <span data-ttu-id="71302-119">L'angle obtenu se trouve dans la plage-PI/2 < = *angle* _LT_ = pi/2 radians (-90 < = *angle* < = 90 degrés).</span><span class="sxs-lookup"><span data-stu-id="71302-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="71302-120">Exemple</span><span class="sxs-lookup"><span data-stu-id="71302-120">Example</span></span>

<span data-ttu-id="71302-121">ASIN (1)</span><span class="sxs-lookup"><span data-stu-id="71302-121">ASIN(1)</span></span>
  
<span data-ttu-id="71302-122">Renvoie 90 deg</span><span class="sxs-lookup"><span data-stu-id="71302-122">Returns 90 deg</span></span>
  

