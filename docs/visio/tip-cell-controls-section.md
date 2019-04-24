---
title: Tip, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1010
localization_priority: Normal
ms.assetid: 7fd11650-fffa-1316-d302-3122ac5feb14
description: Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.
ms.openlocfilehash: b9b0c19aff5e3ab8a4c1e29d319eb42f7ee4a271
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307720"
---
# <a name="tip-cell-controls-section"></a><span data-ttu-id="2e18b-104">Tip, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="2e18b-104">Tip Cell (Controls Section)</span></span>

<span data-ttu-id="2e18b-p102">Représente une chaîne de description qui apparaît sous la forme d'une info-bulle lorsqu'un utilisateur maintient quelques instants le pointeur sur la poignée de contrôle d'une forme. L'application affiche automatiquement ces informations détaillées entre guillemets dans la cellule. Ces guillemets n'apparaissent pas dans l'info-bulle.</span><span class="sxs-lookup"><span data-stu-id="2e18b-p102">Represents a descriptive text string that appears as a tool tip when a user pauses the pointer over a shape's control handle. The application automatically encloses the tip string in quotation marks in the cell, but the quotation marks are not displayed in the tool tip.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e18b-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="2e18b-107">Remarks</span></span>

<span data-ttu-id="2e18b-108">Pour obtenir une référence à la cellule Tip par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="2e18b-108">To get a reference to the Tip cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e18b-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e18b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2e18b-110">Vérifie.</span><span class="sxs-lookup"><span data-stu-id="2e18b-110">Controls.</span></span>  <span data-ttu-id="2e18b-111">*nom* . Contrôles Tipwhere.</span><span class="sxs-lookup"><span data-stu-id="2e18b-111">*name*  .Tipwhere Controls.</span></span>  <span data-ttu-id="2e18b-112">*Name* est le nom de la ligne Controls.</span><span class="sxs-lookup"><span data-stu-id="2e18b-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="2e18b-113">Pour obtenir une référence à la cellule Tip par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="2e18b-113">To get a reference to the Tip cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e18b-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="2e18b-114">Section index:</span></span>  <br/> |<span data-ttu-id="2e18b-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="2e18b-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="2e18b-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="2e18b-116">Row index:</span></span>  <br/> |<span data-ttu-id="2e18b-117">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2e18b-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2e18b-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="2e18b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="2e18b-119">**visCtlTip**</span><span class="sxs-lookup"><span data-stu-id="2e18b-119">**visCtlTip**</span></span> <br/> |
   

