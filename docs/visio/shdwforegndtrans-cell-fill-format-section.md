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
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435039"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="87ac0-103">ShdwForegndTrans, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="87ac0-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="87ac0-104">Détermine le niveau de transparence de la couleur utilisée pour le premier plan (trait) du motif de remplissage de l'ombre de la forme.</span><span class="sxs-lookup"><span data-stu-id="87ac0-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="87ac0-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="87ac0-105">**Value**</span></span>|<span data-ttu-id="87ac0-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="87ac0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="87ac0-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="87ac0-107">0 - 100</span></span>  <br/> |<span data-ttu-id="87ac0-p101">Représente le pourcentage de transparence. La valeur par défaut est 0 % (entièrement opaque).</span><span class="sxs-lookup"><span data-stu-id="87ac0-p101">Represents the percentage of transparency. The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87ac0-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="87ac0-110">Remarks</span></span>

<span data-ttu-id="87ac0-111">Les valeurs sont arrondies au demi-point le plus proche.</span><span class="sxs-lookup"><span data-stu-id="87ac0-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="87ac0-112">Une valeur de 100 % est complètement transparente.</span><span class="sxs-lookup"><span data-stu-id="87ac0-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="87ac0-113">Bien qu’une ombre dont le remplissage est entièrement transparent soit identique sur la page de dessin à une ombre sans remplissage, elle interagit avec les autres objets de la page de la même manière que si elle avait une transparence de 0 %.</span><span class="sxs-lookup"><span data-stu-id="87ac0-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="87ac0-p103">Vous pouvez également définir cette valeur à l’aide du curseur dans la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options d’ombre**). Cette valeur contrôle à la fois les transparences de l’ombre de l’arrière-plan et du premier plan. Pour les définir de façon indépendante, vous devez les entrer dans la fenêtre Feuille ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="87ac0-p103">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**). This value controls the value of both the background and foreground shadow transparencies. To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="87ac0-117">Pour obtenir une référence à la cellule ShdwForegndTrans par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="87ac0-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87ac0-118">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="87ac0-118">Cell name:</span></span>  <br/> |<span data-ttu-id="87ac0-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="87ac0-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="87ac0-120">Pour obtenir une référence à la cellule ShdwForegndTrans par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="87ac0-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87ac0-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="87ac0-121">Section index:</span></span>  <br/> |<span data-ttu-id="87ac0-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="87ac0-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="87ac0-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="87ac0-123">Row index:</span></span>  <br/> |<span data-ttu-id="87ac0-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="87ac0-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="87ac0-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="87ac0-125">Cell index:</span></span>  <br/> |<span data-ttu-id="87ac0-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="87ac0-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

