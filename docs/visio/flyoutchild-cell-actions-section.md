---
title: FlyoutChild, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420863"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="9893e-103">FlyoutChild, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="9893e-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="9893e-104">Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant.</span><span class="sxs-lookup"><span data-stu-id="9893e-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9893e-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="9893e-105">Remarks</span></span>

<span data-ttu-id="9893e-106">Pour obtenir une référence à la cellule FlyoutChild par le nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="9893e-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9893e-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="9893e-107">Cell name:</span></span>  <br/> |<span data-ttu-id="9893e-108">Actions.</span><span class="sxs-lookup"><span data-stu-id="9893e-108">Actions.</span></span> <span data-ttu-id="9893e-109">*nom*  . FlyoutChildwhere Actions.</span><span class="sxs-lookup"><span data-stu-id="9893e-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="9893e-110">*name*  est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="9893e-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="9893e-111">Pour obtenir une référence à la cellule FlyoutChild à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="9893e-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9893e-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="9893e-112">Section index:</span></span>  <br/> |<span data-ttu-id="9893e-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="9893e-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="9893e-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="9893e-114">Row index:</span></span>  <br/> |<span data-ttu-id="9893e-115">**visRowAction**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9893e-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9893e-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="9893e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="9893e-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="9893e-117">**visActionFlyoutChild**</span></span> <br/> |
   

