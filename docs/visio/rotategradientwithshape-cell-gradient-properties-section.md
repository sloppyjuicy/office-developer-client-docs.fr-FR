---
title: RotateGradientWithShape, cellule (Section Propriétés de dégradé)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Détermine si un dégradé de remplissage pivote avec une forme 2D rotation, en tant que valeur de type boolean.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789488"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="7dbb5-103">RotateGradientWithShape, cellule (Section Propriétés de dégradé)</span><span class="sxs-lookup"><span data-stu-id="7dbb5-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="7dbb5-104">Détermine si un dégradé de remplissage pivote avec une forme 2D rotation, en tant que valeur de type boolean.</span><span class="sxs-lookup"><span data-stu-id="7dbb5-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="7dbb5-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="7dbb5-105">**Value**</span></span>|<span data-ttu-id="7dbb5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="7dbb5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7dbb5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7dbb5-107">TRUE</span></span>  <br/> |<span data-ttu-id="7dbb5-108">Dégradé fait pivoter la forme lorsque vous faites pivoter la forme autour de l’axe de rotation.</span><span class="sxs-lookup"><span data-stu-id="7dbb5-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="7dbb5-109">« Haut » du dégradé est parallèle à la poignée de rotation.</span><span class="sxs-lookup"><span data-stu-id="7dbb5-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="7dbb5-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="7dbb5-110">FALSE</span></span>  <br/> |<span data-ttu-id="7dbb5-111">Dégradé ne pivote pas avec la forme lors de la rotation de la forme autour de l’axe de rotation.</span><span class="sxs-lookup"><span data-stu-id="7dbb5-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="7dbb5-112">« Haut » du dégradé est parallèle à la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="7dbb5-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7dbb5-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="7dbb5-113">Remarks</span></span>

<span data-ttu-id="7dbb5-114">Pour obtenir une référence à la cellule **RotateGradientWithShape** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="7dbb5-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dbb5-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7dbb5-115">Cell name:</span></span>  <br/> | <span data-ttu-id="7dbb5-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="7dbb5-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="7dbb5-117">Pour obtenir une référence à la cellule **RotateGradientWithShape** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7dbb5-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7dbb5-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7dbb5-118">Section index:</span></span>  <br/> |<span data-ttu-id="7dbb5-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7dbb5-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7dbb5-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7dbb5-120">Row index:</span></span>  <br/> |<span data-ttu-id="7dbb5-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="7dbb5-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="7dbb5-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7dbb5-122">Cell index:</span></span>  <br/> |<span data-ttu-id="7dbb5-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="7dbb5-123">**visRotateGradientWithShape**</span></span> <br/> |
   

