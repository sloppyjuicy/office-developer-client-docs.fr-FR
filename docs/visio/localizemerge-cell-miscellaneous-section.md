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
ms.openlocfilehash: ddd6041ec6531652deb38a0c16be2c741bac91a6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405673"
---
# <a name="localizemerge-cell-miscellaneous-section"></a><span data-ttu-id="38d6a-103">LocalizeMerge, cellule (section Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="38d6a-103">LocalizeMerge Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="38d6a-104">Détermine si les formes sont localisées lors de leur copie d'un document à l'autre.</span><span class="sxs-lookup"><span data-stu-id="38d6a-104">Determines whether shapes are localized when copied between documents.</span></span>
  
|<span data-ttu-id="38d6a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="38d6a-105">**Value**</span></span>|<span data-ttu-id="38d6a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="38d6a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="38d6a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="38d6a-107">TRUE</span></span>  <br/> | <span data-ttu-id="38d6a-108">Localise une forme dans la langue du document de destination.</span><span class="sxs-lookup"><span data-stu-id="38d6a-108">Localize a shape in the language of the destination document.</span></span>  <br/> |
| <span data-ttu-id="38d6a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="38d6a-109">FALSE</span></span>  <br/> | <span data-ttu-id="38d6a-110">Ne localisez pas une forme en fonction de la langue du document de destination (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="38d6a-110">Do not localize a shape based on the language of the destination document (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38d6a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="38d6a-111">Remarks</span></span>

<span data-ttu-id="38d6a-112">Pour obtenir une référence à la cellule LocalizeMerge par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="38d6a-112">To get a reference to the LocalizeMerge cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38d6a-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="38d6a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="38d6a-114">LocalizeMerge</span><span class="sxs-lookup"><span data-stu-id="38d6a-114">LocalizeMerge</span></span>  <br/> |
   
<span data-ttu-id="38d6a-115">Pour obtenir une référence à la cellule LocalizeMerge à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="38d6a-115">To get a reference to the LocalizeMerge cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="38d6a-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="38d6a-116">Section index:</span></span>  <br/> |<span data-ttu-id="38d6a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="38d6a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="38d6a-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="38d6a-118">Row index:</span></span>  <br/> |<span data-ttu-id="38d6a-119">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="38d6a-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="38d6a-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="38d6a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="38d6a-121">**visObjLocalizeMerge**</span><span class="sxs-lookup"><span data-stu-id="38d6a-121">**visObjLocalizeMerge**</span></span> <br/> |
   

