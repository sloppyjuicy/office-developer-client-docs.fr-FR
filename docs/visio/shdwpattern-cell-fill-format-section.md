---
title: ShdwPattern, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm935
localization_priority: Normal
ms.assetid: eca73b80-9835-9011-1dce-187ccee92e76
description: Détermine le motif de remplissage de l'ombre d'une forme.
ms.openlocfilehash: c2591fbc9f208b1bf9c7d0c85e6de765cd9825f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427611"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="05e31-103">ShdwPattern, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="05e31-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="05e31-104">Détermine le motif de remplissage de l'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="05e31-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="05e31-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="05e31-105">**Value**</span></span>|<span data-ttu-id="05e31-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="05e31-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="05e31-107">0</span><span class="sxs-lookup"><span data-stu-id="05e31-107">0</span></span>  <br/> |<span data-ttu-id="05e31-108">Aucun (remplissage transparent).</span><span class="sxs-lookup"><span data-stu-id="05e31-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="05e31-109">1 </span><span class="sxs-lookup"><span data-stu-id="05e31-109">1</span></span>  <br/> |<span data-ttu-id="05e31-110">Couleur de premier plan unie</span><span class="sxs-lookup"><span data-stu-id="05e31-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="05e31-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="05e31-111">2 - 40</span></span>  <br/> |<span data-ttu-id="05e31-112">Motifs assortis</span><span class="sxs-lookup"><span data-stu-id="05e31-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05e31-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="05e31-113">Remarks</span></span>

<span data-ttu-id="05e31-p101">Pour définir le motif de remplissage, entrez une valeur comprise entre 0 et 40, correspondant à un index d’un ensemble de motifs. Vous pouvez afficher cet index dans la boîte de dialogue **Remplissage** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Remplissage**, puis cliquez sur **Options de remplissage**).</span><span class="sxs-lookup"><span data-stu-id="05e31-p101">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns. You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="05e31-116">Pour obtenir une référence à la cellule ShdwPattern par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="05e31-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05e31-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="05e31-117">Cell name:</span></span>  <br/> |<span data-ttu-id="05e31-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="05e31-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="05e31-119">Pour obtenir une référence à la cellule ShdwPattern dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="05e31-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05e31-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="05e31-120">Section index:</span></span>  <br/> |<span data-ttu-id="05e31-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="05e31-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="05e31-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="05e31-122">Row index:</span></span>  <br/> |<span data-ttu-id="05e31-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="05e31-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="05e31-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="05e31-124">Cell index:</span></span>  <br/> |<span data-ttu-id="05e31-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="05e31-125">**visFillShdwPattern**</span></span> <br/> |
   

