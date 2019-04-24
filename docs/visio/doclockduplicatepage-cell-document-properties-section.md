---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliquées, sous la forme d'une valeur booléenne.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338541"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="77430-103">DocLockDuplicatePage Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="77430-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="77430-104">Détermine si les pages du document peuvent être dupliquées, sous la forme d'une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="77430-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="77430-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="77430-105">TRUE</span></span>  <br/> |<span data-ttu-id="77430-106">\*\*\*\* Les doublons dans le menu contextuel page et la méthode Automation **page. Duplicate** sont tous deux désactivés.</span><span class="sxs-lookup"><span data-stu-id="77430-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="77430-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="77430-107">FALSE</span></span>  <br/> |<span data-ttu-id="77430-108">La page peut être dupliquée.</span><span class="sxs-lookup"><span data-stu-id="77430-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="77430-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="77430-109">Remarks</span></span>

<span data-ttu-id="77430-110">Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="77430-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77430-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="77430-111">Cell name:</span></span>  <br/> | <span data-ttu-id="77430-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="77430-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="77430-113">Pour obtenir une référence à la cellule **DocLockDuplicatePage** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="77430-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="77430-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="77430-114">Section index:</span></span>  <br/> |<span data-ttu-id="77430-115">**Définis**</span><span class="sxs-lookup"><span data-stu-id="77430-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="77430-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="77430-116">Row index:</span></span>  <br/> |<span data-ttu-id="77430-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="77430-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="77430-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="77430-118">Cell index:</span></span>  <br/> |<span data-ttu-id="77430-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="77430-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

