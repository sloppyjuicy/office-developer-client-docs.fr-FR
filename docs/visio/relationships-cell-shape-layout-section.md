---
title: Relationships, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80005
localization_priority: Normal
ms.assetid: 4168cd98-9674-1233-254f-0afe81b7245b
description: Stocke les relations entre les conteneurs, les listes, les légendes et les formes.
ms.openlocfilehash: b270366fe1045aea3d628150c82e7fd798fa21df
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406408"
---
# <a name="relationships-cell-shape-layout-section"></a><span data-ttu-id="bc744-103">Relationships, cellule (section Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="bc744-103">Relationships Cell (Shape Layout Section)</span></span>

<span data-ttu-id="bc744-104">Stocke les relations entre les conteneurs, les listes, les légendes et les formes.</span><span class="sxs-lookup"><span data-stu-id="bc744-104">Stores the relationships between containers, lists, callouts, and shapes.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc744-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="bc744-105">Remarks</span></span>

 <span data-ttu-id="bc744-106">Microsoft Visio utilise la cellule Relationships pour stocker les relations qui impliquent cette forme.</span><span class="sxs-lookup"><span data-stu-id="bc744-106">Microsoft Visio uses the Relationships cell to store the relationships that involve this shape.</span></span> <span data-ttu-id="bc744-107">Une série de fonctions DEPENDSON, avec les paramètres affichés, est utilisée pour représenter les relations avec cette forme, comme l’illustre le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="bc744-107">A series of DEPENDSON functions, with the parameters shown, are used to represent relationships with this shape, as shown in the following table.</span></span> 
  
|<span data-ttu-id="bc744-108">**Premier paramètre**</span><span class="sxs-lookup"><span data-stu-id="bc744-108">**First parameter**</span></span>|<span data-ttu-id="bc744-109">**Paramètres supplémentaires**</span><span class="sxs-lookup"><span data-stu-id="bc744-109">**Additional parameters**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bc744-110">1 </span><span class="sxs-lookup"><span data-stu-id="bc744-110">1</span></span>  <br/> |<span data-ttu-id="bc744-111">Formes membres de ce conteneur.</span><span class="sxs-lookup"><span data-stu-id="bc744-111">Shapes that are members of this container.</span></span>  <br/> |
|<span data-ttu-id="bc744-112">2 </span><span class="sxs-lookup"><span data-stu-id="bc744-112">2</span></span>  <br/> |<span data-ttu-id="bc744-113">Formes membres de cette liste.</span><span class="sxs-lookup"><span data-stu-id="bc744-113">Shapes that are members of this list.</span></span>  <br/> |
|<span data-ttu-id="bc744-114">3 </span><span class="sxs-lookup"><span data-stu-id="bc744-114">3</span></span>  <br/> |<span data-ttu-id="bc744-115">Légendes associées à cette forme.</span><span class="sxs-lookup"><span data-stu-id="bc744-115">Callouts that are associated with this shape.</span></span>  <br/> |
|<span data-ttu-id="bc744-116">4 </span><span class="sxs-lookup"><span data-stu-id="bc744-116">4</span></span>  <br/> |<span data-ttu-id="bc744-117">Conteneurs dont cette forme est membre.</span><span class="sxs-lookup"><span data-stu-id="bc744-117">Containers that this shape is a member of.</span></span>  <br/> |
|<span data-ttu-id="bc744-118">5 </span><span class="sxs-lookup"><span data-stu-id="bc744-118">5</span></span>  <br/> |<span data-ttu-id="bc744-119">Liste dont cet élément de liste est membre.</span><span class="sxs-lookup"><span data-stu-id="bc744-119">List that this list item is a member of.</span></span>  <br/> |
|<span data-ttu-id="bc744-120">6 </span><span class="sxs-lookup"><span data-stu-id="bc744-120">6</span></span>  <br/> |<span data-ttu-id="bc744-121">Forme associée à cette légende.</span><span class="sxs-lookup"><span data-stu-id="bc744-121">Shape associated with this callout.</span></span>  <br/> |
|<span data-ttu-id="bc744-122">7 </span><span class="sxs-lookup"><span data-stu-id="bc744-122">7</span></span>  <br/> |<span data-ttu-id="bc744-123">Conteneur sur le bord de la limite gauche sur laquelle réside la forme.</span><span class="sxs-lookup"><span data-stu-id="bc744-123">Container on the left boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="bc744-124">8 </span><span class="sxs-lookup"><span data-stu-id="bc744-124">8</span></span>  <br/> |<span data-ttu-id="bc744-125">Conteneur sur le bord de la limite droite sur laquelle réside la forme.</span><span class="sxs-lookup"><span data-stu-id="bc744-125">Container on the right boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="bc744-126">9 </span><span class="sxs-lookup"><span data-stu-id="bc744-126">9</span></span>  <br/> |<span data-ttu-id="bc744-127">Conteneur sur le bord de la limite haute sur laquelle réside la forme.</span><span class="sxs-lookup"><span data-stu-id="bc744-127">Container on the top boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="bc744-128">10 </span><span class="sxs-lookup"><span data-stu-id="bc744-128">10</span></span>  <br/> |<span data-ttu-id="bc744-129">Conteneur sur le bord de la limite basse sur laquelle réside la forme.</span><span class="sxs-lookup"><span data-stu-id="bc744-129">Container on the bottom boundary edge of which this shape sits.</span></span>  <br/> |
|<span data-ttu-id="bc744-130">11</span><span class="sxs-lookup"><span data-stu-id="bc744-130">11</span></span>  <br/> |<span data-ttu-id="bc744-131">Liste sur laquelle chevauche cette liste.</span><span class="sxs-lookup"><span data-stu-id="bc744-131">List that this list overlaps.</span></span>  <br/> |
   
<span data-ttu-id="bc744-132">Pour obtenir une référence à la cellule Relationships par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bc744-132">To get a reference to the Relationships cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc744-133">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="bc744-133">Cell name:</span></span>  <br/> |<span data-ttu-id="bc744-134">Relations</span><span class="sxs-lookup"><span data-stu-id="bc744-134">Relationships</span></span>  <br/> |
   
<span data-ttu-id="bc744-135">Pour obtenir une référence à la cellule Relationships à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bc744-135">To get a reference to the Relationships cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bc744-136">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bc744-136">Section index:</span></span>  <br/> |<span data-ttu-id="bc744-137">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bc744-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="bc744-138">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bc744-138">Row index:</span></span>  <br/> |<span data-ttu-id="bc744-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="bc744-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="bc744-140">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bc744-140">Cell index:</span></span>  <br/> |<span data-ttu-id="bc744-141">**visSLORelationships**</span><span class="sxs-lookup"><span data-stu-id="bc744-141">**visSLORelationships**</span></span> <br/> |
   

