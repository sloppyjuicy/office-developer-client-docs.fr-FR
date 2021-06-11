---
title: Menu, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm690
localization_priority: Normal
ms.assetid: 29af746c-b081-24cf-a30d-a56353ee849e
description: Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.
ms.openlocfilehash: adb6915c34946472ada8c4ab4d02fa88bab6651a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436327"
---
# <a name="menu-cell-actions-section"></a><span data-ttu-id="571ed-103">Menu, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="571ed-103">Menu Cell (Actions Section)</span></span>

<span data-ttu-id="571ed-104">Définit le nom d’une option de menu qui s’affiche dans un menu contextuel ou de balise d’action pour une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="571ed-104">Defines the name of a menu item that appears on a shortcut or action tag menu for a shape or page.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="571ed-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="571ed-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="571ed-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="571ed-106">Remarks</span></span>

<span data-ttu-id="571ed-p101">Pour insérer un séparateur dans le menu au-dessus de cette option, utilisez la cellule BeginGroup. Pour faire apparaître la commande au bas du menu, faites précéder son nom d'un caractère de pourcentage (%) .</span><span class="sxs-lookup"><span data-stu-id="571ed-p101">To insert a separator into the menu above this item, use the BeginGroup cell. To display the command at the bottom of the menu, prefix the name with a percent character (%) .</span></span>
  
<span data-ttu-id="571ed-109">Pour obtenir une référence à la cellule Menu par un nom à partir d’une autre formule ou d’un programme en faisant appel à la **propriété CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="571ed-109">To get a reference to the Menu cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="571ed-110">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="571ed-110">Cell name:</span></span>  <br/> |<span data-ttu-id="571ed-111">Actions.</span><span class="sxs-lookup"><span data-stu-id="571ed-111">Actions.</span></span> <span data-ttu-id="571ed-112">*nom*  . Menuwhere Actions.</span><span class="sxs-lookup"><span data-stu-id="571ed-112">*name*  .Menuwhere Actions.</span></span>  <span data-ttu-id="571ed-113">*name*  est le nom de la ligne Actions</span><span class="sxs-lookup"><span data-stu-id="571ed-113">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="571ed-114">Pour obtenir une référence à la cellule Menu à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="571ed-114">To get a reference to the Menu cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="571ed-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="571ed-115">Section index:</span></span>  <br/> |<span data-ttu-id="571ed-116">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="571ed-116">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="571ed-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="571ed-117">Row index:</span></span>  <br/> |<span data-ttu-id="571ed-118">**visRowAction**  +   *i* où i = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="571ed-118">**visRowAction** +  *i*  where i = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="571ed-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="571ed-119">Cell index:</span></span>  <br/> |<span data-ttu-id="571ed-120">**visActionMenu**</span><span class="sxs-lookup"><span data-stu-id="571ed-120">**visActionMenu**</span></span> <br/> |
   

