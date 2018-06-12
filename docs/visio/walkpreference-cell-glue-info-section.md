---
title: WalkPreference, cellule (section Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Détermine si un point de fin d'une forme 1D se déplace vers un point de connexion horizontal ou vertical sur la forme à laquelle il est collé avec de la colle dynamique, lorsque la forme est déplacée dans une position ambiguë. Par défaut, les deux points de fin d'une forme 1D se déplacent vers les points de connexion horizontaux.
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790027"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="db439-104">WalkPreference, cellule (section Glue Info)</span><span class="sxs-lookup"><span data-stu-id="db439-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="db439-p102">Détermine si un point de fin d'une forme 1D se déplace vers un point de connexion horizontal ou vertical sur la forme à laquelle il est collé avec de la colle dynamique, lorsque la forme est déplacée dans une position ambiguë. Par défaut, les deux points de fin d'une forme 1D se déplacent vers les points de connexion horizontaux.</span><span class="sxs-lookup"><span data-stu-id="db439-p102">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position. By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="db439-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="db439-107">**Value**</span></span>|<span data-ttu-id="db439-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="db439-108">**Description**</span></span>|<span data-ttu-id="db439-109">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="db439-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="db439-110">1</span><span class="sxs-lookup"><span data-stu-id="db439-110">1</span></span>  <br/> | <span data-ttu-id="db439-111">Le point de début de la forme 1D se déplace vers un point de connexion vertical et le point de fin, vers un point de connexion horizontal (connexions haut / bas vers côté).</span><span class="sxs-lookup"><span data-stu-id="db439-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="db439-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="db439-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="db439-113">2</span><span class="sxs-lookup"><span data-stu-id="db439-113">2</span></span>  <br/> | <span data-ttu-id="db439-114">Le point de début de la forme 1D se déplace vers un point de connexion horizontal et le point de fin, vers un point de connexion vertical (connexions côté vers haut ou côté vers bas).</span><span class="sxs-lookup"><span data-stu-id="db439-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="db439-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="db439-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db439-116">Note</span><span class="sxs-lookup"><span data-stu-id="db439-116">Remarks</span></span>

<span data-ttu-id="db439-p103">Cette cellule n'a pas d'effet sur les liens dynamiques. Le comportement d'un lien dynamique est déterminé par son style de positionnement. Reportez-vous à la cellule RouteStyle pour connaître le style de positionnement par défaut des liens dynamiques d'une page ou à la cellule ShapeRouteStyle pour le style de positionnement d'un lien dynamique donné.</span><span class="sxs-lookup"><span data-stu-id="db439-p103">This cell has no effect on dynamic connectors. A dynamic connector's behavior is determined by its routing style. See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="db439-120">Pour obtenir une référence à la cellule WalkPreference par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="db439-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db439-121">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="db439-121">Cell name:</span></span>  <br/> | <span data-ttu-id="db439-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="db439-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="db439-123">Pour obtenir une référence à la cellule WalkPreference par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="db439-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db439-124">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="db439-124">Section index:</span></span>  <br/> |<span data-ttu-id="db439-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db439-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="db439-126">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="db439-126">Row index:</span></span>  <br/> |<span data-ttu-id="db439-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="db439-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="db439-128">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="db439-128">Cell index:</span></span>  <br/> |<span data-ttu-id="db439-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="db439-129">**visWalkPref**</span></span> <br/> |
   

