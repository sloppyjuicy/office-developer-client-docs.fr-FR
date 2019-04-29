---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Détermine si un dégradé de remplissage pivote avec une forme dans la rotation 2D, sous la forme d'un type Boolean.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412218"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a><span data-ttu-id="00bec-103">RotateGradientWithShape Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="00bec-103">RotateGradientWithShape Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="00bec-104">Détermine si un dégradé de remplissage pivote avec une forme dans la rotation 2D, sous la forme d'un type Boolean.</span><span class="sxs-lookup"><span data-stu-id="00bec-104">Determines whether a fill gradient rotates with a shape in 2D rotation, as a boolean.</span></span>
  
|<span data-ttu-id="00bec-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="00bec-105">**Value**</span></span>|<span data-ttu-id="00bec-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="00bec-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00bec-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="00bec-107">TRUE</span></span>  <br/> |<span data-ttu-id="00bec-108">Le dégradé pivote avec la forme lorsque la forme pivote autour de la broche de rotation.</span><span class="sxs-lookup"><span data-stu-id="00bec-108">The gradient rotates with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="00bec-109">Le «haut» du dégradé est parallèle à la poignée de rotation.</span><span class="sxs-lookup"><span data-stu-id="00bec-109">The "top" of the gradient is parallel to the rotation handle.</span></span>  <br/> |
|<span data-ttu-id="00bec-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="00bec-110">FALSE</span></span>  <br/> |<span data-ttu-id="00bec-111">Le dégradé ne pivote pas avec la forme lorsque la forme pivote autour de la broche de rotation.</span><span class="sxs-lookup"><span data-stu-id="00bec-111">The gradient does not rotate with the shape when the shape is rotated around the rotation pin.</span></span> <span data-ttu-id="00bec-112">Le «haut» du dégradé est parallèle à la zone de dessin.</span><span class="sxs-lookup"><span data-stu-id="00bec-112">The "top" of the gradient is parallel to the drawing canvas.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00bec-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="00bec-113">Remarks</span></span>

<span data-ttu-id="00bec-114">Pour obtenir une référence à la cellule **RotateGradientWithShape** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="00bec-114">To get a reference to the **RotateGradientWithShape** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00bec-115">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="00bec-115">Cell name:</span></span>  <br/> | <span data-ttu-id="00bec-116">RotateGradientWithShape</span><span class="sxs-lookup"><span data-stu-id="00bec-116">RotateGradientWithShape</span></span>  <br/> |
   
<span data-ttu-id="00bec-117">Pour obtenir une référence à la cellule **RotateGradientWithShape** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="00bec-117">To get a reference to the **RotateGradientWithShape** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00bec-118">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="00bec-118">Section index:</span></span>  <br/> |<span data-ttu-id="00bec-119">**Définis**</span><span class="sxs-lookup"><span data-stu-id="00bec-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="00bec-120">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="00bec-120">Row index:</span></span>  <br/> |<span data-ttu-id="00bec-121">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="00bec-121">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="00bec-122">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="00bec-122">Cell index:</span></span>  <br/> |<span data-ttu-id="00bec-123">**visRotateGradientWithShape**</span><span class="sxs-lookup"><span data-stu-id="00bec-123">**visRotateGradientWithShape**</span></span> <br/> |
   

