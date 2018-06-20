---
title: ScaleY, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Indique le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789593"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="93fe4-103">ScaleY, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="93fe4-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="93fe4-104">Indique le pourcentage d’agrandissement de la page de dessin sur la page d’impression.</span><span class="sxs-lookup"><span data-stu-id="93fe4-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="93fe4-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="93fe4-105">Remarks</span></span>

<span data-ttu-id="93fe4-106">Cette valeur est utilisée uniquement lorsque la valeur de la cellule OnPage est FALSE.</span><span class="sxs-lookup"><span data-stu-id="93fe4-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="93fe4-107">Les cellules ScaleX et ScaleY ont toujours la même valeur, qui correspond à la valeur du paramètre **Ajuster sur** sous l’onglet **Configuration de l’impression** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).</span><span class="sxs-lookup"><span data-stu-id="93fe4-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="93fe4-108">Pour obtenir une référence à la cellule ScaleY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="93fe4-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93fe4-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="93fe4-109">Cell name:</span></span>  <br/> |<span data-ttu-id="93fe4-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="93fe4-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="93fe4-111">Pour obtenir une référence à la cellule ScaleY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="93fe4-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="93fe4-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="93fe4-112">Section index:</span></span>  <br/> |<span data-ttu-id="93fe4-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="93fe4-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="93fe4-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="93fe4-114">Row index:</span></span>  <br/> |<span data-ttu-id="93fe4-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="93fe4-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="93fe4-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="93fe4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="93fe4-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="93fe4-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

