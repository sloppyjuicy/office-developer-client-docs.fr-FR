---
title: LOCTOLOC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: Renvoie un point transformé en coordonnées locales dans le système de coordonnées de destination.
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427485"
---
# <a name="loctoloc-function"></a><span data-ttu-id="f9483-103">Fonction LOCTOLOC</span><span class="sxs-lookup"><span data-stu-id="f9483-103">LOCTOLOC Function</span></span>

<span data-ttu-id="f9483-104">Renvoie un point transformé en coordonnées locales dans le système de coordonnées de destination.</span><span class="sxs-lookup"><span data-stu-id="f9483-104">Returns a transformed point in local coordinates in the destination coordinate system.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f9483-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9483-105">Syntax</span></span>

<span data-ttu-id="f9483-106">LOCTOLOC(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span><span class="sxs-lookup"><span data-stu-id="f9483-106">LOCTOLOC(\*\* *srcPoint* \*\*, \*\* *srcRef* \*\*, \*\* *dstRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f9483-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9483-107">Parameters</span></span>

|<span data-ttu-id="f9483-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="f9483-108">**Name**</span></span>|<span data-ttu-id="f9483-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="f9483-109">**Required/Optional**</span></span>|<span data-ttu-id="f9483-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="f9483-110">**Data Type**</span></span>|<span data-ttu-id="f9483-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="f9483-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f9483-112">_srcPoint_</span><span class="sxs-lookup"><span data-stu-id="f9483-112">_srcPoint_</span></span> <br/> |<span data-ttu-id="f9483-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9483-113">Required</span></span>  <br/> |<span data-ttu-id="f9483-114">**String**</span><span class="sxs-lookup"><span data-stu-id="f9483-114">**String**</span></span> <br/> | <span data-ttu-id="f9483-115">Point en coordonnées locales du système de coordonnées source</span><span class="sxs-lookup"><span data-stu-id="f9483-115">A point in local coordinates in the source coordinate system.</span></span>  <br/> |
| <span data-ttu-id="f9483-116">_srcRef_</span><span class="sxs-lookup"><span data-stu-id="f9483-116">_srcRef_</span></span> <br/> |<span data-ttu-id="f9483-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9483-117">Required</span></span>  <br/> |<span data-ttu-id="f9483-118">**String**</span><span class="sxs-lookup"><span data-stu-id="f9483-118">**String**</span></span> <br/> | <span data-ttu-id="f9483-119">Référence à une cellule de l’objet source</span><span class="sxs-lookup"><span data-stu-id="f9483-119">A reference to a cell in the source object.</span></span>  <br/> |
| <span data-ttu-id="f9483-120">_dstRef_</span><span class="sxs-lookup"><span data-stu-id="f9483-120">_dstRef_</span></span> <br/> |<span data-ttu-id="f9483-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="f9483-121">Required</span></span>  <br/> |<span data-ttu-id="f9483-122">**String**</span><span class="sxs-lookup"><span data-stu-id="f9483-122">**String**</span></span> <br/> | <span data-ttu-id="f9483-123">Référence à une cellule de l’objet cible</span><span class="sxs-lookup"><span data-stu-id="f9483-123">A reference to a cell in the destination object.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f9483-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="f9483-124">Return value</span></span>

<span data-ttu-id="f9483-125">Chaîne</span><span class="sxs-lookup"><span data-stu-id="f9483-125">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f9483-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9483-126">Remarks</span></span>

<span data-ttu-id="f9483-p101">La fonction LOCTOLOC convertit un point des coordonnées locales de la forme source en coordonnées locales de la forme de destination. Elle permet, par exemple, de construire une forme en utilisant les points d’un autre système de coordonnées. Elle permet également de transformer un point local en coordonnées de page ou vice-versa.</span><span class="sxs-lookup"><span data-stu-id="f9483-p101">The LOCTOLOC function converts a point from local coordinates in a source shape to local coordinates in a destination shape. You can use this function to construct a shape, for example, in terms of a point from another coordinate space. You can also use this function to transform a local point to page coordinates, or vice versa.</span></span>
  
<span data-ttu-id="f9483-p102">Cette fonction peut être utilisée même si les formes source et cible sont contenues dans des groupes. Elle effectue également des ajustements de rotation et de retournement dans la transformation intermédiaire.</span><span class="sxs-lookup"><span data-stu-id="f9483-p102">This function works even when the source and destination shapes are within groups. It also adjusts for rotation and flips in the intermediate transformation.</span></span>
  
<span data-ttu-id="f9483-132">Les coordonnées source et cible doivent se trouver sur la même page.</span><span class="sxs-lookup"><span data-stu-id="f9483-132">The source and destination coordinates must be on the same page.</span></span>
  
## <a name="example"></a><span data-ttu-id="f9483-133">Exemple</span><span class="sxs-lookup"><span data-stu-id="f9483-133">Example</span></span>

<span data-ttu-id="f9483-134">La formule suivante convertit les coordonnées de l’axe local de la forme associée à la formule en un point de la page.</span><span class="sxs-lookup"><span data-stu-id="f9483-134">The following formula converts the local pin of the shape associated with the formula to a point on the page.</span></span>
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


