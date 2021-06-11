---
title: QuickStyleFontColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Détermine la couleur de police des styles rapides dont le texte d’une forme hérite du thème actif, sous la forme d’un nombre integer de 0 à 1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415025"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="56e89-103">QuickStyleFontColor Cell (Quick Style Section)</span><span class="sxs-lookup"><span data-stu-id="56e89-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="56e89-104">Détermine la couleur de police des styles rapides dont le texte d’une forme hérite du thème actif, sous la forme d’un nombre integer de 0 à 1.</span><span class="sxs-lookup"><span data-stu-id="56e89-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56e89-105">Valeur</span><span class="sxs-lookup"><span data-stu-id="56e89-105">Value</span></span>  <br/> |<span data-ttu-id="56e89-106">Description</span><span class="sxs-lookup"><span data-stu-id="56e89-106">Description</span></span>  <br/> |
|<span data-ttu-id="56e89-107">0</span><span class="sxs-lookup"><span data-stu-id="56e89-107">0</span></span>  <br/> |<span data-ttu-id="56e89-108">Le texte de la forme utilise la couleur de police Foncé.</span><span class="sxs-lookup"><span data-stu-id="56e89-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="56e89-109">1</span><span class="sxs-lookup"><span data-stu-id="56e89-109">1</span></span>  <br/> |<span data-ttu-id="56e89-110">Le texte de la forme utilise la couleur de police Light.</span><span class="sxs-lookup"><span data-stu-id="56e89-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56e89-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="56e89-111">Remarks</span></span>

<span data-ttu-id="56e89-112">Pour obtenir une référence à la cellule **QuickStyleFontColor** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="56e89-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56e89-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="56e89-113">Cell name:</span></span>  <br/> | <span data-ttu-id="56e89-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="56e89-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="56e89-115">Pour obtenir une référence à la **cellule QuickStyleFontColor** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="56e89-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56e89-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="56e89-116">Section index:</span></span>  <br/> |<span data-ttu-id="56e89-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="56e89-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="56e89-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="56e89-118">Row index:</span></span>  <br/> |<span data-ttu-id="56e89-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="56e89-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="56e89-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="56e89-120">Cell index:</span></span>  <br/> |<span data-ttu-id="56e89-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="56e89-121">**visQuickStyleFontColor**</span></span> <br/> |
   

