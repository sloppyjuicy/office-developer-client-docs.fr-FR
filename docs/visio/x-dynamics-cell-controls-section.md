---
title: X Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Représente la coordonnée x du point d’ancrage d’une poignée de contrôle dans les coordonnées locales.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432127"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="f9749-103">X Dynamics, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="f9749-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="f9749-104">Représente la coordonnée  *x*  du point d’ancrage d’une poignée de contrôle dans les coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="f9749-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f9749-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="f9749-105">Remarks</span></span>

<span data-ttu-id="f9749-106">Le point d'ancrage est utilisé pour l'étirement dynamique des formes.</span><span class="sxs-lookup"><span data-stu-id="f9749-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="f9749-107">Pour obtenir une référence à la cellule X Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="f9749-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9749-108">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f9749-108">Cell name:</span></span>  <br/> | <span data-ttu-id="f9749-109">Contrôles.</span><span class="sxs-lookup"><span data-stu-id="f9749-109">Controls.</span></span>  <span data-ttu-id="f9749-110">*nom*  . Contrôles XDynwhere.</span><span class="sxs-lookup"><span data-stu-id="f9749-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="f9749-111">*nom*  est le nom de la ligne des contrôles.</span><span class="sxs-lookup"><span data-stu-id="f9749-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f9749-112">Pour obtenir une référence à la cellule X Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="f9749-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f9749-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="f9749-113">Section index:</span></span>  <br/> |<span data-ttu-id="f9749-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f9749-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f9749-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="f9749-115">Row index:</span></span>  <br/> |<span data-ttu-id="f9749-116">**visRowControl**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f9749-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f9749-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="f9749-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f9749-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="f9749-118">**visCtlXDyn**</span></span> <br/> |
   

