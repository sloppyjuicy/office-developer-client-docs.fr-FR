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
ms.openlocfilehash: d320c35fa8ae65dd0b21a83ad2cf23dbb3af77f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790000"
---
# <a name="value-cell-user-defined-cells-section"></a><span data-ttu-id="159d9-103">Value, cellule (section User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="159d9-103">Value Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="159d9-104">Indique une valeur pour la cellule définie par l'utilisateur correspondante.</span><span class="sxs-lookup"><span data-stu-id="159d9-104">Specifies a value for the corresponding user-defined cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="159d9-105">Note</span><span class="sxs-lookup"><span data-stu-id="159d9-105">Remarks</span></span>

<span data-ttu-id="159d9-106">Pour faire référence à cette valeur dans une autre cellule, indiquez le nom défini par l'utilisateur entré dans la ligne User.Row.</span><span class="sxs-lookup"><span data-stu-id="159d9-106">To refer to this value in another cell, specify the user-defined name entered in the row label User.Row.</span></span>
  
<span data-ttu-id="159d9-107">Pour obtenir une référence à la cellule Value par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="159d9-107">To get a reference to the Value cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="159d9-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="159d9-108">Cell name:</span></span>  <br/> | <span data-ttu-id="159d9-109">Utilisateur.</span><span class="sxs-lookup"><span data-stu-id="159d9-109">User.</span></span>  <span data-ttu-id="159d9-110">*Nom* . Où la valeur utilisateur.</span><span class="sxs-lookup"><span data-stu-id="159d9-110">*Name*  .Value            where User.</span></span>  <span data-ttu-id="159d9-111">*Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="159d9-111">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="159d9-112">Pour obtenir une référence à la cellule Value par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="159d9-112">To get a reference to the Value cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="159d9-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="159d9-113">Section index:</span></span>  <br/> |<span data-ttu-id="159d9-114">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="159d9-114">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="159d9-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="159d9-115">Row index:</span></span>  <br/> |<span data-ttu-id="159d9-116">**visRowUser** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="159d9-116">**visRowUser** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="159d9-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="159d9-117">Cell index:</span></span>  <br/> |<span data-ttu-id="159d9-118">**visUserValue**</span><span class="sxs-lookup"><span data-stu-id="159d9-118">**visUserValue**</span></span> <br/> |
   

