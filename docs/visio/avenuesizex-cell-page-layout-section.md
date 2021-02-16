---
title: AvenueSizeX, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm65
localization_priority: Normal
ms.assetid: 86fe25ed-590d-b2f0-5dfe-9746a19c6b04
description: Détermine la quantité d’espace horizontal entre les formes de la page de dessin lorsque vous les avez mises en page à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Re-Layout Page, puis sur Autres options de disposition).
ms.openlocfilehash: 28eea2589e34c7793e89e01495eb519b987553a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411644"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="5c5fc-103">AvenueSizeX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="5c5fc-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="5c5fc-104">Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque  vous les  avez mises en page à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe Disposition, cliquez sur Nouvelle disposition **de page,** puis cliquez sur \*\* Autres options de disposition \*\*). </span><span class="sxs-lookup"><span data-stu-id="5c5fc-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click \*\* More Layout Options \*\*).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5c5fc-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c5fc-105">Remarks</span></span>

<span data-ttu-id="5c5fc-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **Espacement : disposition et positionnement** (sous l’onglet **Création**, cliquez sur la flèche dans le groupe **Mise en page**, cliquez sur **Disposition et positionnement**, puis sur **Espacement**).</span><span class="sxs-lookup"><span data-stu-id="5c5fc-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="5c5fc-p101">La grille dynamique utilise le paramètre dans la cellule AvenueSizeX uniquement lorsqu’une forme est disponible pour calculer l’espacement horizontal. Pour utiliser la grille dynamique, dans le groupe **Aides visuelles** de l’onglet **Affichage**, activez la case à cocher **Grille dynamique**.</span><span class="sxs-lookup"><span data-stu-id="5c5fc-p101">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing. To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="5c5fc-109">Pour obtenir une référence à la cellule AvenueSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="5c5fc-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c5fc-110">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="5c5fc-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5c5fc-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="5c5fc-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="5c5fc-112">Pour obtenir une référence à la cellule AvenueSizeX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c5fc-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5c5fc-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5c5fc-113">Section index:</span></span>  <br/> |<span data-ttu-id="5c5fc-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c5fc-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5c5fc-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5c5fc-115">Row index:</span></span>  <br/> |<span data-ttu-id="5c5fc-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="5c5fc-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="5c5fc-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5c5fc-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5c5fc-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="5c5fc-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

