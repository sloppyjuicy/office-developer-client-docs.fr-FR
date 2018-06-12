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
description: Indique un message descriptif ou commentaire pour la cellule définie par l'utilisateur. L’application insère automatiquement le texte d’invite les guillemets doubles () pour indiquer qu’il s’agit d’une chaîne de texte. Si vous tapez un signe égal (=) et omettez les guillemets, vous pouvez entrer une formule dans une cellule qui évalue l’application.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789372"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="4cbc6-105">Prompt, cellule (section User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="4cbc6-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="4cbc6-p102">Contient un message descriptif ou commentaire associé à la cellule définie par l'utilisateur. L'application encadre automatiquement le message par des guillemets (" ") pour signaler qu'il s'agit d'une chaîne de texte. Si vous tapez un signe égal (=) sans guillemets, vous pouvez entrer dans cette cellule une formule qui est alors évaluée par l'application.</span><span class="sxs-lookup"><span data-stu-id="4cbc6-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4cbc6-109">Note</span><span class="sxs-lookup"><span data-stu-id="4cbc6-109">Remarks</span></span>

<span data-ttu-id="4cbc6-110">Pour obtenir une référence à la cellule Prompt par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="4cbc6-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4cbc6-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4cbc6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="4cbc6-112">Utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4cbc6-112">User.</span></span>  <span data-ttu-id="4cbc6-113">*Nom* . Où invite utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4cbc6-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="4cbc6-114">*Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="4cbc6-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="4cbc6-115">Pour obtenir une référence à la cellule Prompt par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="4cbc6-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4cbc6-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="4cbc6-116">Section index:</span></span>  <br/> |<span data-ttu-id="4cbc6-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="4cbc6-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="4cbc6-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="4cbc6-118">Row index:</span></span>  <br/> |<span data-ttu-id="4cbc6-119">**visRowUser +** *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4cbc6-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4cbc6-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="4cbc6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4cbc6-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="4cbc6-121">**visUserPrompt**</span></span> <br/> |
   

