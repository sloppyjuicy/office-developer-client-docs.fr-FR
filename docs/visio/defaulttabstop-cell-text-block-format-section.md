---
title: DefaultTabstop, cellule (section Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm220
localization_priority: Normal
ms.assetid: 3b3e458a-206c-8699-8bf7-da80f4350706
description: Détermine l’intervalle des taquets de tabulation par défaut dans un bloc de texte.
ms.openlocfilehash: 2b9c2c5b03da98b30e338a250b56091479067955
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788460"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="e9ad1-103">DefaultTabstop, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="e9ad1-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="e9ad1-104">Détermine l’intervalle des taquets de tabulation par défaut dans un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="e9ad1-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e9ad1-105">Note</span><span class="sxs-lookup"><span data-stu-id="e9ad1-105">Remarks</span></span>

<span data-ttu-id="e9ad1-106">La valeur par défaut est de 1,5 cm pour les documents créés en unités métriques et de 0,5 pouce pour ceux créés en unités impériales.</span><span class="sxs-lookup"><span data-stu-id="e9ad1-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="e9ad1-107">Pour obtenir une référence à la cellule DefaultTabstop par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e9ad1-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9ad1-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="e9ad1-108">Cell name:</span></span>  <br/> |<span data-ttu-id="e9ad1-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="e9ad1-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="e9ad1-110">Pour obtenir une référence à la cellule DefaultTabstop par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e9ad1-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e9ad1-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e9ad1-111">Section index:</span></span>  <br/> |<span data-ttu-id="e9ad1-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9ad1-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e9ad1-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e9ad1-113">Row index:</span></span>  <br/> |<span data-ttu-id="e9ad1-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="e9ad1-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="e9ad1-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e9ad1-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e9ad1-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="e9ad1-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

