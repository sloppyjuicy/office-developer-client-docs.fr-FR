---
title: ArcTo, ligne (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Contient les coordonnées x - et y-coordonnées et la courbure d’un arc circulaire.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788028"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="e1e52-103">ArcTo, ligne (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="e1e52-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="e1e52-104">Contient les coordonnées *x* - et *y* -coordonnées et la courbure d’un arc circulaire.</span><span class="sxs-lookup"><span data-stu-id="e1e52-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="e1e52-105">La ligne ArcTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1e52-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="e1e52-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e1e52-106">**Cell**</span></span>|<span data-ttu-id="e1e52-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1e52-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e1e52-108">X</span><span class="sxs-lookup"><span data-stu-id="e1e52-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e1e52-109">*X* -coordonnées du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="e1e52-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="e1e52-110">Y</span><span class="sxs-lookup"><span data-stu-id="e1e52-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e1e52-111">La valeur *y* -coordonnées du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="e1e52-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="e1e52-112">A</span><span class="sxs-lookup"><span data-stu-id="e1e52-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="e1e52-113">Distance entre le milieu de l'arc et le milieu de sa corde.</span><span class="sxs-lookup"><span data-stu-id="e1e52-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1e52-114">Notes</span><span class="sxs-lookup"><span data-stu-id="e1e52-114">Remarks</span></span>

<span data-ttu-id="e1e52-p101">Les arcs dessinés dans Visio sont des arcs elliptiques, même s'ils sont basés sur des cercles. Par défaut, les arcs dessinés sont représentés par une ligne EllipticalArcTo dans la fenêtre Feuille ShapeSheet. Pour afficher une ligne ArcTo dans une fenêtre Feuille ShapeSheet, vous devez dessiner un arc puis changer le type de ligne EllipticalArcTo en type de ligne ArcTo ; de ce fait, vous changez un arc elliptique en arc circulaire.</span><span class="sxs-lookup"><span data-stu-id="e1e52-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="e1e52-118">Pour modifier un type de ligne, avec le bouton droit à une ligne, puis cliquez sur **Modifier le Type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="e1e52-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

