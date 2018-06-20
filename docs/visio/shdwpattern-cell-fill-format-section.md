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
ms.openlocfilehash: fd24a8d23d62436a6d81cf6b8049dcabe47db677
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789701"
---
# <a name="shdwpattern-cell-fill-format-section"></a><span data-ttu-id="5c36f-103">ShdwPattern, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="5c36f-103">ShdwPattern Cell (Fill Format Section)</span></span>

<span data-ttu-id="5c36f-104">Détermine le motif de remplissage de l'ombre d'une forme.</span><span class="sxs-lookup"><span data-stu-id="5c36f-104">Determines the fill pattern for a shape's shadow.</span></span>
  
|<span data-ttu-id="5c36f-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5c36f-105">**Value**</span></span>|<span data-ttu-id="5c36f-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="5c36f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5c36f-107">0</span><span class="sxs-lookup"><span data-stu-id="5c36f-107">0</span></span>  <br/> |<span data-ttu-id="5c36f-108">Aucun (remplissage transparent).</span><span class="sxs-lookup"><span data-stu-id="5c36f-108">None (transparent fill)</span></span>  <br/> |
|<span data-ttu-id="5c36f-109">1</span><span class="sxs-lookup"><span data-stu-id="5c36f-109">1</span></span>  <br/> |<span data-ttu-id="5c36f-110">Couleur de premier plan unie</span><span class="sxs-lookup"><span data-stu-id="5c36f-110">Solid foreground color</span></span>  <br/> |
|<span data-ttu-id="5c36f-111">2 - 40</span><span class="sxs-lookup"><span data-stu-id="5c36f-111">2 - 40</span></span>  <br/> |<span data-ttu-id="5c36f-112">Motifs assortis</span><span class="sxs-lookup"><span data-stu-id="5c36f-112">Assorted patterns</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5c36f-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="5c36f-113">Remarks</span></span>

<span data-ttu-id="5c36f-114">Pour définir le motif de remplissage, entrez un numéro à partir de 0 à 40, qui est un index dans une collection de modèles.</span><span class="sxs-lookup"><span data-stu-id="5c36f-114">To set the fill pattern, enter a number from 0 to 40, which is an index into a collection of patterns.</span></span> <span data-ttu-id="5c36f-115">Vous pouvez afficher l’ensemble des motifs de remplissage dans la boîte de dialogue **remplissage** (sous l’onglet **accueil** , dans le groupe **forme** , cliquez sur **remplissage**, puis cliquez sur **Options de remplissage**).</span><span class="sxs-lookup"><span data-stu-id="5c36f-115">You can view the fill pattern collection in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span>
  
<span data-ttu-id="5c36f-116">Pour obtenir une référence à la cellule ShdwPattern par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="5c36f-116">To get a reference to the ShdwPattern cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c36f-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5c36f-117">Cell name:</span></span>  <br/> |<span data-ttu-id="5c36f-118">ShdwPattern</span><span class="sxs-lookup"><span data-stu-id="5c36f-118">ShdwPattern</span></span>  <br/> |
   
<span data-ttu-id="5c36f-119">Pour obtenir une référence à la cellule ShdwPattern par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5c36f-119">To get a reference to the ShdwPattern cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5c36f-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5c36f-120">Section index:</span></span>  <br/> |<span data-ttu-id="5c36f-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5c36f-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5c36f-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5c36f-122">Row index:</span></span>  <br/> |<span data-ttu-id="5c36f-123">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="5c36f-123">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="5c36f-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5c36f-124">Cell index:</span></span>  <br/> |<span data-ttu-id="5c36f-125">**visFillShdwPattern**</span><span class="sxs-lookup"><span data-stu-id="5c36f-125">**visFillShdwPattern**</span></span> <br/> |
   

