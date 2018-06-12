---
title: LocalizeMerge, cellule (section Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033773
localization_priority: Normal
ms.assetid: 734d4415-05dd-4c4d-763e-e035fa56dcec
description: Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.
ms.openlocfilehash: 47593802e412c1871685f7218dd2a810bc2bc469
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788976"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="25997-103">LocalizeMerge, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="25997-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="25997-104">Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.</span><span class="sxs-lookup"><span data-stu-id="25997-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="25997-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="25997-105">**Value**</span></span>|<span data-ttu-id="25997-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="25997-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="25997-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="25997-107">TRUE</span></span>  <br/> | <span data-ttu-id="25997-108">Localise une forme dans la langue du document de destination.</span><span class="sxs-lookup"><span data-stu-id="25997-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="25997-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="25997-109">FALSE</span></span>  <br/> | <span data-ttu-id="25997-110">Ne localise pas une forme en fonction de la langue du document de destination (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="25997-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25997-111">Note</span><span class="sxs-lookup"><span data-stu-id="25997-111">Remarks</span></span>

<span data-ttu-id="25997-112">Pour obtenir une référence à la cellule LocalizeMerge par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="25997-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25997-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="25997-113">Cell name:</span></span>  <br/> | <span data-ttu-id="25997-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="25997-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="25997-115">Pour obtenir une référence à la cellule LocalizeMerge par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="25997-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25997-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="25997-116">Section index:</span></span>  <br/> |<span data-ttu-id="25997-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="25997-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="25997-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="25997-118">Row index:</span></span>  <br/> |<span data-ttu-id="25997-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="25997-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="25997-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="25997-120">Cell index:</span></span>  <br/> |<span data-ttu-id="25997-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="25997-121">**visObjLocalizeMerge**</span></span> <br/> |
   

