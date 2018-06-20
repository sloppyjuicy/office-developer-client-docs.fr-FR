---
title: TxtPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Détermine le x-coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789947"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="c341f-104">TxtPinX, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="c341f-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="c341f-105">Détermine le *x* -coordonnées du centre du bloc de texte de rotation par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="c341f-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="c341f-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="c341f-106">The default formula is:</span></span> 
  
<span data-ttu-id="c341f-107">= Largeur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="c341f-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c341f-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="c341f-108">Remarks</span></span>

<span data-ttu-id="c341f-109">Pour obtenir une référence à la cellule TxtPinX par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c341f-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c341f-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c341f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c341f-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="c341f-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="c341f-112">Pour obtenir une référence à la cellule TxtPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c341f-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c341f-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c341f-113">Section index:</span></span>  <br/> |<span data-ttu-id="c341f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c341f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c341f-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c341f-115">Row index:</span></span>  <br/> |<span data-ttu-id="c341f-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="c341f-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="c341f-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c341f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c341f-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="c341f-118">**visXFormPinX**</span></span> <br/> |
   

