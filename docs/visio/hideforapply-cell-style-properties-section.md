---
title: HideForApply, cellule (section Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Détermine où un style apparaît dans l’interface utilisateur de Microsoft Visio.
ms.openlocfilehash: 5b0221c54c17a3b9957cce5e890842def0ba7525
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788787"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="10e96-103">HideForApply, cellule (section Style Properties)</span><span class="sxs-lookup"><span data-stu-id="10e96-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="10e96-104">Détermine où un style apparaît dans l’interface utilisateur de Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="10e96-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="10e96-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="10e96-105">**Value**</span></span>|<span data-ttu-id="10e96-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="10e96-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="10e96-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="10e96-107">TRUE</span></span>  <br/> | <span data-ttu-id="10e96-108">Le style apparaît uniquement dans l' **Explorateur de dessins**.</span><span class="sxs-lookup"><span data-stu-id="10e96-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="10e96-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="10e96-109">FALSE</span></span>  <br/> | <span data-ttu-id="10e96-110">Le style apparaît dans l' **Explorateur de dessins**.</span><span class="sxs-lookup"><span data-stu-id="10e96-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10e96-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="10e96-111">Remarks</span></span>

<span data-ttu-id="10e96-112">Lorsque vous basez un nouveau style sur un style masqué, il n'hérite pas de cet attribut.</span><span class="sxs-lookup"><span data-stu-id="10e96-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="10e96-113">Pour obtenir une référence à la cellule HideForApply par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="10e96-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10e96-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10e96-114">Cell name:</span></span>  <br/> | <span data-ttu-id="10e96-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="10e96-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="10e96-116">Pour obtenir une référence à la cellule HideForApply par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="10e96-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10e96-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="10e96-117">Section index:</span></span>  <br/> |<span data-ttu-id="10e96-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10e96-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="10e96-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="10e96-119">Row index:</span></span>  <br/> |<span data-ttu-id="10e96-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="10e96-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="10e96-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="10e96-121">Cell index:</span></span>  <br/> |<span data-ttu-id="10e96-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="10e96-122">**visStyleHidden**</span></span> <br/> |
   

