---
title: TxtLocPinX, cellule (section Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: "Détermine la coordonnée x du centre de rotation du bloc de texte par rapport à l'origine du bloc de texte. La formule par défaut est la suivante :"
ms.openlocfilehash: 390f8129e8000a043969eda0ab1c8e4ef62515ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316449"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="35aaf-104">TxtLocPinX, cellule (section Text Transform)</span><span class="sxs-lookup"><span data-stu-id="35aaf-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="35aaf-105">Détermine la coordonnée *x* du centre de rotation du bloc de texte par rapport à l'origine du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="35aaf-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="35aaf-106">La formule par défaut est la suivante :</span><span class="sxs-lookup"><span data-stu-id="35aaf-106">The default formula is:</span></span> 
  
<span data-ttu-id="35aaf-107">= TxtWidth \* 0,5</span><span class="sxs-lookup"><span data-stu-id="35aaf-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="35aaf-108">Cette formule calcule le centre horizontal du bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="35aaf-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="35aaf-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="35aaf-109">Remarks</span></span>

<span data-ttu-id="35aaf-110">Pour obtenir une référence à la cellule TxtLocPinX par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="35aaf-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35aaf-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="35aaf-111">Cell name:</span></span>  <br/> | <span data-ttu-id="35aaf-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="35aaf-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="35aaf-113">Pour obtenir une référence à la cellule TxtLocPinX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="35aaf-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35aaf-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="35aaf-114">Section index:</span></span>  <br/> |<span data-ttu-id="35aaf-115">**Définis**</span><span class="sxs-lookup"><span data-stu-id="35aaf-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="35aaf-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="35aaf-116">Row index:</span></span>  <br/> |<span data-ttu-id="35aaf-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="35aaf-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="35aaf-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="35aaf-118">Cell index:</span></span>  <br/> |<span data-ttu-id="35aaf-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="35aaf-119">**visXFormLocPinX**</span></span> <br/> |
   

