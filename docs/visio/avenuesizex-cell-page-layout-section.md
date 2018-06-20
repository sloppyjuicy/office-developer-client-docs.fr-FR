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
description: Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue Configurer la disposition (sous l’onglet Création, dans le groupe mise en page, cliquez sur Re-mise en Page, puis cliquez sur autres Options de mise en page).
ms.openlocfilehash: efb29181414957063e038b97c2d7b79720aa0405
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788052"
---
# <a name="avenuesizex-cell-page-layout-section"></a><span data-ttu-id="373fd-103">AvenueSizeX, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="373fd-103">AvenueSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="373fd-104">Détermine la quantité d’espace horizontal entre les formes sur la page de dessin lorsque vous les disposez à l’aide de la boîte de dialogue **Configurer la disposition** (sous l’onglet **Création** , dans le groupe **mise en page** , cliquez sur **Re-mise en Page**, puis cliquez sur ** plus Options de disposition **).</span><span class="sxs-lookup"><span data-stu-id="373fd-104">Determines the amount of horizontal space between shapes on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click ** More Layout Options **).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="373fd-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="373fd-105">Remarks</span></span>

<span data-ttu-id="373fd-106">Vous pouvez également définir cette valeur dans la boîte de dialogue **disposition et positionnement** (sous l’onglet **Création** , cliquez sur la flèche dans le groupe **Mise en Page** , cliquez sur l’onglet **disposition et positionnement** , puis cliquez sur **espacement**).</span><span class="sxs-lookup"><span data-stu-id="373fd-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="373fd-107">La grille dynamique utilise le paramètre dans la cellule AvenueSizeX lorsque qu’une seule forme est disponible pour calculer l’espacement horizontal.</span><span class="sxs-lookup"><span data-stu-id="373fd-107">The dynamic grid uses the setting in the AvenueSizeX cell when only one shape is available for calculating horizontal spacing.</span></span> <span data-ttu-id="373fd-108">Pour utiliser la grille dynamique, sous l’onglet **affichage** , dans le groupe **aides visuelles** , sélectionnez **Grille dynamique**.</span><span class="sxs-lookup"><span data-stu-id="373fd-108">To use the dynamic grid, on the **View** tab, in the **Visual Aids** group, select **Dynamic Grid**.</span></span>
  
<span data-ttu-id="373fd-109">Pour obtenir une référence à la cellule AvenueSizeX par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="373fd-109">To get a reference to the AvenueSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="373fd-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="373fd-110">Cell name:</span></span>  <br/> | <span data-ttu-id="373fd-111">AvenueSizeY</span><span class="sxs-lookup"><span data-stu-id="373fd-111">AvenueSizeY</span></span>  <br/> |
   
<span data-ttu-id="373fd-112">Pour obtenir une référence à la cellule AvenueSizeX par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="373fd-112">To get a reference to the AvenueSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="373fd-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="373fd-113">Section index:</span></span>  <br/> |<span data-ttu-id="373fd-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="373fd-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="373fd-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="373fd-115">Row index:</span></span>  <br/> |<span data-ttu-id="373fd-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="373fd-116">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="373fd-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="373fd-117">Cell index:</span></span>  <br/> |<span data-ttu-id="373fd-118">**visPLOAvenueSizeX**</span><span class="sxs-lookup"><span data-stu-id="373fd-118">**visPLOAvenueSizeX**</span></span> <br/> |
   

