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
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788653"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="87443-103">FlyoutChild, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="87443-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="87443-104">Détermine si la ligne est un menu flottant enfant de la dernière ligne se trouvant au-dessus d’elle si cette dernière n’est pas un menu flottant enfant.</span><span class="sxs-lookup"><span data-stu-id="87443-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="87443-105">Note</span><span class="sxs-lookup"><span data-stu-id="87443-105">Remarks</span></span>

<span data-ttu-id="87443-106">Pour obtenir une référence à la cellule FlyoutChild par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="87443-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87443-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="87443-107">Cell name:</span></span>  <br/> |<span data-ttu-id="87443-108">Actions.</span><span class="sxs-lookup"><span data-stu-id="87443-108">Actions.</span></span> <span data-ttu-id="87443-109">*nom* . Actions FlyoutChildwhere.</span><span class="sxs-lookup"><span data-stu-id="87443-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="87443-110">*nom* est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="87443-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="87443-111">Pour obtenir une référence à la cellule FlyoutChild par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="87443-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="87443-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="87443-112">Section index:</span></span>  <br/> |<span data-ttu-id="87443-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="87443-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="87443-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="87443-114">Row index:</span></span>  <br/> |<span data-ttu-id="87443-115">**visRowAction** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87443-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="87443-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="87443-116">Cell index:</span></span>  <br/> |<span data-ttu-id="87443-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="87443-117">**visActionFlyoutChild**</span></span> <br/> |
   

