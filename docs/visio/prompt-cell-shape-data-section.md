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
description: Spécifie le texte descriptif ou d’instructions qui apparaît comme une info-bulle lorsque vous positionnez la souris sur une valeur dans la fenêtre données de forme.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789355"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="d6b89-103">Prompt, cellule (section Shape Data)</span><span class="sxs-lookup"><span data-stu-id="d6b89-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="d6b89-104">Spécifie le texte descriptif ou d’instructions qui apparaît comme une info-bulle lorsque vous positionnez la souris sur une valeur dans la fenêtre **Données de forme** .</span><span class="sxs-lookup"><span data-stu-id="d6b89-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d6b89-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d6b89-105">Remarks</span></span>

<span data-ttu-id="d6b89-106">Pour obtenir une référence à la cellule Prompt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="d6b89-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6b89-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d6b89-107">Cell name:</span></span>  <br/> | <span data-ttu-id="d6b89-108">Propriétés.  *Nom* . Invite où *nom* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="d6b89-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="d6b89-109">Pour obtenir une référence à la cellule Prompt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d6b89-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d6b89-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d6b89-110">Section index:</span></span>  <br/> |<span data-ttu-id="d6b89-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="d6b89-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="d6b89-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d6b89-112">Row index:</span></span>  <br/> |<span data-ttu-id="d6b89-113">**visRowProp +** *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d6b89-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d6b89-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d6b89-114">Cell index:</span></span>  <br/> |<span data-ttu-id="d6b89-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="d6b89-115">**visCustPropsPrompt**</span></span> <br/> |
   

