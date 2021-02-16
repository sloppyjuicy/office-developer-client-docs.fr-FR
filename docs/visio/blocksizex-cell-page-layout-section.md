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
description: Détermine la taille horizontale du bloc, la zone dans laquelle chacune de vos formes doit tenir sur la page de dessin lorsque vous les avez mises en page à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Re-Layout Page, puis sur Autres options de disposition).
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424188"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="763d0-103">BlockSizeX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="763d0-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="763d0-104">Détermine la taille horizontale du bloc, la zone dans laquelle chacune de vos formes doit tenir sur la  page de dessin  lorsque vous les avez mises en page à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition de **page,** puis cliquez sur Autres  **options** de disposition).</span><span class="sxs-lookup"><span data-stu-id="763d0-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="763d0-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="763d0-105">Remarks</span></span>

<span data-ttu-id="763d0-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **Espacement : disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="763d0-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="763d0-107">Pour obtenir une référence à la cellule BlockSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="763d0-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="763d0-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="763d0-108">Cell name:</span></span>  <br/> |<span data-ttu-id="763d0-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="763d0-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="763d0-110">Pour obtenir une référence à la cellule BlockSizeX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="763d0-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="763d0-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="763d0-111">Section index:</span></span>  <br/> |<span data-ttu-id="763d0-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="763d0-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="763d0-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="763d0-113">Row index:</span></span>  <br/> |<span data-ttu-id="763d0-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="763d0-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="763d0-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="763d0-115">Cell index:</span></span>  <br/> |<span data-ttu-id="763d0-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="763d0-116">**visPLOBlockSizeX**</span></span> <br/> |
   

