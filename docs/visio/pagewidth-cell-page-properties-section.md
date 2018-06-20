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
ms.openlocfilehash: e03696c8f1c921c930d3563e9c73ef4ae613a7c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789225"
---
# <a name="pagewidth-cell-page-properties-section"></a><span data-ttu-id="c5f61-103">PageWidth, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="c5f61-103">PageWidth Cell (Page Properties Section)</span></span>

<span data-ttu-id="c5f61-104">Détermine la largeur de la page imprimée en unités de dessin.</span><span class="sxs-lookup"><span data-stu-id="c5f61-104">Determines the width of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5f61-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="c5f61-105">Remarks</span></span>

<span data-ttu-id="c5f61-106">Vous pouvez également définir la largeur de la page sous l’onglet **Taille de la Page** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ) ou redimensionnez manuellement la page avec la souris.</span><span class="sxs-lookup"><span data-stu-id="c5f61-106">You can also set the page width on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) or by manually resizing the page with the mouse.</span></span> <span data-ttu-id="c5f61-107">Pour ce faire, faites glisser la bordure de la page tout en maintenant la touche CTRL enfoncée.</span><span class="sxs-lookup"><span data-stu-id="c5f61-107">To do this, drag the edge of the page while holding down the CTRL key.</span></span> 
  
<span data-ttu-id="c5f61-108">Pour obtenir une référence à la cellule PageWidth par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c5f61-108">To get a reference to the PageWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5f61-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c5f61-109">Cell name:</span></span>  <br/> |<span data-ttu-id="c5f61-110">PageWidth</span><span class="sxs-lookup"><span data-stu-id="c5f61-110">PageWidth</span></span>  <br/> |
   
<span data-ttu-id="c5f61-111">Pour obtenir une référence à la cellule PageWidth par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c5f61-111">To get a reference to the PageWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c5f61-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c5f61-112">Section index:</span></span>  <br/> |<span data-ttu-id="c5f61-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c5f61-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c5f61-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c5f61-114">Row index:</span></span>  <br/> |<span data-ttu-id="c5f61-115">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="c5f61-115">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="c5f61-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c5f61-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c5f61-117">**visPageWidth**</span><span class="sxs-lookup"><span data-stu-id="c5f61-117">**visPageWidth**</span></span> <br/> |
   

