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
description: Représente la valeur y-coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.
ms.openlocfilehash: 8104ae6d647feb4e1b83474b63f40e243e5405e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790076"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="83822-103">Y, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="83822-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="83822-104">Représente la valeur *y* -coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="83822-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="83822-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="83822-105">Remarks</span></span>

<span data-ttu-id="83822-106">Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="83822-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83822-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="83822-107">Cell name:</span></span>  <br/> | <span data-ttu-id="83822-108">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="83822-108">Controls.</span></span>  <span data-ttu-id="83822-109">*nom* . Contrôles Ywhere.</span><span class="sxs-lookup"><span data-stu-id="83822-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="83822-110">*nom* est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="83822-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="83822-111">Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="83822-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83822-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="83822-112">Section index:</span></span>  <br/> |<span data-ttu-id="83822-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="83822-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="83822-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="83822-114">Row index:</span></span>  <br/> |<span data-ttu-id="83822-115">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="83822-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="83822-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="83822-116">Cell index:</span></span>  <br/> |<span data-ttu-id="83822-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="83822-117">**visCtlY**</span></span> <br/> |
   

