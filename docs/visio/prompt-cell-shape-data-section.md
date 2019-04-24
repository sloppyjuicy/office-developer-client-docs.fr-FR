---
title: Prompt, cellule (section Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Contient la description ou l’instruction qui apparaît sous la forme d’un conseil lorsque vous positionnez la souris sur la valeur dans la fenêtre Données de forme.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326816"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="9437a-103">Prompt, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="9437a-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="9437a-104">Contient la description ou l’instruction qui apparaît sous la forme d’un conseil lorsque vous positionnez la souris sur la valeur dans la fenêtre **Données de forme**.</span><span class="sxs-lookup"><span data-stu-id="9437a-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9437a-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="9437a-105">Remarks</span></span>

<span data-ttu-id="9437a-106">Pour obtenir une référence à la cellule Prompt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9437a-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9437a-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9437a-107">Cell name:</span></span>  <br/> | <span data-ttu-id="9437a-108">Hélice.  *Nom* . Invite où *nom* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="9437a-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="9437a-109">Pour obtenir une référence à la cellule Prompt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9437a-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9437a-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9437a-110">Section index:</span></span>  <br/> |<span data-ttu-id="9437a-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="9437a-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="9437a-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9437a-112">Row index:</span></span>  <br/> |<span data-ttu-id="9437a-113">**visRowProp +** *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9437a-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="9437a-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9437a-114">Cell index:</span></span>  <br/> |<span data-ttu-id="9437a-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="9437a-115">**visCustPropsPrompt**</span></span> <br/> |
   

