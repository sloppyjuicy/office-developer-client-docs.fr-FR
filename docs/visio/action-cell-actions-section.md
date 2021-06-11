---
title: Action, cellule (section Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm5
localization_priority: Normal
ms.assetid: 435e49ee-0b51-8ce3-0589-3f0717026f4a
description: Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.
ms.openlocfilehash: e6bc576982cad871804cbcbc5f3d9c6bceb558c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407612"
---
# <a name="action-cell-actions-section"></a><span data-ttu-id="b8316-103">Action, cellule (section Actions)</span><span class="sxs-lookup"><span data-stu-id="b8316-103">Action Cell (Actions Section)</span></span>

<span data-ttu-id="b8316-104">Contient la formule à exécuter lorsqu’un utilisateur choisit une commande de menu contextuel ou de balise d’action.</span><span class="sxs-lookup"><span data-stu-id="b8316-104">Contains the formula to be executed when a user chooses a command on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b8316-105">Dans les versions précédentes de Microsoft Visio, les balises d’action sont appelées « balises actives ».</span><span class="sxs-lookup"><span data-stu-id="b8316-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b8316-106">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8316-106">Remarks</span></span>

<span data-ttu-id="b8316-107">Une cellule Action n'est évaluée que lorsque l'action se produit, et non lorsque la formule est entrée.</span><span class="sxs-lookup"><span data-stu-id="b8316-107">An Action cell is evaluated only when the action occurs, not when the formula is entered.</span></span>
  
<span data-ttu-id="b8316-108">Pour obtenir une référence à la cellule Action à partir du nom d’une autre formule ou d’un programme à l’aide de la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b8316-108">To get a reference to the the Action cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8316-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b8316-109">Cell name:</span></span>  <br/> | <span data-ttu-id="b8316-110">Actions.</span><span class="sxs-lookup"><span data-stu-id="b8316-110">Actions.</span></span>  <span data-ttu-id="b8316-111">*nom*  . Action où Actions.</span><span class="sxs-lookup"><span data-stu-id="b8316-111">*name*  .Action           where Actions.</span></span> <span data-ttu-id="b8316-112">*name*  est le nom de la ligne actions</span><span class="sxs-lookup"><span data-stu-id="b8316-112">*name*  is the name of the actions row</span></span>  <br/> |
   
<span data-ttu-id="b8316-113">Pour obtenir une référence à la cellule Action à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b8316-113">To get a reference to thethe Action cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8316-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b8316-114">Section index:</span></span>  <br/> |<span data-ttu-id="b8316-115">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="b8316-115">**visSectionAction**</span></span> <br/> |
| <span data-ttu-id="b8316-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b8316-116">Row index:</span></span>  <br/> |<span data-ttu-id="b8316-117">**visRowAction**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b8316-117">**visRowAction** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b8316-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b8316-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b8316-119">**visActionAction**</span><span class="sxs-lookup"><span data-stu-id="b8316-119">**visActionAction**</span></span> <br/> |
   

