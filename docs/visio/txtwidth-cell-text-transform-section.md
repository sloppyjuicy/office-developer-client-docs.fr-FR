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
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426092"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="f36da-104">TxtWidth, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="f36da-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="f36da-p102">Détermine la largeur du bloc de texte. La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="f36da-p102">Determines the width of the text block. The default formula is:</span></span>
  
<span data-ttu-id="f36da-107">= Largeur \* 1</span><span class="sxs-lookup"><span data-stu-id="f36da-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f36da-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="f36da-108">Remarks</span></span>

<span data-ttu-id="f36da-109">Pour obtenir une référence à la cellule TxtWidth par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f36da-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f36da-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f36da-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f36da-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="f36da-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="f36da-112">Pour obtenir une référence à la cellule TxtWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f36da-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f36da-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f36da-113">Section index:</span></span>  <br/> |<span data-ttu-id="f36da-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f36da-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f36da-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f36da-115">Row index:</span></span>  <br/> |<span data-ttu-id="f36da-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="f36da-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="f36da-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f36da-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f36da-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="f36da-118">**visXFormWidth**</span></span> <br/> |
   

