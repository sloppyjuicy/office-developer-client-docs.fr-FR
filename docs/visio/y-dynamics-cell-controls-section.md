---
title: Y Dynamics, cellule (section Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Représente la coordonnée y du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales. Le point d'ancrage est utilisé pour l'étirement dynamique des formes.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341180"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="bf714-104">Y Dynamics, cellule (section Controls)</span><span class="sxs-lookup"><span data-stu-id="bf714-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="bf714-105">Représente la coordonnée *y* du point d'ancrage d'une poignée de contrôle, exprimée dans le système de coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="bf714-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="bf714-106">Le point d'ancrage est utilisé pour l'étirement dynamique des formes.</span><span class="sxs-lookup"><span data-stu-id="bf714-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bf714-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="bf714-107">Remarks</span></span>

<span data-ttu-id="bf714-108">Pour obtenir une référence à la cellule Y Dynamics par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bf714-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf714-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bf714-109">Cell name:</span></span>  <br/> | <span data-ttu-id="bf714-110">Vérifie.</span><span class="sxs-lookup"><span data-stu-id="bf714-110">Controls.</span></span>  <span data-ttu-id="bf714-111">*nom* . Contrôles YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="bf714-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="bf714-112">*Name* est le nom de la ligne Controls.</span><span class="sxs-lookup"><span data-stu-id="bf714-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="bf714-113">Pour obtenir une référence à la cellule Y Dynamics par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bf714-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bf714-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bf714-114">Section index:</span></span>  <br/> |<span data-ttu-id="bf714-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="bf714-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="bf714-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bf714-116">Row index:</span></span>  <br/> |<span data-ttu-id="bf714-117">**visRowControl** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bf714-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bf714-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bf714-118">Cell index:</span></span>  <br/> |<span data-ttu-id="bf714-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="bf714-119">**visCtlYDyn**</span></span> <br/> |
   

