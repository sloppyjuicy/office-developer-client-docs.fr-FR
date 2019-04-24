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
description: Détermine la taille du bloc vertical, la zone dans laquelle vos formes doivent entrer sur la page de dessin lorsque vous les disposez à l'aide de la boîte de dialogue Configurer la disposition (sous l'onglet création, dans le groupe disposition, cliquez sur nouvelle disposition de page, puis cliquez sur autres options de disposition).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297346"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="466cc-103">BlockSizeY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="466cc-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="466cc-104">Détermine la taille du bloc vertical, la zone dans laquelle vos formes doivent entrer sur la page de dessin lorsque vous les disposez à l'aide de la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition de page**, puis cliquez sur **autres options de disposition**.</span><span class="sxs-lookup"><span data-stu-id="466cc-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="466cc-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="466cc-105">Remarks</span></span>

<span data-ttu-id="466cc-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **Espacement : disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="466cc-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="466cc-107">Pour obtenir une référence à la cellule BlockSizeY par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="466cc-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="466cc-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="466cc-108">Cell name:</span></span>  <br/> | <span data-ttu-id="466cc-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="466cc-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="466cc-110">Pour obtenir une référence à la cellule BlockSizeY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="466cc-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="466cc-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="466cc-111">Section index:</span></span>  <br/> |<span data-ttu-id="466cc-112">**Définis**</span><span class="sxs-lookup"><span data-stu-id="466cc-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="466cc-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="466cc-113">Row index:</span></span>  <br/> |<span data-ttu-id="466cc-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="466cc-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="466cc-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="466cc-115">Cell index:</span></span>  <br/> |<span data-ttu-id="466cc-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="466cc-116">**visPLOBlockSizeY**</span></span> <br/> |
   

