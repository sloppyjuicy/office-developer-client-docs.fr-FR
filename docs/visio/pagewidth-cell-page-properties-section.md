---
title: PageWidth, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251372
localization_priority: Normal
ms.assetid: b98c5bf3-10c8-7299-2836-3906d6a9135d
description: Détermine la largeur de la page imprimée en unités de dessin.
ms.openlocfilehash: 6d887cb4335d2725101db54ba2b1483ccf01cff4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327369"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="96e75-103">PageWidth, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="96e75-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="96e75-104">Détermine la largeur de la page imprimée en unités de dessin.</span><span class="sxs-lookup"><span data-stu-id="96e75-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96e75-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="96e75-105">Remarks</span></span>

<span data-ttu-id="96e75-106">Vous pouvez également définir la largeur de la page sous l'onglet taille de la **page** de la boîte de dialogue **mise en page** (sous l'onglet **création** , cliquez sur la flèche mise en **page** ) ou en redimensionnant manuellement la page à l'aide de la souris.</span><span class="sxs-lookup"><span data-stu-id="96e75-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="96e75-107">Pour ce faire, faites glisser le bord de la page en maintenant la touche Ctrl enfoncée.</span><span class="sxs-lookup"><span data-stu-id="96e75-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="96e75-108">Pour obtenir une référence à la cellule PageWidth par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="96e75-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96e75-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="96e75-109">Cell name:</span></span>  <br/> |<span data-ttu-id="96e75-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="96e75-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="96e75-111">Pour obtenir une référence à la cellule PageWidth à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="96e75-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="96e75-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="96e75-112">Section index:</span></span>  <br/> |<span data-ttu-id="96e75-113">**Définis**</span><span class="sxs-lookup"><span data-stu-id="96e75-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="96e75-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="96e75-114">Row index:</span></span>  <br/> |<span data-ttu-id="96e75-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="96e75-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="96e75-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="96e75-116">Cell index:</span></span>  <br/> |<span data-ttu-id="96e75-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="96e75-117">**visPageWidth**</span></span> <br/> |
   

