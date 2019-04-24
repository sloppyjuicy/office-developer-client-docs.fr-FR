---
title: Prompt, cellule (section User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Contient un message descriptif ou commentaire associé à la cellule définie par l'utilisateur. L'application encadre automatiquement le texte de l'invite entre guillemets () pour indiquer qu'il s'agit d'une chaîne de texte. Si vous tapez un signe égal (=) sans guillemets, vous pouvez entrer dans cette cellule une formule qui est alors évaluée par l'application.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326886"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="2d131-105">Prompt, cellule (section User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="2d131-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="2d131-p102">Contient un message descriptif ou commentaire associé à la cellule définie par l'utilisateur. L'application encadre automatiquement le message par des guillemets (" ") pour signaler qu'il s'agit d'une chaîne de texte. Si vous tapez un signe égal (=) sans guillemets, vous pouvez entrer dans cette cellule une formule qui est alors évaluée par l'application.</span><span class="sxs-lookup"><span data-stu-id="2d131-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2d131-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="2d131-109">Remarks</span></span>

<span data-ttu-id="2d131-110">Pour obtenir une référence à la cellule Prompt par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2d131-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d131-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2d131-111">Cell name:</span></span>  <br/> | <span data-ttu-id="2d131-112">Guide.</span><span class="sxs-lookup"><span data-stu-id="2d131-112">User.</span></span>  <span data-ttu-id="2d131-113">*Nom* . Invite où utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2d131-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="2d131-114">*Name* est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="2d131-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="2d131-115">Pour obtenir une référence à la cellule Prompt à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2d131-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d131-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2d131-116">Section index:</span></span>  <br/> |<span data-ttu-id="2d131-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="2d131-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="2d131-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2d131-118">Row index:</span></span>  <br/> |<span data-ttu-id="2d131-119">**visRowUser +** *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2d131-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2d131-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2d131-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2d131-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="2d131-121">**visUserPrompt**</span></span> <br/> |
   

