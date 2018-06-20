---
title: BlockSizeY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Détermine la taille de bloc vertical, la zone dans laquelle vos formes doit entrer sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: 283723bf902c07cfb044ab73107491df3c170a4d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788159"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="8eb0c-103">BlockSizeY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="8eb0c-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="8eb0c-104">Détermine la taille de bloc vertical, la zone dans laquelle vos formes doit entrer sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur **Autres Options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="8eb0c-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8eb0c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="8eb0c-105">Remarks</span></span>

<span data-ttu-id="8eb0c-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **disposition et positionnement** (sous l’onglet **Création** , cliquez sur la flèche dans le groupe **Mise en Page** , cliquez sur l’onglet **disposition et positionnement** , puis cliquez sur **espacement**).</span><span class="sxs-lookup"><span data-stu-id="8eb0c-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="8eb0c-107">Pour obtenir une référence à la cellule BlockSizeY par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="8eb0c-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8eb0c-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8eb0c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8eb0c-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="8eb0c-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="8eb0c-110">Pour obtenir une référence à la cellule BlockSizeY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="8eb0c-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8eb0c-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="8eb0c-111">Section index:</span></span>  <br/> |<span data-ttu-id="8eb0c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8eb0c-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8eb0c-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="8eb0c-113">Row index:</span></span>  <br/> |<span data-ttu-id="8eb0c-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8eb0c-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="8eb0c-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="8eb0c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8eb0c-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="8eb0c-116">**visPLOBlockSizeY**</span></span> <br/> |
   

