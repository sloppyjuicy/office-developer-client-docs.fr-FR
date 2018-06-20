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
ms.openlocfilehash: e198e90e9c70aad1e41ee02d5dcefea68846486c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789201"
---
# <a name="pageheight-cell-page-properties-section"></a><span data-ttu-id="53d49-103">PageHeight, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="53d49-103">PageHeight Cell (Page Properties Section)</span></span>

<span data-ttu-id="53d49-104">Contient la hauteur de la page imprimée en unités de dessin.</span><span class="sxs-lookup"><span data-stu-id="53d49-104">Contains the height of the printed page in drawing units.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="53d49-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="53d49-105">Remarks</span></span>

<span data-ttu-id="53d49-106">Vous pouvez également définir la hauteur de page sous l’onglet **Taille de la Page** de la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ), ou redimensionnez manuellement la page avec la souris.</span><span class="sxs-lookup"><span data-stu-id="53d49-106">You can also set the page height on the **Page Size** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow), or by manually resizing the page with the mouse.</span></span> 
  
<span data-ttu-id="53d49-107">Pour obtenir une référence à la cellule PageHeight par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="53d49-107">To get a reference to the PageHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53d49-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="53d49-108">Cell name:</span></span>  <br/> |<span data-ttu-id="53d49-109">PageHeight</span><span class="sxs-lookup"><span data-stu-id="53d49-109">PageHeight</span></span>  <br/> |
   
<span data-ttu-id="53d49-110">Pour obtenir une référence à la cellule PageHeight par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="53d49-110">To get a reference to the PageHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="53d49-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="53d49-111">Section index:</span></span>  <br/> |<span data-ttu-id="53d49-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="53d49-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="53d49-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="53d49-113">Row index:</span></span>  <br/> |<span data-ttu-id="53d49-114">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="53d49-114">**visRowPage**</span></span> <br/> |
|<span data-ttu-id="53d49-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="53d49-115">Cell index:</span></span>  <br/> |<span data-ttu-id="53d49-116">**visPageHeight**</span><span class="sxs-lookup"><span data-stu-id="53d49-116">**visPageHeight**</span></span> <br/> |
   

