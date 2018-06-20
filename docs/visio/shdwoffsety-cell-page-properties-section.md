---
title: ShdwOffsetY, cellule (section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Détermine, en unités de page, la distance du décalage vertical entre l'ombre d'une forme et la forme.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789719"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="5bc24-103">ShdwOffsetY, cellule (section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="5bc24-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="5bc24-104">Détermine, en unités de page, la distance du décalage vertical entre l'ombre d'une forme et la forme.</span><span class="sxs-lookup"><span data-stu-id="5bc24-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5bc24-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="5bc24-105">Remarks</span></span>

<span data-ttu-id="5bc24-106">Cette valeur est définie dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** ).</span><span class="sxs-lookup"><span data-stu-id="5bc24-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="5bc24-107">Cette valeur est indépendante de l’échelle du dessin.</span><span class="sxs-lookup"><span data-stu-id="5bc24-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="5bc24-108">Si le dessin est mis à l’échelle, le décalage d’ombre reste identique.</span><span class="sxs-lookup"><span data-stu-id="5bc24-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="5bc24-109">Pour obtenir une référence à la cellule ShdwOffsetY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="5bc24-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bc24-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5bc24-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5bc24-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="5bc24-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="5bc24-112">Pour obtenir une référence à la cellule ShdwOffsetY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5bc24-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5bc24-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5bc24-113">Section index:</span></span>  <br/> |<span data-ttu-id="5bc24-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5bc24-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5bc24-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5bc24-115">Row index:</span></span>  <br/> |<span data-ttu-id="5bc24-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5bc24-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="5bc24-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5bc24-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5bc24-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="5bc24-118">**visPageShdwOffsetY**</span></span> <br/> |
   

