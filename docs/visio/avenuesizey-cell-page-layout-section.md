---
title: AvenueSizeY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Détermine la distance verticale entre les formes sur la page de dessin lorsque vous les disposez à l'aide de la boîte de dialogue Configurer la disposition (sous l'onglet création, dans le groupe disposition, cliquez sur nouvelle disposition de page, puis cliquez sur autres options de disposition).
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420205"
---
# <a name="avenuesizey-cell-page-layout-section"></a><span data-ttu-id="073ce-103">AvenueSizeY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="073ce-103">AvenueSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="073ce-104">Détermine la quantité d'espace verticale entre les formes sur la page de dessin lorsque vous les disposez à l'aide de la boîte de dialogue **configurer la disposition** (sous l'onglet **création** , dans le groupe **disposition** , cliquez sur **nouvelle disposition** de page, puis cliquez sur **plus Options de disposition**).</span><span class="sxs-lookup"><span data-stu-id="073ce-104">Determines the amount of vertical space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="073ce-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="073ce-105">Remarks</span></span>

<span data-ttu-id="073ce-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **Espacement : disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="073ce-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="073ce-p101">La grille dynamique utilise le paramètre dans la cellule AvenueSizeY uniquement lorsqu’une forme est disponible pour calculer l’espacement vertical. Pour utiliser la grille dynamique, dans le groupe **Aides visuelles** de l’onglet **Affichage**, activez la case à cocher **Grille dynamique**.</span><span class="sxs-lookup"><span data-stu-id="073ce-p101">The dynamic grid uses the setting in the AvenueSizeY cell when only one shape is available for calculating vertical spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="073ce-109">Pour obtenir une référence à la cellule AvenueSizeY par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="073ce-109">To get a reference to the AvenueSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="073ce-110">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="073ce-110">Cell name:</span></span>  <br/> | <span data-ttu-id="073ce-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="073ce-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="073ce-112">Pour obtenir une référence à la cellule AvenueSizeY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="073ce-112">To get a reference to the AvenueSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="073ce-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="073ce-113">Section index:</span></span>  <br/> |<span data-ttu-id="073ce-114">**Définis**</span><span class="sxs-lookup"><span data-stu-id="073ce-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="073ce-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="073ce-115">Row index:</span></span>  <br/> |<span data-ttu-id="073ce-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="073ce-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="073ce-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="073ce-117">Cell index:</span></span>  <br/> |<span data-ttu-id="073ce-118">**visPLOAvenueSizeY**</span><span class="sxs-lookup"><span data-stu-id="073ce-118">**visPLOAvenueSizeY**</span></span> <br/> |
   

