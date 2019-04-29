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
ms.openlocfilehash: 340ccdc9f3819fb29e210832107e270bd302433c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422928"
---
# <a name="fillpattern-cell-fill-format-section"></a><span data-ttu-id="7d151-104">FillPattern, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="7d151-104">FillPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="7d151-105">Détermine le motif de remplissage de la forme.</span><span class="sxs-lookup"><span data-stu-id="7d151-105">Determines the fill pattern for the shape.</span></span> <span data-ttu-id="7d151-106">Pour définir un motif de remplissage personnalisé, utilisez la fonction UTILISATION dans cette cellule.</span><span class="sxs-lookup"><span data-stu-id="7d151-106">To specify a custom fill pattern, use the USE function in this cell.</span></span>
  
|<span data-ttu-id="7d151-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7d151-107">**Value**</span></span>|<span data-ttu-id="7d151-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="7d151-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7d151-109">0</span><span class="sxs-lookup"><span data-stu-id="7d151-109">0</span></span>  <br/> |<span data-ttu-id="7d151-110">Aucun (remplissage transparent).</span><span class="sxs-lookup"><span data-stu-id="7d151-110">None (transparent fill).</span></span>  <br/> |
|<span data-ttu-id="7d151-111">0,1</span><span class="sxs-lookup"><span data-stu-id="7d151-111">1</span></span>  <br/> |<span data-ttu-id="7d151-112">Couleur d'arrière-plan unie.</span><span class="sxs-lookup"><span data-stu-id="7d151-112">Solid foreground color.</span></span>  <br/> |
|<span data-ttu-id="7d151-113">2 - 40</span><span class="sxs-lookup"><span data-stu-id="7d151-113">2 - 40</span></span>  <br/> |<span data-ttu-id="7d151-114">Motifs de remplissage correspondant aux entrées indexées de la boîte de dialogue **Remplir**.</span><span class="sxs-lookup"><span data-stu-id="7d151-114">Assorted fill patterns that correspond to indexed entries in the **Fill** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d151-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="7d151-115">Remarks</span></span>

<span data-ttu-id="7d151-116">Vous pouvez également définir cette valeur au moyen de la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**).</span><span class="sxs-lookup"><span data-stu-id="7d151-116">You can also set this value using the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill** and then click **Fill Options**).</span></span>
  
<span data-ttu-id="7d151-117">Pour obtenir une référence à la cellule FillPattern par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="7d151-117">To get a reference to the FillPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d151-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7d151-118">Cell name:</span></span>  <br/> |<span data-ttu-id="7d151-119">FillPattern</span><span class="sxs-lookup"><span data-stu-id="7d151-119">FillPattern</span></span>  <br/> |
   
<span data-ttu-id="7d151-120">Pour obtenir une référence à la cellule FillPattern à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7d151-120">To get a reference to the FillPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7d151-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7d151-121">Section index:</span></span>  <br/> |<span data-ttu-id="7d151-122">**Définis**</span><span class="sxs-lookup"><span data-stu-id="7d151-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="7d151-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7d151-123">Row index:</span></span>  <br/> |<span data-ttu-id="7d151-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="7d151-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="7d151-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7d151-125">Cell index:</span></span>  <br/> |<span data-ttu-id="7d151-126">**visFillPattern**</span><span class="sxs-lookup"><span data-stu-id="7d151-126">**visFillPattern**</span></span> <br/> |
   

