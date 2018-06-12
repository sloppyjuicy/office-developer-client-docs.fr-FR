---
title: TxtWidth, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Détermine la largeur du bloc de texte. La formule par défaut est la suivante :'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789969"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="fb4b3-104">TxtWidth, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="fb4b3-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="fb4b3-p102">Détermine la largeur du bloc de texte. La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-p102">Determines the width of the text block. The default formula is:</span></span>
  
<span data-ttu-id="fb4b3-107">= Largeur \* 1</span><span class="sxs-lookup"><span data-stu-id="fb4b3-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="fb4b3-108">Note</span><span class="sxs-lookup"><span data-stu-id="fb4b3-108">Remarks</span></span>

<span data-ttu-id="fb4b3-109">Pour obtenir une référence à la cellule TxtWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb4b3-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-110">Cell name:</span></span>  <br/> | <span data-ttu-id="fb4b3-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="fb4b3-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="fb4b3-112">Pour obtenir une référence à la cellule TxtWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb4b3-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-113">Section index:</span></span>  <br/> |<span data-ttu-id="fb4b3-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb4b3-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb4b3-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-115">Row index:</span></span>  <br/> |<span data-ttu-id="fb4b3-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="fb4b3-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="fb4b3-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fb4b3-117">Cell index:</span></span>  <br/> |<span data-ttu-id="fb4b3-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="fb4b3-118">**visXFormWidth**</span></span> <br/> |
   

