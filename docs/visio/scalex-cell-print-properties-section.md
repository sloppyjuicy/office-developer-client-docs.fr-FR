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
description: Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’impression.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410209"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="59121-103">ScaleX, cellule (section Print Properties)</span><span class="sxs-lookup"><span data-stu-id="59121-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="59121-104">Spécifie le pourcentage d’agrandissement de la page de dessin sur la page d’impression.</span><span class="sxs-lookup"><span data-stu-id="59121-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="59121-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="59121-105">Remarks</span></span>

<span data-ttu-id="59121-106">Cette valeur n’est utilisée que lorsque la valeur de la cellule OnPage est FALSE.</span><span class="sxs-lookup"><span data-stu-id="59121-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="59121-107">Les cellules ScaleX et ScaleY ont toujours la même valeur, ce qui  correspond à la valeur du paramètre  Ajuster à sous l’onglet Configuration de l’impression de la boîte de dialogue Mise en **page** (sous l’onglet Création, cliquez sur la flèche Mise en **page).** </span><span class="sxs-lookup"><span data-stu-id="59121-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="59121-108">Pour obtenir une référence à la cellule ScaleX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="59121-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59121-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="59121-109">Cell name:</span></span>  <br/> |<span data-ttu-id="59121-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="59121-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="59121-111">Pour obtenir une référence à la cellule ScaleX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="59121-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="59121-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="59121-112">Section index:</span></span>  <br/> |<span data-ttu-id="59121-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="59121-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="59121-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="59121-114">Row index:</span></span>  <br/> |<span data-ttu-id="59121-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="59121-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="59121-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="59121-116">Cell index:</span></span>  <br/> |<span data-ttu-id="59121-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="59121-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

