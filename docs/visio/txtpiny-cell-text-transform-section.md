---
title: TxtPinY, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Détermine la coordonnée y du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418490"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="20fd5-104">TxtPinY, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="20fd5-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="20fd5-105">Détermine la coordonnée  *y*  du centre de rotation du bloc de texte par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="20fd5-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="20fd5-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="20fd5-106">The default formula is:</span></span> 
  
<span data-ttu-id="20fd5-107">= Hauteur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="20fd5-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="20fd5-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="20fd5-108">Remarks</span></span>

<span data-ttu-id="20fd5-109">Pour obtenir une référence à la cellule TxtPinY par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="20fd5-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20fd5-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="20fd5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="20fd5-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="20fd5-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="20fd5-112">Pour obtenir une référence à la cellule TxtPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="20fd5-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="20fd5-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="20fd5-113">Section index:</span></span>  <br/> |<span data-ttu-id="20fd5-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="20fd5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="20fd5-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="20fd5-115">Row index:</span></span>  <br/> |<span data-ttu-id="20fd5-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="20fd5-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="20fd5-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="20fd5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="20fd5-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="20fd5-118">**visXFormPinY**</span></span> <br/> |
   

