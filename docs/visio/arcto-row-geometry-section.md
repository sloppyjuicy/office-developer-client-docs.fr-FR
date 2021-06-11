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
description: Contient les coordonnées x - et y - et courbe d’un arc circulaire.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430041"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="5bf14-103">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="5bf14-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="5bf14-104">Contient les  *coordonnées x*  - et  *y*  - et courbe d’un arc circulaire.</span><span class="sxs-lookup"><span data-stu-id="5bf14-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="5bf14-105">La ligne ArcTo contient les cellules suivantes.</span><span class="sxs-lookup"><span data-stu-id="5bf14-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="5bf14-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5bf14-106">**Cell**</span></span>|<span data-ttu-id="5bf14-107">**Description**</span><span class="sxs-lookup"><span data-stu-id="5bf14-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bf14-108">X</span><span class="sxs-lookup"><span data-stu-id="5bf14-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="5bf14-109">Coordonnée  *x*  du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="5bf14-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="5bf14-110">Y</span><span class="sxs-lookup"><span data-stu-id="5bf14-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="5bf14-111">Coordonnée  *y*  du sommet de fin d’un arc.</span><span class="sxs-lookup"><span data-stu-id="5bf14-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="5bf14-112">A</span><span class="sxs-lookup"><span data-stu-id="5bf14-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="5bf14-113">Distance entre le milieu de l'arc et le milieu de sa corde.</span><span class="sxs-lookup"><span data-stu-id="5bf14-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bf14-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="5bf14-114">Remarks</span></span>

<span data-ttu-id="5bf14-p101">Les arcs dessinés dans Visio sont des arcs elliptiques, même s'ils sont basés sur des cercles. Par défaut, les arcs dessinés sont représentés par une ligne EllipticalArcTo dans la fenêtre Feuille ShapeSheet. Pour afficher une ligne ArcTo dans une fenêtre Feuille ShapeSheet, vous devez dessiner un arc puis changer le type de ligne EllipticalArcTo en type de ligne ArcTo ; de ce fait, vous changez un arc elliptique en arc circulaire.</span><span class="sxs-lookup"><span data-stu-id="5bf14-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="5bf14-118">Pour changer de type de ligne, cliquez avec le bouton droit de la souris sur la ligne, puis cliquez sur **Modifier le type de ligne** dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="5bf14-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

