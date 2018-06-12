---
title: FillPattern, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm375
localization_priority: Normal
ms.assetid: dac82a4f-4508-541a-e118-7d79df987232
description: Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.
ms.openlocfilehash: 26429e06ad432eaf7fae9188ac676cb4be3201c1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788634"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="dd54a-104">FillPattern, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="dd54a-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="dd54a-p102">Détermine le motif de remplissage de la forme. Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.</span><span class="sxs-lookup"><span data-stu-id="dd54a-p102">Determines the fill pattern for the shape. To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="dd54a-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="dd54a-107">**Value**</span></span>|<span data-ttu-id="dd54a-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="dd54a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dd54a-109">0</span><span class="sxs-lookup"><span data-stu-id="dd54a-109">0</span></span>  <br/> |<span data-ttu-id="dd54a-110">Aucun (remplissage transparent).</span><span class="sxs-lookup"><span data-stu-id="dd54a-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="dd54a-111">1</span><span class="sxs-lookup"><span data-stu-id="dd54a-111">1</span></span>  <br/> |<span data-ttu-id="dd54a-112">Couleur d'arrière-plan unie.</span><span class="sxs-lookup"><span data-stu-id="dd54a-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="dd54a-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="dd54a-113">2 - 40</span></span>  <br/> |<span data-ttu-id="dd54a-114">Motifs de remplissage correspondant aux entrées indexées de la boîte de dialogue **remplissage** .</span><span class="sxs-lookup"><span data-stu-id="dd54a-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dd54a-115">Note</span><span class="sxs-lookup"><span data-stu-id="dd54a-115">Remarks</span></span>

<span data-ttu-id="dd54a-116">Vous pouvez également définir cette valeur à l’aide de la boîte de dialogue **remplissage** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **remplissage** , puis sur **Options de remplissage**).</span><span class="sxs-lookup"><span data-stu-id="dd54a-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="dd54a-117">Pour obtenir une référence à la cellule FillPattern par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="dd54a-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd54a-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd54a-118">Cell name:</span></span>  <br/> |<span data-ttu-id="dd54a-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="dd54a-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="dd54a-120">Pour obtenir une référence à la cellule FillPattern par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="dd54a-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dd54a-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="dd54a-121">Section index:</span></span>  <br/> |<span data-ttu-id="dd54a-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dd54a-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dd54a-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="dd54a-123">Row index:</span></span>  <br/> |<span data-ttu-id="dd54a-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="dd54a-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="dd54a-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="dd54a-125">Cell index:</span></span>  <br/> |<span data-ttu-id="dd54a-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="dd54a-126">**visFillPattern**</span></span> <br/> |
   

