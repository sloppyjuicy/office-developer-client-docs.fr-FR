---
title: ScaleX, cellule (section Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Indique le pourcentage d'agrandissement de la page de dessin sur la page de l'imprimante.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326711"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="f2f42-103">ScaleX, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="f2f42-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="f2f42-104">Indique le pourcentage d'agrandissement de la page de dessin sur la page de l'imprimante.</span><span class="sxs-lookup"><span data-stu-id="f2f42-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2f42-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2f42-105">Remarks</span></span>

<span data-ttu-id="f2f42-106">Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE.</span><span class="sxs-lookup"><span data-stu-id="f2f42-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="f2f42-107">Les cellules ScaleX et ScaleY ont toujours la même valeur, ce qui correspond à la valeur du paramètre ajuster sur dans l'onglet **configuration** de l'impression de la boîte de dialogue **mise en page** (sous l'onglet **création** , cliquez sur la flèche mise **en** **page** ).</span><span class="sxs-lookup"><span data-stu-id="f2f42-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="f2f42-108">Pour obtenir une référence à la cellule ScaleX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f2f42-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2f42-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f2f42-109">Cell name:</span></span>  <br/> |<span data-ttu-id="f2f42-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="f2f42-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="f2f42-111">Pour obtenir une référence à la cellule ScaleX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f2f42-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2f42-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f2f42-112">Section index:</span></span>  <br/> |<span data-ttu-id="f2f42-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="f2f42-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f2f42-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f2f42-114">Row index:</span></span>  <br/> |<span data-ttu-id="f2f42-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="f2f42-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="f2f42-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f2f42-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f2f42-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="f2f42-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

