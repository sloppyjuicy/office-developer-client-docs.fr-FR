---
title: LineJumpFactorY, cellule (section Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Détermine la taille des déviations sur les connecteurs dynamiques verticaux de la page par rapport à la valeur de la cellule LineToLineY. La valeur de cette cellule est comprise entre 0 et 10 mais des valeurs fractionnelles de 0 à 1 sont proposées.
ms.openlocfilehash: deba4c27585644604e7bac1dbfe284bc3977835e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788967"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="64151-104">LineJumpFactorY, cellule (section Page Layout)</span><span class="sxs-lookup"><span data-stu-id="64151-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="64151-p102">Détermine la taille des déviations sur les connecteurs dynamiques verticaux de la page par rapport à la valeur de la cellule LineToLineY. La valeur de cette cellule est comprise entre 0 et 10 mais des valeurs fractionnelles de 0 à 1 sont proposées.</span><span class="sxs-lookup"><span data-stu-id="64151-p102">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64151-107">Note</span><span class="sxs-lookup"><span data-stu-id="64151-107">Remarks</span></span>

<span data-ttu-id="64151-108">Vous pouvez également définir la valeur de cette cellule sous l’onglet **disposition et positionnement** dans la boîte de dialogue **Mise en Page** (sous l’onglet **Création** , cliquez sur la flèche **Mise en Page** , puis cliquez sur **disposition et positionnement**).</span><span class="sxs-lookup"><span data-stu-id="64151-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="64151-109">Pour obtenir une référence à la cellule LineJumpFactorY par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="64151-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64151-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="64151-110">Cell name:</span></span>  <br/> |<span data-ttu-id="64151-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="64151-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="64151-112">Pour obtenir une référence à la cellule LineJumpFactorY par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="64151-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64151-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="64151-113">Section index:</span></span>  <br/> |<span data-ttu-id="64151-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="64151-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="64151-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="64151-115">Row index:</span></span>  <br/> |<span data-ttu-id="64151-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="64151-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="64151-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="64151-117">Cell index:</span></span>  <br/> |<span data-ttu-id="64151-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="64151-118">**visPLOJumpFactorY**</span></span> <br/> |
   

