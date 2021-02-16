---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme. ReplaceLockShapeData détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme en cours de remplacement.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408872"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="6b2aa-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="6b2aa-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="6b2aa-105">Indique si les valeurs des cellules spécifiées dans une forme de base remplacent les valeurs (y compris les valeurs locales) d’une forme remplacée lors d’une opération de remplacement de forme.</span><span class="sxs-lookup"><span data-stu-id="6b2aa-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="6b2aa-106">**ReplaceLockShapeData** détermine si les données de forme de la forme de base remplacent toutes les données de forme de la forme en cours de remplacement.</span><span class="sxs-lookup"><span data-stu-id="6b2aa-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="6b2aa-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-107">**Value**</span></span>|<span data-ttu-id="6b2aa-108">**Description**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b2aa-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="6b2aa-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="6b2aa-110">Toutes les lignes et valeurs de la section **Données** de forme de la forme de base sont copiées sur la forme de remplacement et toutes les valeurs locales de l’ancienne forme en cours de remplacement sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="6b2aa-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="6b2aa-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="6b2aa-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="6b2aa-112">Les lignes et les valeurs de la section **Données** de forme de la forme de base sont copiées dans la forme de remplacement.</span><span class="sxs-lookup"><span data-stu-id="6b2aa-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="6b2aa-113">Toutes les lignes de la section **Données de** forme de l’ancienne forme avec des valeurs locales sont transférées vers la forme de remplacement.</span><span class="sxs-lookup"><span data-stu-id="6b2aa-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b2aa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="6b2aa-114">Remarks</span></span>

<span data-ttu-id="6b2aa-115">Pour obtenir une référence à la cellule **ReplaceLockShapeData** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="6b2aa-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b2aa-116">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="6b2aa-116">Cell name:</span></span>  <br/> | <span data-ttu-id="6b2aa-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="6b2aa-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="6b2aa-118">Pour obtenir une référence à la **cellule ReplaceLockShapeData** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6b2aa-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b2aa-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6b2aa-119">Section index:</span></span>  <br/> |<span data-ttu-id="6b2aa-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b2aa-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6b2aa-121">Row index:</span></span>  <br/> |<span data-ttu-id="6b2aa-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="6b2aa-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6b2aa-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6b2aa-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="6b2aa-124">**visReplaceLockShapeData**</span></span> <br/> |
   

