---
title: PageLockDuplicate Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, sous la forme d'une valeur booléenne.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283663"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="fe8d4-103">PageLockDuplicate Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="fe8d4-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="fe8d4-104">Détermine si la page peut être dupliquée, sous la forme d'une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="fe8d4-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fe8d4-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="fe8d4-105">TRUE</span></span>  <br/> |<span data-ttu-id="fe8d4-106">\*\*\*\* Les doublons dans le menu contextuel page et la méthode Automation **page. Duplicate** sont tous deux désactivés pour la page.</span><span class="sxs-lookup"><span data-stu-id="fe8d4-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="fe8d4-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="fe8d4-107">FALSE</span></span>  <br/> |<span data-ttu-id="fe8d4-108">La page peut être dupliquée.</span><span class="sxs-lookup"><span data-stu-id="fe8d4-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fe8d4-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="fe8d4-109">Remarks</span></span>

<span data-ttu-id="fe8d4-110">Pour obtenir une référence à la cellule **PageLockDuplicate** par un nom à partir d'une autre formule, par valeur de l'attribut **N** d'un élément de **cellule** ou d'un programme en faisant appel à la propriété **CellsU** , utilisez:</span><span class="sxs-lookup"><span data-stu-id="fe8d4-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe8d4-111">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="fe8d4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fe8d4-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="fe8d4-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="fe8d4-113">Pour obtenir une référence à la cellule **PageLockDuplicate** à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="fe8d4-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fe8d4-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fe8d4-114">Section index:</span></span>  <br/> |<span data-ttu-id="fe8d4-115">**Définis**</span><span class="sxs-lookup"><span data-stu-id="fe8d4-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fe8d4-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fe8d4-116">Row index:</span></span>  <br/> |<span data-ttu-id="fe8d4-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="fe8d4-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="fe8d4-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fe8d4-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fe8d4-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="fe8d4-119">**visPageLockDuplicate**</span></span> <br/> |
   

