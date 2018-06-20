---
title: X Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Représente le x-coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local.
ms.openlocfilehash: 9dee2381c15ed2817df9f89ebc830cf31bf64c1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790080"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="3105e-103">X Dynamics, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="3105e-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="3105e-104">Représente le *x* -coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="3105e-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3105e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="3105e-105">Remarks</span></span>

<span data-ttu-id="3105e-106">Le point d'ancrage est utilisé pour l'étirement dynamique des formes.</span><span class="sxs-lookup"><span data-stu-id="3105e-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="3105e-107">Pour obtenir une référence à la cellule X Dynamics par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="3105e-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3105e-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3105e-108">Cell name:</span></span>  <br/> | <span data-ttu-id="3105e-109">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="3105e-109">Controls.</span></span>  <span data-ttu-id="3105e-110">*nom* . Contrôles XDynwhere.</span><span class="sxs-lookup"><span data-stu-id="3105e-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="3105e-111">*nom* est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="3105e-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="3105e-112">Pour obtenir une référence à la cellule X Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="3105e-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3105e-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="3105e-113">Section index:</span></span>  <br/> |<span data-ttu-id="3105e-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="3105e-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="3105e-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="3105e-115">Row index:</span></span>  <br/> |<span data-ttu-id="3105e-116">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3105e-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3105e-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="3105e-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3105e-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="3105e-118">**visCtlXDyn**</span></span> <br/> |
   

