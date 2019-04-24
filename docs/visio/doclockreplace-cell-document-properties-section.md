---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Détermine si l'interface utilisateur de remplacement de la forme doit être désactivée pour ce document.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338604"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="6a2ce-103">DocLockReplace Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="6a2ce-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="6a2ce-104">Détermine si l'interface utilisateur de remplacement de la forme doit être désactivée pour ce document.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6a2ce-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="6a2ce-105">TRUE</span></span>  <br/> |<span data-ttu-id="6a2ce-106">Le bouton **remplacer la forme** est grisé dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="6a2ce-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="6a2ce-107">FALSE</span></span>  <br/> |<span data-ttu-id="6a2ce-108">Le bouton **remplacer la forme** est actif dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="6a2ce-109">Les utilisateurs peuvent utiliser la fonctionnalité remplacer la forme dans ce document.</span><span class="sxs-lookup"><span data-stu-id="6a2ce-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a2ce-110">Remarques</span><span class="sxs-lookup"><span data-stu-id="6a2ce-110">Remarks</span></span>

<span data-ttu-id="6a2ce-111">Pour obtenir une référence à la cellule **DocLockReplace** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="6a2ce-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a2ce-112">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="6a2ce-112">Cell name:</span></span>  <br/> | <span data-ttu-id="6a2ce-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="6a2ce-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="6a2ce-114">Pour obtenir une référence à la cellule **DocLocReplace** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="6a2ce-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a2ce-115">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6a2ce-115">Section index:</span></span>  <br/> |<span data-ttu-id="6a2ce-116">**Définis**</span><span class="sxs-lookup"><span data-stu-id="6a2ce-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a2ce-117">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6a2ce-117">Row index:</span></span>  <br/> |<span data-ttu-id="6a2ce-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="6a2ce-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="6a2ce-119">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6a2ce-119">Cell index:</span></span>  <br/> |<span data-ttu-id="6a2ce-120">\* \* visDocLockReplace \* \*</span><span class="sxs-lookup"><span data-stu-id="6a2ce-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

