---
title: Value, cellule (section User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1100
localization_priority: Normal
ms.assetid: 495b2aec-e197-75eb-9974-e7c92d26546f
description: Indique une valeur pour la cellule définie par l'utilisateur correspondante.
ms.openlocfilehash: 137d22430829f96a9c6ad69a73a6b44e964d5f4f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422987"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="b6ccb-103">Value, cellule (section User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="b6ccb-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="b6ccb-104">Indique une valeur pour la cellule définie par l'utilisateur correspondante.</span><span class="sxs-lookup"><span data-stu-id="b6ccb-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b6ccb-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="b6ccb-105">Remarks</span></span>

<span data-ttu-id="b6ccb-106">Pour faire référence à cette valeur dans une autre cellule, indiquez le nom défini par l'utilisateur entré dans la ligne User.Row.</span><span class="sxs-lookup"><span data-stu-id="b6ccb-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="b6ccb-107">Pour obtenir une référence à la cellule Value par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b6ccb-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6ccb-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b6ccb-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b6ccb-109">Guide.</span><span class="sxs-lookup"><span data-stu-id="b6ccb-109">User.</span></span>  <span data-ttu-id="b6ccb-110">*Nom* . Valeur où User.</span><span class="sxs-lookup"><span data-stu-id="b6ccb-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="b6ccb-111">*Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="b6ccb-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b6ccb-112">Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b6ccb-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6ccb-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b6ccb-113">Section index:</span></span>  <br/> |<span data-ttu-id="b6ccb-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="b6ccb-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="b6ccb-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b6ccb-115">Row index:</span></span>  <br/> |<span data-ttu-id="b6ccb-116">**visRowUser** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b6ccb-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b6ccb-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b6ccb-117">Cell index:</span></span>  <br/> |<span data-ttu-id="b6ccb-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="b6ccb-118">**visUserValue**</span></span> <br/> |
   

