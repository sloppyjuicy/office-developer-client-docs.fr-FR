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
description: Représente la coordonnée x qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406450"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="577f6-103">X, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="577f6-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="577f6-104">Représente la coordonnée *x* qui indique l'emplacement de la poignée de contrôle d'une forme en coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="577f6-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="577f6-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="577f6-105">Remarks</span></span>

<span data-ttu-id="577f6-106">Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="577f6-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="577f6-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="577f6-107">Cell name:</span></span>  <br/> | <span data-ttu-id="577f6-108">Vérifie.</span><span class="sxs-lookup"><span data-stu-id="577f6-108">Controls.</span></span>  <span data-ttu-id="577f6-109">*nom* . X où Controls.</span><span class="sxs-lookup"><span data-stu-id="577f6-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="577f6-110">*Name* est le nom de la ligne Controls.</span><span class="sxs-lookup"><span data-stu-id="577f6-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="577f6-111">Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="577f6-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="577f6-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="577f6-112">Section index:</span></span>  <br/> |<span data-ttu-id="577f6-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="577f6-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="577f6-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="577f6-114">Row index:</span></span>  <br/> |<span data-ttu-id="577f6-115">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="577f6-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="577f6-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="577f6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="577f6-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="577f6-117">**visCtlX**</span></span> <br/> |
   

