---
title: Y, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Représente la coordonnée y qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360150"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="99062-103">Y, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="99062-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="99062-104">Représente la coordonnée *y* qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="99062-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="99062-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="99062-105">Remarks</span></span>

<span data-ttu-id="99062-106">Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="99062-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99062-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="99062-107">Cell name:</span></span>  <br/> | <span data-ttu-id="99062-108">Vérifie.</span><span class="sxs-lookup"><span data-stu-id="99062-108">Controls.</span></span>  <span data-ttu-id="99062-109">*nom* . Contrôles Yoù.</span><span class="sxs-lookup"><span data-stu-id="99062-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="99062-110">*Name* est le nom de la ligne Controls.</span><span class="sxs-lookup"><span data-stu-id="99062-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="99062-111">Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="99062-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="99062-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="99062-112">Section index:</span></span>  <br/> |<span data-ttu-id="99062-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="99062-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="99062-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="99062-114">Row index:</span></span>  <br/> |<span data-ttu-id="99062-115">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="99062-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="99062-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="99062-116">Cell index:</span></span>  <br/> |<span data-ttu-id="99062-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="99062-117">**visCtlY**</span></span> <br/> |
   

