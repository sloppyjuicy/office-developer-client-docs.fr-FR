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
description: 'Détermine la coordonnée x du centre de rotation du bloc de texte par rapport à l’origine de la forme. La formule par défaut est la suivante :'
ms.openlocfilehash: 836f5c807d0c0e53efc825f62f60429274282165
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423495"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="2f5fd-104">TxtPinX, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="2f5fd-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="2f5fd-105">Détermine la  *coordonnée x*  du centre de rotation du bloc de texte par rapport à l’origine de la forme.</span><span class="sxs-lookup"><span data-stu-id="2f5fd-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="2f5fd-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-106">The default formula is:</span></span> 
  
<span data-ttu-id="2f5fd-107">= Largeur \* 0,5</span><span class="sxs-lookup"><span data-stu-id="2f5fd-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2f5fd-108">Remarques</span><span class="sxs-lookup"><span data-stu-id="2f5fd-108">Remarks</span></span>

<span data-ttu-id="2f5fd-109">Pour obtenir une référence à la cellule TxtPinX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f5fd-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-110">Cell name:</span></span>  <br/> | <span data-ttu-id="2f5fd-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="2f5fd-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="2f5fd-112">Pour obtenir une référence à la cellule TxtPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f5fd-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-113">Section index:</span></span>  <br/> |<span data-ttu-id="2f5fd-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2f5fd-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2f5fd-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-115">Row index:</span></span>  <br/> |<span data-ttu-id="2f5fd-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="2f5fd-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="2f5fd-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2f5fd-117">Cell index:</span></span>  <br/> |<span data-ttu-id="2f5fd-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="2f5fd-118">**visXFormPinX**</span></span> <br/> |
   

