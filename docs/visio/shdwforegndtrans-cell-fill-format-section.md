---
title: ShdwForegndTrans, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.
ms.openlocfilehash: 5fd385fc2f46f1ff8eedc961833813ec16ba7b73
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789694"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="1c013-103">ShdwForegndTrans, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="1c013-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="1c013-104">Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.</span><span class="sxs-lookup"><span data-stu-id="1c013-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="1c013-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="1c013-105">**Value**</span></span>|<span data-ttu-id="1c013-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="1c013-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1c013-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="1c013-107">0 - 100</span></span>  <br/> |<span data-ttu-id="1c013-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="1c013-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c013-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="1c013-110">Remarks</span></span>

<span data-ttu-id="1c013-111">Les valeurs sont arrondies au pourcentage le plus proche.</span><span class="sxs-lookup"><span data-stu-id="1c013-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="1c013-112">Une valeur de 100 % est complètement transparente.</span><span class="sxs-lookup"><span data-stu-id="1c013-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="1c013-113">Même si une ombre qui possède un remplissage transparent identiques sur la page de dessin apparaît une ombre qui n’est pas remplie, il interagit avec d’autres objets dans la page de la même façon que si sa transparence ont été 0 %.</span><span class="sxs-lookup"><span data-stu-id="1c013-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="1c013-114">Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **ombre** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="1c013-114">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span> <span data-ttu-id="1c013-115">Cette valeur contrôle la valeur de l’arrière-plan et premier plan transparents ombre.</span><span class="sxs-lookup"><span data-stu-id="1c013-115">This value controls the value of both the background and foreground shadow transparencies.</span></span> <span data-ttu-id="1c013-116">Pour définir ces valeurs de façon indépendante, vous devez les entrer dans la fenêtre feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="1c013-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="1c013-117">Pour obtenir une référence à la cellule ShdwForegndTrans par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="1c013-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c013-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c013-118">Cell name:</span></span>  <br/> |<span data-ttu-id="1c013-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="1c013-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="1c013-120">Pour obtenir une référence à la cellule ShdwForegndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1c013-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1c013-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1c013-121">Section index:</span></span>  <br/> |<span data-ttu-id="1c013-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1c013-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1c013-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1c013-123">Row index:</span></span>  <br/> |<span data-ttu-id="1c013-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="1c013-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="1c013-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1c013-125">Cell index:</span></span>  <br/> |<span data-ttu-id="1c013-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="1c013-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

