---
title: Transparency, cellule (section Image Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Définit le niveau de transparence de la couleur d'un calque.
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789922"
---
# <a name="transparency-cell-image-properties-section"></a><span data-ttu-id="0be28-103">Transparency, cellule (section Image Properties)</span><span class="sxs-lookup"><span data-stu-id="0be28-103">Transparency Cell (Image Properties Section)</span></span>

<span data-ttu-id="0be28-104">Définit le niveau de transparence de la couleur d'un calque.</span><span class="sxs-lookup"><span data-stu-id="0be28-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="0be28-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0be28-105">**Value**</span></span>|<span data-ttu-id="0be28-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="0be28-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0be28-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="0be28-107">0 - 100</span></span>  <br/> |<span data-ttu-id="0be28-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="0be28-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0be28-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="0be28-110">Remarks</span></span>

<span data-ttu-id="0be28-111">Les valeurs sont arrondies au pourcentage le plus proche.</span><span class="sxs-lookup"><span data-stu-id="0be28-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="0be28-112">Une valeur de 100 % est complètement transparente.</span><span class="sxs-lookup"><span data-stu-id="0be28-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="0be28-113">Bien qu’un calque dont la couleur transparente complètement la même page de dessin s’affiche en tant que couche qui n’a aucune couleur, il interagit avec d’autres objets dans la page de la même manière que si sa transparence ont été 0 %.</span><span class="sxs-lookup"><span data-stu-id="0be28-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="0be28-114">Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Propriétés des calques** (sous l’onglet **accueil** , dans le groupe **modification** , cliquez sur **calques**, puis cliquez sur **Propriétés des calques**).</span><span class="sxs-lookup"><span data-stu-id="0be28-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="0be28-115">Pour obtenir une référence à la cellule Transparency par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="0be28-115">To get a reference to the Transparency cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0be28-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0be28-116">Cell name:</span></span>  <br/> |<span data-ttu-id="0be28-117">Transparency</span><span class="sxs-lookup"><span data-stu-id="0be28-117">Transparency</span></span>  <br/> |
   
<span data-ttu-id="0be28-118">Pour obtenir une référence à la cellule Transparency par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="0be28-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0be28-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="0be28-119">Section index:</span></span>  <br/> |<span data-ttu-id="0be28-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0be28-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0be28-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="0be28-121">Row index:</span></span>  <br/> |<span data-ttu-id="0be28-122">**visRowImage**</span><span class="sxs-lookup"><span data-stu-id="0be28-122">**visRowImage**</span></span> <br/> |
|<span data-ttu-id="0be28-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="0be28-123">Cell index:</span></span>  <br/> |<span data-ttu-id="0be28-124">**visImageTransparency**</span><span class="sxs-lookup"><span data-stu-id="0be28-124">**visImageTransparency**</span></span> <br/> |
   

