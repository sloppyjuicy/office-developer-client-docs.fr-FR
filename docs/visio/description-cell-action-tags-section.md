---
title: Description, cellule (section Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.
ms.openlocfilehash: 00c7a4c1547927b8d1a979b8ae074f96f26dc17c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360229"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="102d2-103">Description Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="102d2-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="102d2-104">Contient une chaîne qui décrit la balise d’action, qui s’affiche sous forme d’info-bulle lorsque l’utilisateur place le pointeur sur la balise.</span><span class="sxs-lookup"><span data-stu-id="102d2-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="102d2-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="102d2-105">Remarks</span></span>

<span data-ttu-id="102d2-106">Pour faire référence à la cellule Description par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="102d2-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="102d2-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="102d2-107">Cell name:</span></span>  <br/> | <span data-ttu-id="102d2-108">SmartTag.</span><span class="sxs-lookup"><span data-stu-id="102d2-108">SmartTags.</span></span>  <span data-ttu-id="102d2-109">*nom* . Description où SmartTags.</span><span class="sxs-lookup"><span data-stu-id="102d2-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="102d2-110">*Name* est le nom de la ligne de balise d'action</span><span class="sxs-lookup"><span data-stu-id="102d2-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="102d2-111">Pour faire référence à la cellule Description à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="102d2-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="102d2-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="102d2-112">Section index:</span></span>  <br/> |<span data-ttu-id="102d2-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="102d2-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="102d2-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="102d2-114">Row index:</span></span>  <br/> |<span data-ttu-id="102d2-115">**visRowSmartTag** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="102d2-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="102d2-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="102d2-116">Cell index:</span></span>  <br/> |<span data-ttu-id="102d2-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="102d2-117">**visSmartTagDescription**</span></span> <br/> |
   

