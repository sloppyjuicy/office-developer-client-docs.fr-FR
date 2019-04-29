---
title: DisplayLevel, cellule (section Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Détermine la bande du niveau d’affichage (la plage relative de regroupement de l’ordre de plan) pour la forme.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408144"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="d1849-103">DisplayLevel Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="d1849-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="d1849-104">Détermine la bande du niveau d’affichage (la plage relative de regroupement de l’ordre de plan) pour la forme.</span><span class="sxs-lookup"><span data-stu-id="d1849-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1849-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1849-105">Remarks</span></span>

<span data-ttu-id="d1849-p101">L’ordre de plan est l’ordre d’affichage pour les formes sur la page de dessin. Une forme plus élevée dans l’ordre de plan s’affiche devant une forme plus basse dans l’ordre de plan lorsqu’une des formes chevauche l’autre.</span><span class="sxs-lookup"><span data-stu-id="d1849-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="d1849-p102">Le niveau d’affichage scinde les formes en regroupements, ou bandes. Toutes les formes d’une bande donnée ont un ordre de plan plus élevé que les formes dans une bande plus basse. Par défaut, la plupart des formes ont un niveau d’affichage de zéro (0).</span><span class="sxs-lookup"><span data-stu-id="d1849-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="d1849-p103">La plage des niveaux d’affichage varie de -32 767 à +32 767. Les formes ayant le même niveau d’affichage sont combinées dans une bande unique, dans laquelle elles sont également classées de manière relative l’une par rapport à l’autre par ordre de plan.</span><span class="sxs-lookup"><span data-stu-id="d1849-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="d1849-113">Vous pouvez modifier l'ordre de plan des formes au sein d'une bande à l'aide des commandes **avancer**, **Envoyer**vers l'arrière, **mettre au premier plan**et **Envoyer à l'arrière**-plan.</span><span class="sxs-lookup"><span data-stu-id="d1849-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="d1849-114">Si ces commandes déplacent une forme en dehors de sa bande donnée, Microsoft Visio affiche la valeur réservée -32 768 dans la cellule DisplayLevel de la forme, à moins que la cellule ne soit protégée.</span><span class="sxs-lookup"><span data-stu-id="d1849-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="d1849-115">Dans ce cas, la forme ne peut pas être déplacée sur une autre bande et Visio affiche l’avertissement « La protection de la forme et/ou les propriétés de la couche empêchent de terminer l’exécution de cette commande ».</span><span class="sxs-lookup"><span data-stu-id="d1849-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="d1849-116">Pour obtenir une référence à la cellule DisplayLevel par le nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d1849-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1849-117">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d1849-117">Cell name:</span></span>  <br/> |<span data-ttu-id="d1849-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="d1849-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="d1849-119">Pour obtenir une référence à la cellule DisplayLevel à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d1849-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1849-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d1849-120">Section index:</span></span>  <br/> |<span data-ttu-id="d1849-121">**Définis**</span><span class="sxs-lookup"><span data-stu-id="d1849-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d1849-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d1849-122">Row index:</span></span>  <br/> |<span data-ttu-id="d1849-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="d1849-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="d1849-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d1849-124">Cell index:</span></span>  <br/> |<span data-ttu-id="d1849-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="d1849-125">**visSLODisplayLevel**</span></span> <br/> |
   

