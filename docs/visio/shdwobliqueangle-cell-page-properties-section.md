---
title: ShdwObliqueAngle, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Contient une valeur indiquant l'angle de la direction oblique lors de l'application du type d'ombre par défaut de la page.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430426"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="7d653-103">ShdwObliqueAngle, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="7d653-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="7d653-104">Contient une valeur indiquant l'angle de la direction oblique lors de l'application du type d'ombre par défaut de la page.</span><span class="sxs-lookup"><span data-stu-id="7d653-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7d653-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d653-105">Remarks</span></span>

<span data-ttu-id="7d653-106">Une valeur de zéro (0) dans cette cellule indique que la direction de l'angle est verticale et mesurée dans le sens des aiguilles d'une montre.</span><span class="sxs-lookup"><span data-stu-id="7d653-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="7d653-107">L’angle décrit dans cette cellule est utilisé chaque fois que la cellule ShapeShdwType (le type d’ombre d’une forme sur la page) est définie sur Page Default (**visFSTPageDefault** ), et que le type d’ombre est oblique.</span><span class="sxs-lookup"><span data-stu-id="7d653-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="7d653-108">Le type d'ombre par défaut de la page est défini dans la cellule ShdwType.</span><span class="sxs-lookup"><span data-stu-id="7d653-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="7d653-109">Pour définir ce comportement pour une forme individuelle, utilisez la cellule ShapeShdwObliqueAngle dans la section Fill Format.</span><span class="sxs-lookup"><span data-stu-id="7d653-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="7d653-110">Pour obtenir une référence à la cellule ShdwObliqueAngle par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7d653-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d653-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="7d653-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7d653-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="7d653-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="7d653-113">Pour obtenir une référence à la cellule ShdwObliqueAngle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7d653-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d653-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7d653-114">Section index:</span></span>  <br/> |<span data-ttu-id="7d653-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7d653-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7d653-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7d653-116">Row index:</span></span>  <br/> |<span data-ttu-id="7d653-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="7d653-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="7d653-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7d653-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7d653-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="7d653-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   

