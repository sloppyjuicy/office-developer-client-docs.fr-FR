---
title: ReplaceLockShapeData, cellule (Section de comportement de forme modification)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme. Le ReplaceLockShapeData détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme remplacée.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789470"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="fb3af-104">ReplaceLockShapeData, cellule (Section de comportement de forme modification)</span><span class="sxs-lookup"><span data-stu-id="fb3af-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="fb3af-105">Indique si les valeurs des cellules spécifiées dans une forme de remplacent les valeurs (y compris les valeurs locales) d’une forme qui est remplacé pendant une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="fb3af-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="fb3af-106">Le **ReplaceLockShapeData** détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme remplacée.</span><span class="sxs-lookup"><span data-stu-id="fb3af-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="fb3af-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="fb3af-107">**Value**</span></span>|<span data-ttu-id="fb3af-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="fb3af-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fb3af-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="fb3af-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="fb3af-110">Toutes les lignes et les valeurs de la section **Données de forme** de la forme de base sont copiés dans la forme de remplacement et des valeurs locales de la forme ancienne remplacée sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="fb3af-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="fb3af-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="fb3af-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="fb3af-112">Les lignes et les valeurs de la section **Données de forme** de la forme de base sont copiés à la forme de remplacement.</span><span class="sxs-lookup"><span data-stu-id="fb3af-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="fb3af-113">Toutes les lignes dans la section **Données de forme** de la forme avec les valeurs locales ancienne sont transférés vers la forme de remplacement.</span><span class="sxs-lookup"><span data-stu-id="fb3af-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb3af-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="fb3af-114">Remarks</span></span>

<span data-ttu-id="fb3af-115">Pour obtenir une référence à la cellule **ReplaceLockShapeData** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fb3af-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb3af-116">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fb3af-116">Cell name:</span></span>  <br/> | <span data-ttu-id="fb3af-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="fb3af-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="fb3af-118">Pour obtenir une référence à la cellule **ReplaceLockShapeData** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fb3af-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fb3af-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fb3af-119">Section index:</span></span>  <br/> |<span data-ttu-id="fb3af-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fb3af-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fb3af-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fb3af-121">Row index:</span></span>  <br/> |<span data-ttu-id="fb3af-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="fb3af-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="fb3af-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fb3af-123">Cell index:</span></span>  <br/> |<span data-ttu-id="fb3af-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="fb3af-124">**visReplaceLockShapeData**</span></span> <br/> |
   

