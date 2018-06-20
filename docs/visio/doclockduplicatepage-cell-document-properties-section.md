---
title: DocLockDuplicatePage, cellule (Section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliqués, comme une valeur booléenne.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788493"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="e9023-103">DocLockDuplicatePage, cellule (Section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="e9023-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="e9023-104">Détermine si les pages du document peuvent être dupliqués, comme une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="e9023-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9023-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="e9023-105">TRUE</span></span>  <br/> |<span data-ttu-id="e9023-106">**En double** dans le menu contextuel de page et la méthode d’automation **Page.Duplicate** sont tous deux désactivés.</span><span class="sxs-lookup"><span data-stu-id="e9023-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="e9023-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="e9023-107">FALSE</span></span>  <br/> |<span data-ttu-id="e9023-108">La page peut être dupliquée.</span><span class="sxs-lookup"><span data-stu-id="e9023-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9023-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="e9023-109">Remarks</span></span>

<span data-ttu-id="e9023-110">Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="e9023-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9023-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e9023-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e9023-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="e9023-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="e9023-113">Pour obtenir une référence à la cellule **DocLockDuplicatePage** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="e9023-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9023-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="e9023-114">Section index:</span></span>  <br/> |<span data-ttu-id="e9023-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e9023-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e9023-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="e9023-116">Row index:</span></span>  <br/> |<span data-ttu-id="e9023-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="e9023-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="e9023-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="e9023-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e9023-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="e9023-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

