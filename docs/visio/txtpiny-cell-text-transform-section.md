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
description: "Détermine la coordonnée y du centre de la rotation du bloc de texte par rapport à l'origine de la forme. La formule par défaut est la suivante :"
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316421"
---
# <a name="txtpiny-cell-text-transform-section"></a><span data-ttu-id="d8f50-104">TxtPinY, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="d8f50-104">TxtPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="d8f50-105">Détermine la coordonnée *y* du centre de la rotation du bloc de texte par rapport à l'origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="d8f50-105">Determines the  *y*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="d8f50-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="d8f50-106">The default formula is:</span></span> 
  
<span data-ttu-id="d8f50-107">= Hauteur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="d8f50-107">= Height \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8f50-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="d8f50-108">Remarks</span></span>

<span data-ttu-id="d8f50-109">Pour obtenir une référence à la cellule TxtPinY par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d8f50-109">To get a reference to the TxtPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d8f50-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d8f50-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d8f50-111">TxtPinY</span><span class="sxs-lookup"><span data-stu-id="d8f50-111">TxtPinY</span></span>  <br/> |
   
<span data-ttu-id="d8f50-112">Pour obtenir une référence à la cellule TxtPinY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d8f50-112">To get a reference to the TxtPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d8f50-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d8f50-113">Section index:</span></span>  <br/> |<span data-ttu-id="d8f50-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="d8f50-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d8f50-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d8f50-115">Row index:</span></span>  <br/> |<span data-ttu-id="d8f50-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="d8f50-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="d8f50-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d8f50-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d8f50-118">**visXFormPinY**</span><span class="sxs-lookup"><span data-stu-id="d8f50-118">**visXFormPinY**</span></span> <br/> |
   

