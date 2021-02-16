---
title: ShapeShdwOffsetY, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60077
localization_priority: Normal
ms.assetid: ef200f41-7b69-1291-f9df-a7035239a033
description: Détermine, en unités de page, la distance du décalage vertical entre l'ombre d'une forme et la forme.
ms.openlocfilehash: 4ae4347ba9009e88bbd181d4dd6e242e1fad53be
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426820"
---
# <a name="shapeshdwoffsety-cell-fill-format-section"></a><span data-ttu-id="e3ae6-103">ShapeShdwOffsetY, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="e3ae6-103">ShapeShdwOffsetY Cell (Fill Format Section)</span></span>

<span data-ttu-id="e3ae6-104">Détermine, en unités de page, la distance du décalage vertical entre l'ombre d'une forme et la forme.</span><span class="sxs-lookup"><span data-stu-id="e3ae6-104">Determines the distance in page units that a shape's shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3ae6-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="e3ae6-105">Remarks</span></span>

<span data-ttu-id="e3ae6-106">Cette valeur correspond à celle du paramètre **Décalage Y** de la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="e3ae6-106">This value corresponds to the value in the **Y Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="e3ae6-107">Pour obtenir une référence à la cellule ShapeShdwOffsetY par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="e3ae6-107">To get a reference to the ShapeShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3ae6-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="e3ae6-108">Cell name:</span></span>  <br/> | <span data-ttu-id="e3ae6-109">ShapeShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="e3ae6-109">ShapeShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="e3ae6-110">Pour obtenir une référence à la cellule ShapeShdwOffsetY à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e3ae6-110">To get a reference to the ShapeShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3ae6-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e3ae6-111">Section index:</span></span>  <br/> |<span data-ttu-id="e3ae6-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3ae6-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e3ae6-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e3ae6-113">Row index:</span></span>  <br/> |<span data-ttu-id="e3ae6-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e3ae6-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="e3ae6-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e3ae6-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e3ae6-116">**visFillShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="e3ae6-116">**visFillShdwOffsetY**</span></span> <br/> |
   

