---
title: ANGLETOLOC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
localization_priority: Normal
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: Renvoie un angle transformé dans le système de coordonnées locales de la forme de destination. Convertit un angle de coordonnées locales de la forme source en coordonnées locales de la forme de destination.
ms.openlocfilehash: e971613d4fc33cd991e7e9aeba49ac47871ebe8f
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160264"
---
# <a name="angletoloc-function"></a><span data-ttu-id="39f7f-104">Fonction ANGLETOLOC</span><span class="sxs-lookup"><span data-stu-id="39f7f-104">ANGLETOLOC Function</span></span>

<span data-ttu-id="39f7f-105">Renvoie un angle transformé dans le système de coordonnées locales de la forme de destination.</span><span class="sxs-lookup"><span data-stu-id="39f7f-105">Returns a transformed angle in the destination shape's local coordinate system.</span></span> <span data-ttu-id="39f7f-106">Convertit un angle de coordonnées locales de la forme source en coordonnées locales de la forme de destination.</span><span class="sxs-lookup"><span data-stu-id="39f7f-106">Converts an angle from local coordinates in a source shape to the local coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="39f7f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="39f7f-107">Syntax</span></span>

<span data-ttu-id="39f7f-108">ANGLETOLOC (***srcAngle***, ***srcRef***, ***dstRef*** )</span><span class="sxs-lookup"><span data-stu-id="39f7f-108">ANGLETOLOC(***srcAngle***, ***srcRef***, ***dstRef*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="39f7f-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="39f7f-109">Parameters</span></span>

|<span data-ttu-id="39f7f-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="39f7f-110">**Name**</span></span>|<span data-ttu-id="39f7f-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="39f7f-111">**Required/Optional**</span></span>|<span data-ttu-id="39f7f-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="39f7f-112">**Data Type**</span></span>|<span data-ttu-id="39f7f-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="39f7f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="39f7f-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="39f7f-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="39f7f-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="39f7f-115">Required</span></span>  <br/> |<span data-ttu-id="39f7f-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="39f7f-116">**Numeric**</span></span> <br/> |<span data-ttu-id="39f7f-117">Angle dans le système de coordonnées source.</span><span class="sxs-lookup"><span data-stu-id="39f7f-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="39f7f-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="39f7f-118">_srcRef_</span></span> <br/> |<span data-ttu-id="39f7f-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="39f7f-119">Required</span></span>  <br/> |<span data-ttu-id="39f7f-120">**String**</span><span class="sxs-lookup"><span data-stu-id="39f7f-120">**String**</span></span> <br/> | <span data-ttu-id="39f7f-121">Référence à une cellule de l’objet source, comme une forme, un groupe, une page, etc.</span><span class="sxs-lookup"><span data-stu-id="39f7f-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="39f7f-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="39f7f-122">_dstRef_</span></span> <br/> |<span data-ttu-id="39f7f-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="39f7f-123">Required</span></span>  <br/> |<span data-ttu-id="39f7f-124">**String**</span><span class="sxs-lookup"><span data-stu-id="39f7f-124">**String**</span></span> <br/> |<span data-ttu-id="39f7f-125">Référence à une cellule de l’objet de destination, comme une forme, un groupe, une page, etc.</span><span class="sxs-lookup"><span data-stu-id="39f7f-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="39f7f-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="39f7f-126">Remarks</span></span>

<span data-ttu-id="39f7f-127">La fonction ANGLETOLOC permet de définir les cellules d’angle local d’une forme en termes d’angle d’un autre espace de coordonnées.</span><span class="sxs-lookup"><span data-stu-id="39f7f-127">You can use the ANGLETOLOC function to set local angle cells in a shape in terms of an angle from another coordinate space.</span></span>
  
<span data-ttu-id="39f7f-p103">Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="39f7f-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="39f7f-130">Les coordonnées source et cible doivent se trouver sur la même page.</span><span class="sxs-lookup"><span data-stu-id="39f7f-130">The source and destination coordinates must be on the same page.</span></span>
  

