---
title: ANGLETOPAR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: Renvoie un angle transformé dans le système de coordonnées parent de la forme de destination. Convertit un angle des coordonnées locales de la forme source en coordonnées parent de la forme de destination.
ms.openlocfilehash: e411cbae21d832039e2fbda93393a8fe0bd1f9f8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404322"
---
# <a name="angletopar-function"></a><span data-ttu-id="28b93-104">Fonction ANGLETOPAR</span><span class="sxs-lookup"><span data-stu-id="28b93-104">ANGLETOPAR Function</span></span>

<span data-ttu-id="28b93-105">Renvoie un angle transformé dans le système de coordonnées parent de la forme de destination.</span><span class="sxs-lookup"><span data-stu-id="28b93-105">Returns a transformed angle in the destination shape's parent coordinate system.</span></span> <span data-ttu-id="28b93-106">Convertit un angle des coordonnées locales de la forme source en coordonnées parent de la forme de destination.</span><span class="sxs-lookup"><span data-stu-id="28b93-106">Converts an angle from local coordinates in a source shape to the parent coordinates in a destination shape.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28b93-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="28b93-107">Syntax</span></span>

<span data-ttu-id="28b93-108">ANGLETOPAR (\* \* *srcAngle* \* \*, \* \* *srcRef* \* \*, \* \* *dstRef* \* \*)</span><span class="sxs-lookup"><span data-stu-id="28b93-108">ANGLETOPAR(\*\* *srcAngle* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28b93-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="28b93-109">Parameters</span></span>

|<span data-ttu-id="28b93-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="28b93-110">**Name**</span></span>|<span data-ttu-id="28b93-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="28b93-111">**Required/Optional**</span></span>|<span data-ttu-id="28b93-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="28b93-112">**Data Type**</span></span>|<span data-ttu-id="28b93-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="28b93-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28b93-114">_srcAngle_</span><span class="sxs-lookup"><span data-stu-id="28b93-114">_srcAngle_</span></span> <br/> |<span data-ttu-id="28b93-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28b93-115">Required</span></span>  <br/> |<span data-ttu-id="28b93-116">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="28b93-116">**Numeric**</span></span> <br/> |<span data-ttu-id="28b93-117">Angle dans le système de coordonnées source.</span><span class="sxs-lookup"><span data-stu-id="28b93-117">An angle in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="28b93-118">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="28b93-118">_srcRef_</span></span> <br/> |<span data-ttu-id="28b93-119">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28b93-119">Required</span></span>  <br/> |<span data-ttu-id="28b93-120">**String**</span><span class="sxs-lookup"><span data-stu-id="28b93-120">**String**</span></span> <br/> | <span data-ttu-id="28b93-121">Référence à une cellule de l’objet source, comme une forme, un groupe, une page, etc.</span><span class="sxs-lookup"><span data-stu-id="28b93-121">A reference to a cell in the source object, such as a shape, group, page, and so on.</span></span>  <br/> |
| <span data-ttu-id="28b93-122">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="28b93-122">_dstRef_</span></span> <br/> |<span data-ttu-id="28b93-123">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="28b93-123">Required</span></span>  <br/> |<span data-ttu-id="28b93-124">**String**</span><span class="sxs-lookup"><span data-stu-id="28b93-124">**String**</span></span> <br/> |<span data-ttu-id="28b93-125">Référence à une cellule de l’objet de destination, comme une forme, un groupe, une page, etc.</span><span class="sxs-lookup"><span data-stu-id="28b93-125">A reference to a cell in the destination object, such as a shape, group, page, and so on.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28b93-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="28b93-126">Remarks</span></span>

<span data-ttu-id="28b93-p103">Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="28b93-p103">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="28b93-129">Les coordonnées source et cible doivent se trouver sur la même page.</span><span class="sxs-lookup"><span data-stu-id="28b93-129">The source and destination coordinates must be on the same page.</span></span>
  
<span data-ttu-id="28b93-130">Si la destination est une page, qui n’a pas de parent, le résultat est exprimé dans les coordonnées locales de la page.</span><span class="sxs-lookup"><span data-stu-id="28b93-130">If the destination is a page, which has no parent, the result is expressed in page's local coordinates.</span></span>
  

