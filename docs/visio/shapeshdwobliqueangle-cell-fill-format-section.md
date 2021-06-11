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
ms.openlocfilehash: 005415e497a4d985d3fb8ec70d62ba40d9e80c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414031"
---
# <a name="shapeshdwobliqueangle-cell-fill-format-section"></a><span data-ttu-id="d2479-103">ShapeShdwObliqueAngle, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="d2479-103">ShapeShdwObliqueAngle Cell (Fill Format Section)</span></span>

<span data-ttu-id="d2479-104">Indique l'angle de la direction oblique de l'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="d2479-104">Specifies the angle of oblique direction of a shape's shadow.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2479-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2479-105">Remarks</span></span>

<span data-ttu-id="d2479-106">Une valeur de zéro (0) dans cette cellule indique que la direction de l'angle est verticale et mesurée dans le sens des aiguilles d'une montre.</span><span class="sxs-lookup"><span data-stu-id="d2479-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
<span data-ttu-id="d2479-107">Cette valeur correspond à celle du paramètre **Orientation** de la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="d2479-107">This value corresponds to the value of the **Direction** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="d2479-108">Pour obtenir une référence à la cellule ShapeShdwObliqueAngle par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d2479-108">To get a reference to the ShapeShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2479-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d2479-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d2479-110">ShapeShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="d2479-110">ShapeShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="d2479-111">Pour obtenir une référence à la cellule ShapeShdwObliqueAngle à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d2479-111">To get a reference to the ShapeShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2479-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d2479-112">Section index:</span></span>  <br/> |<span data-ttu-id="d2479-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2479-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2479-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d2479-114">Row index:</span></span>  <br/> |<span data-ttu-id="d2479-115">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="d2479-115">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="d2479-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2479-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d2479-117">**visFillShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="d2479-117">**visFillShdwObliqueAngle**</span></span> <br/> |
   

