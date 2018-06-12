---
title: ShapeShdwObliqueAngle, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033174
localization_priority: Normal
ms.assetid: bad4c512-e91f-d459-d65c-a4ab725c3c14
description: Indique l'angle de la direction oblique de l'ombre d'une forme.
ms.openlocfilehash: 11f172de33dfbb65d0176733f5c0bf8b33db483d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789660"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a><span data-ttu-id="a752b-103">ShapeShdwObliqueAngle, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="a752b-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span></span>

<span data-ttu-id="a752b-104">Indique l'angle de la direction oblique de l'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="a752b-104">Specifies the angle of oblique direction of a shape's shadow.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a752b-105">Note</span><span class="sxs-lookup"><span data-stu-id="a752b-105">Remarks</span></span>

<span data-ttu-id="a752b-106">Une valeur de zéro (0) dans cette cellule indique que la direction de l'angle est verticale et mesurée dans le sens des aiguilles d'une montre.</span><span class="sxs-lookup"><span data-stu-id="a752b-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
<span data-ttu-id="a752b-107">Cette valeur correspond à la valeur du paramètre **orientation** de la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="a752b-107">This value corresponds to the value of the **Direction** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="a752b-108">Pour obtenir une référence à la cellule ShapeShdwObliqueAngle par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="a752b-108">To get a reference to the ShapeShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a752b-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="a752b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="a752b-110">ShapeShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="a752b-110">ShapeShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="a752b-111">Pour obtenir une référence à la cellule ShapeShdwObliqueAngle par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a752b-111">To get a reference to the ShapeShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a752b-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a752b-112">Section index:</span></span>  <br/> |<span data-ttu-id="a752b-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a752b-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a752b-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a752b-114">Row index:</span></span>  <br/> |<span data-ttu-id="a752b-115">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="a752b-115">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="a752b-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a752b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a752b-117">**visFillShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="a752b-117">**visFillShdwObliqueAngle**</span></span> <br/> |
   

