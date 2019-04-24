---
title: TxtLocPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: "Détermine la coordonnée y du centre de rotation du bloc de texte par rapport à l'origine du bloc de texte. La formule par défaut est la suivante :"
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317730"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="27366-104">TxtLocPinY, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="27366-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="27366-105">Détermine la coordonnée *y* du centre de rotation du bloc de texte par rapport à l'origine du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="27366-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="27366-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="27366-106">The default formula is:</span></span> 
  
<span data-ttu-id="27366-107">= TxtHeight \* 0,5</span><span class="sxs-lookup"><span data-stu-id="27366-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="27366-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="27366-108">Remarks</span></span>

<span data-ttu-id="27366-109">Pour obtenir une référence à la cellule TxtLocPinY par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="27366-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27366-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27366-110">Cell name:</span></span>  <br/> | <span data-ttu-id="27366-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="27366-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="27366-112">Pour obtenir une référence à la cellule TxtLocPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="27366-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27366-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="27366-113">Section index:</span></span>  <br/> |<span data-ttu-id="27366-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="27366-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27366-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="27366-115">Row index:</span></span>  <br/> |<span data-ttu-id="27366-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="27366-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="27366-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="27366-117">Cell index:</span></span>  <br/> |<span data-ttu-id="27366-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="27366-118">**visXFormLocPinY**</span></span> <br/> |
   

