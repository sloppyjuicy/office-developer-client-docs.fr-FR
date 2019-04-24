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
description: Indique le pourcentage d'agrandissement de la page de dessin sur la page de l'imprimante.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342727"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="b4a9e-103">ScaleY, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="b4a9e-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="b4a9e-104">Indique le pourcentage d'agrandissement de la page de dessin sur la page de l'imprimante.</span><span class="sxs-lookup"><span data-stu-id="b4a9e-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4a9e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="b4a9e-105">Remarks</span></span>

<span data-ttu-id="b4a9e-106">Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE.</span><span class="sxs-lookup"><span data-stu-id="b4a9e-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="b4a9e-107">Les cellules ScaleX et ScaleY ont toujours la même valeur, ce qui correspond à la valeur du paramètre ajuster sur dans l'onglet **configuration** de l'impression de la boîte de dialogue **mise en page** (sous l'onglet **création** , cliquez sur la flèche mise **en** **page** ).</span><span class="sxs-lookup"><span data-stu-id="b4a9e-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="b4a9e-108">Pour obtenir une référence à la cellule ScaleY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b4a9e-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4a9e-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b4a9e-109">Cell name:</span></span>  <br/> |<span data-ttu-id="b4a9e-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="b4a9e-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="b4a9e-111">Pour obtenir une référence à la cellule ScaleY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b4a9e-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4a9e-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b4a9e-112">Section index:</span></span>  <br/> |<span data-ttu-id="b4a9e-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="b4a9e-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b4a9e-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b4a9e-114">Row index:</span></span>  <br/> |<span data-ttu-id="b4a9e-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="b4a9e-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="b4a9e-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b4a9e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="b4a9e-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="b4a9e-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

