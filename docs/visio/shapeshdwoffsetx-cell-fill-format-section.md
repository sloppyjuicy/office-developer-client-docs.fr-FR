---
title: ShapeShdwOffsetX, cellule (section Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60076
localization_priority: Normal
ms.assetid: a426f471-d35f-ef87-4c59-2c007ec2653f
description: Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.
ms.openlocfilehash: 5c3f994f0ceba84c86585a76c7a67667a0c20a53
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426484"
---
# <a name="shapeshdwoffsetx-cell-fill-format-section"></a><span data-ttu-id="17d1d-103">ShapeShdwOffsetX, cellule (section Fill Format)</span><span class="sxs-lookup"><span data-stu-id="17d1d-103">ShapeShdwOffsetX Cell (Fill Format Section)</span></span>

<span data-ttu-id="17d1d-104">Détermine, en unités de page, la distance du décalage horizontal entre l'ombre d'une forme et la forme.</span><span class="sxs-lookup"><span data-stu-id="17d1d-104">Determines the distance in page units that a shape's shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="17d1d-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="17d1d-105">Remarks</span></span>

<span data-ttu-id="17d1d-106">Cette valeur correspond à celle du paramètre **Décalage X** de la boîte de dialogue **Ombre** (sous l’onglet **Accueil**, dans le groupe **Forme**, cliquez sur **Ombre**, puis cliquez sur **Options d’ombres**).</span><span class="sxs-lookup"><span data-stu-id="17d1d-106">This value corresponds to the value in the **X Offset** setting in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="17d1d-107">Pour obtenir une référence à la cellule ShapeShdwOffsetX par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="17d1d-107">To get a reference to the ShapeShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17d1d-108">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="17d1d-108">Cell name:</span></span>  <br/> | <span data-ttu-id="17d1d-109">ShapeShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="17d1d-109">ShapeShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="17d1d-110">Pour obtenir une référence à la cellule ShapeShdwOffsetX à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="17d1d-110">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17d1d-111">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="17d1d-111">Section index:</span></span>  <br/> |<span data-ttu-id="17d1d-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="17d1d-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="17d1d-113">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="17d1d-113">Row index:</span></span>  <br/> |<span data-ttu-id="17d1d-114">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="17d1d-114">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="17d1d-115">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="17d1d-115">Cell index:</span></span>  <br/> |<span data-ttu-id="17d1d-116">**visFillShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="17d1d-116">**visFillShdwOffsetX**</span></span> <br/> |
   

