---
title: Rounding, cellule (section Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358582"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="c3c54-105">Rounding, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="c3c54-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="c3c54-p102">Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).</span><span class="sxs-lookup"><span data-stu-id="c3c54-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3c54-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="c3c54-109">Remarks</span></span>

<span data-ttu-id="c3c54-110">Vous pouvez également définir cette valeur dans la boîte de dialogue **trait** (sous l'onglet **Accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **autres traits**).</span><span class="sxs-lookup"><span data-stu-id="c3c54-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="c3c54-111">Pour obtenir une référence à la cellule Rounding par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="c3c54-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3c54-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c3c54-112">Cell name:</span></span>  <br/> |<span data-ttu-id="c3c54-113">Arrondi</span><span class="sxs-lookup"><span data-stu-id="c3c54-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="c3c54-114">Pour obtenir une référence à la cellule Rounding à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c3c54-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c3c54-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c3c54-115">Section index:</span></span>  <br/> |<span data-ttu-id="c3c54-116">**Définis**</span><span class="sxs-lookup"><span data-stu-id="c3c54-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c3c54-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c3c54-117">Row index:</span></span>  <br/> |<span data-ttu-id="c3c54-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="c3c54-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="c3c54-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c3c54-119">Cell index:</span></span>  <br/> |<span data-ttu-id="c3c54-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="c3c54-120">**visLineRounding**</span></span> <br/> |
   

