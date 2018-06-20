---
title: DocLockReplace, cellule (Section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Détermine si la forme de remplacer l’interface utilisateur doit être désactivée pour ce document.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788517"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="80027-103">DocLockReplace, cellule (Section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="80027-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="80027-104">Détermine si la forme de remplacer l’interface utilisateur doit être désactivée pour ce document.</span><span class="sxs-lookup"><span data-stu-id="80027-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="80027-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="80027-105">TRUE</span></span>  <br/> |<span data-ttu-id="80027-106">Le bouton **Remplacer une forme** est désactivé dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="80027-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="80027-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="80027-107">FALSE</span></span>  <br/> |<span data-ttu-id="80027-108">Le bouton **Remplacer une forme** est actif dans l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="80027-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="80027-109">Les utilisateurs peuvent utiliser la fonctionnalité de remplacer la forme dans ce document.</span><span class="sxs-lookup"><span data-stu-id="80027-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="80027-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="80027-110">Remarks</span></span>

<span data-ttu-id="80027-111">Pour obtenir une référence à la cellule **DocLockReplace** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="80027-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80027-112">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="80027-112">Cell name:</span></span>  <br/> | <span data-ttu-id="80027-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="80027-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="80027-114">Pour obtenir une référence à la cellule **DocLocReplace** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="80027-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="80027-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="80027-115">Section index:</span></span>  <br/> |<span data-ttu-id="80027-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="80027-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="80027-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="80027-117">Row index:</span></span>  <br/> |<span data-ttu-id="80027-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="80027-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="80027-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="80027-119">Cell index:</span></span>  <br/> |<span data-ttu-id="80027-120">** visDocLockReplace **</span><span class="sxs-lookup"><span data-stu-id="80027-120">**visDocLockReplace **</span></span> <br/> |
   

