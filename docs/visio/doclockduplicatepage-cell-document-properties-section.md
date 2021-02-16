---
title: DocLockDuplicatePage Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Détermine si les pages du document peuvent être dupliquées, en tant que booléens.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439659"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="7f022-103">DocLockDuplicatePage Cell (Document Properties Section)</span><span class="sxs-lookup"><span data-stu-id="7f022-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="7f022-104">Détermine si les pages du document peuvent être dupliquées, en tant que booléens.</span><span class="sxs-lookup"><span data-stu-id="7f022-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7f022-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="7f022-105">TRUE</span></span>  <br/> |<span data-ttu-id="7f022-106">**Le doublon** dans le menu raccourci de la page et la **méthode d’automatisation Page.Duplicate** sont tous deux désactivés.</span><span class="sxs-lookup"><span data-stu-id="7f022-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="7f022-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="7f022-107">FALSE</span></span>  <br/> |<span data-ttu-id="7f022-108">La page peut être dupliquée.</span><span class="sxs-lookup"><span data-stu-id="7f022-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f022-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="7f022-109">Remarks</span></span>

<span data-ttu-id="7f022-110">Pour obtenir une référence à la cellule **DocLockDuplicatePage** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="7f022-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f022-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="7f022-111">Cell name:</span></span>  <br/> | <span data-ttu-id="7f022-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="7f022-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="7f022-113">Pour obtenir une référence à la **cellule DocLockDuplicatePage** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="7f022-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7f022-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="7f022-114">Section index:</span></span>  <br/> |<span data-ttu-id="7f022-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7f022-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7f022-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="7f022-116">Row index:</span></span>  <br/> |<span data-ttu-id="7f022-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="7f022-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="7f022-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="7f022-118">Cell index:</span></span>  <br/> |<span data-ttu-id="7f022-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="7f022-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

