---
title: BlockSizeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Détermine la taille de bloc horizontal, la zone dans laquelle vos formes doit entrer sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: 68ed13b85583326c25635049d7e85babe62d5eb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788155"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="9799a-103">BlockSizeX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="9799a-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="9799a-104">Détermine la taille de bloc horizontal, la zone dans laquelle vos formes doit entrer sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page **, puis cliquez sur **Autres Options de mise en page**).</span><span class="sxs-lookup"><span data-stu-id="9799a-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9799a-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="9799a-105">Remarks</span></span>

<span data-ttu-id="9799a-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **disposition et positionnement** (sous l’onglet **Création** , cliquez sur la flèche dans le groupe **Mise en Page** , cliquez sur l’onglet **disposition et positionnement** , puis cliquez sur **espacement**).</span><span class="sxs-lookup"><span data-stu-id="9799a-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="9799a-107">Pour obtenir une référence à la cellule BlockSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="9799a-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9799a-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9799a-108">Cell name:</span></span>  <br/> |<span data-ttu-id="9799a-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="9799a-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="9799a-110">Pour obtenir une référence à la cellule BlockSizeX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9799a-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9799a-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9799a-111">Section index:</span></span>  <br/> |<span data-ttu-id="9799a-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9799a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9799a-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9799a-113">Row index:</span></span>  <br/> |<span data-ttu-id="9799a-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9799a-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="9799a-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9799a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="9799a-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="9799a-116">**visPLOBlockSizeX**</span></span> <br/> |
   

