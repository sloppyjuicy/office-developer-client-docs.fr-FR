---
title: Y Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Représente la valeur y-coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local. Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790110"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="d1f12-104">Y Dynamics, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="d1f12-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="d1f12-105">Représente la valeur *y* -coordonnées d’un point d’ancrage d’une poignée de contrôle dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="d1f12-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="d1f12-106">Le point d'ancrage est utilisé pour l'étirement dynamique des formes.</span><span class="sxs-lookup"><span data-stu-id="d1f12-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d1f12-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="d1f12-107">Remarks</span></span>

<span data-ttu-id="d1f12-108">Pour obtenir une référence à la cellule Y Dynamics par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d1f12-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1f12-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d1f12-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d1f12-110">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="d1f12-110">Controls.</span></span>  <span data-ttu-id="d1f12-111">*nom* . Contrôles YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="d1f12-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="d1f12-112">*nom* est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="d1f12-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="d1f12-113">Pour obtenir une référence à la cellule Y Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d1f12-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1f12-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d1f12-114">Section index:</span></span>  <br/> |<span data-ttu-id="d1f12-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="d1f12-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="d1f12-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d1f12-116">Row index:</span></span>  <br/> |<span data-ttu-id="d1f12-117">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d1f12-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d1f12-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d1f12-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d1f12-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="d1f12-119">**visCtlYDyn**</span></span> <br/> |
   

