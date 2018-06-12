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
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789509"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="70be6-105">Rounding, cellule (section Line Format)</span><span class="sxs-lookup"><span data-stu-id="70be6-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="70be6-p102">Indique le rayon de l'arrondi qui est appliqué lorsque deux segments contigus d'un chemin se rejoignent. Par exemple, l'arrondi permet d'attribuer des angles arrondis à un rectangle. Pour le définir, entrez une valeur associée à des unités de mesure (une paire nombre-unité).</span><span class="sxs-lookup"><span data-stu-id="70be6-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="70be6-109">Note</span><span class="sxs-lookup"><span data-stu-id="70be6-109">Remarks</span></span>

<span data-ttu-id="70be6-110">Vous pouvez également définir cette valeur dans la boîte de dialogue **trait** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **trait**, pointez sur **poids**, puis cliquez sur **Autres traits**).</span><span class="sxs-lookup"><span data-stu-id="70be6-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="70be6-111">Pour obtenir une référence à la cellule Rounding par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="70be6-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70be6-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="70be6-112">Cell name:</span></span>  <br/> |<span data-ttu-id="70be6-113">Rounding</span><span class="sxs-lookup"><span data-stu-id="70be6-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="70be6-114">Pour obtenir une référence à la cellule Rounding par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="70be6-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70be6-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="70be6-115">Section index:</span></span>  <br/> |<span data-ttu-id="70be6-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="70be6-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="70be6-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="70be6-117">Row index:</span></span>  <br/> |<span data-ttu-id="70be6-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="70be6-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="70be6-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="70be6-119">Cell index:</span></span>  <br/> |<span data-ttu-id="70be6-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="70be6-120">**visLineRounding**</span></span> <br/> |
   

