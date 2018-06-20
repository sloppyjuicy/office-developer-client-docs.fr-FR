---
title: X, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Représente le x-coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.
ms.openlocfilehash: e47b26c72709a2ee74675e73b8e8424bbfb325e3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790056"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="c1793-103">X, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="c1793-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="c1793-104">Représente le *x* -coordonnées qui indique l’emplacement de la poignée de contrôle d’une forme dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="c1793-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c1793-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c1793-105">Remarks</span></span>

<span data-ttu-id="c1793-106">Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c1793-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1793-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c1793-107">Cell name:</span></span>  <br/> | <span data-ttu-id="c1793-108">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="c1793-108">Controls.</span></span>  <span data-ttu-id="c1793-109">*nom* . X où contrôle.</span><span class="sxs-lookup"><span data-stu-id="c1793-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="c1793-110">*nom* est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="c1793-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="c1793-111">Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c1793-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1793-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c1793-112">Section index:</span></span>  <br/> |<span data-ttu-id="c1793-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="c1793-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="c1793-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c1793-114">Row index:</span></span>  <br/> |<span data-ttu-id="c1793-115">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c1793-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="c1793-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c1793-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c1793-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="c1793-117">**visCtlX**</span></span> <br/> |
   

