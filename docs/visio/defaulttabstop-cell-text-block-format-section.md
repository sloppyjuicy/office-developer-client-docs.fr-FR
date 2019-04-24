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
ms.openlocfilehash: 1ae923f6373b9cee76238b1fb27ec5eb3acb43ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360269"
---
# <a name="defaulttabstop-cell-text-block-format-section"></a><span data-ttu-id="d564c-103">DefaultTabstop, cellule (section Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="d564c-103">DefaultTabstop Cell (Text Block Format Section)</span></span>

<span data-ttu-id="d564c-104">Détermine l’intervalle des taquets de tabulation par défaut dans un bloc de texte.</span><span class="sxs-lookup"><span data-stu-id="d564c-104">Determines the interval of the default tab stops in a text block.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d564c-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="d564c-105">Remarks</span></span>

<span data-ttu-id="d564c-106">La valeur par défaut est de 1,5 cm pour les documents créés en unités métriques et de 0,5 pouce pour ceux créés en unités impériales.</span><span class="sxs-lookup"><span data-stu-id="d564c-106">The default value is 0.5 inches for documents created in imperial units and 1.5 centimeters for documents created in metric units.</span></span>
  
<span data-ttu-id="d564c-107">Pour obtenir une référence à la cellule DefaultTabstop par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d564c-107">To get a reference to the DefaultTabstop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d564c-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="d564c-108">Cell name:</span></span>  <br/> |<span data-ttu-id="d564c-109">DefaultTabstop</span><span class="sxs-lookup"><span data-stu-id="d564c-109">DefaultTabstop</span></span>  <br/> |
   
<span data-ttu-id="d564c-110">Pour obtenir une référence à la cellule DefaultTabstop à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d564c-110">To get a reference to the DefaultTabstop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d564c-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d564c-111">Section index:</span></span>  <br/> |<span data-ttu-id="d564c-112">**Définis**</span><span class="sxs-lookup"><span data-stu-id="d564c-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d564c-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d564c-113">Row index:</span></span>  <br/> |<span data-ttu-id="d564c-114">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="d564c-114">**visRowText**</span></span> <br/> |
|<span data-ttu-id="d564c-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d564c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="d564c-116">**visTxtBlkDefaultTabStop**</span><span class="sxs-lookup"><span data-stu-id="d564c-116">**visTxtBlkDefaultTabStop**</span></span> <br/> |
   

