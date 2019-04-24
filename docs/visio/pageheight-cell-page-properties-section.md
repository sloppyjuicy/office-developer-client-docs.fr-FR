---
title: PageHeight, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm760
localization_priority: Normal
ms.assetid: 0184814c-2d67-6ad4-e336-5694612e518d
description: Contient la hauteur de la page imprimée en unités de dessin.
ms.openlocfilehash: ac24bee517f29da333a445f276447c1aa682f01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334348"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="ee1a1-103">PageHeight, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="ee1a1-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="ee1a1-104">Contient la hauteur de la page imprimée en unités de dessin.</span><span class="sxs-lookup"><span data-stu-id="ee1a1-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ee1a1-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee1a1-105">Remarks</span></span>

<span data-ttu-id="ee1a1-106">Vous pouvez également définir la hauteur de la page sous l’onglet **Taille de la page** de la boîte de dialogue **Mise en page** (sous l’onglet **Création**, cliquez sur la flèche **Mise en page**) ou en redimensionnant manuellement la page avec la souris.</span><span class="sxs-lookup"><span data-stu-id="ee1a1-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="ee1a1-107">Pour obtenir une référence à la cellule PageHeight par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="ee1a1-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee1a1-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ee1a1-108">Cell name:</span></span>  <br/> |<span data-ttu-id="ee1a1-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="ee1a1-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="ee1a1-110">Pour obtenir une référence à la cellule PageHeight à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="ee1a1-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ee1a1-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="ee1a1-111">Section index:</span></span>  <br/> |<span data-ttu-id="ee1a1-112">**Définis**</span><span class="sxs-lookup"><span data-stu-id="ee1a1-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ee1a1-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="ee1a1-113">Row index:</span></span>  <br/> |<span data-ttu-id="ee1a1-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="ee1a1-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="ee1a1-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="ee1a1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ee1a1-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="ee1a1-116">**visPageHeight**</span></span> <br/> |
   

