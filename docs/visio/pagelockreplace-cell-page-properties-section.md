---
title: PageLockReplace, cellule (Section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indique si le bouton Remplacer la forme doit être désactivé pour cette page.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789210"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="b8fff-103">PageLockReplace, cellule (Section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="b8fff-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="b8fff-104">Indique si le bouton **Remplacer la forme** doit être désactivé pour cette page.</span><span class="sxs-lookup"><span data-stu-id="b8fff-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="b8fff-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="b8fff-105">**Value**</span></span>|<span data-ttu-id="b8fff-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="b8fff-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b8fff-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="b8fff-107">TRUE</span></span>  <br/> |<span data-ttu-id="b8fff-108">Le bouton **Modifier la forme** est grisé lorsque cette page est active.</span><span class="sxs-lookup"><span data-stu-id="b8fff-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="b8fff-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b8fff-109">FALSE</span></span>  <br/> |<span data-ttu-id="b8fff-110">Le bouton **Modifier la forme** n’est pas désactivé par cette page.</span><span class="sxs-lookup"><span data-stu-id="b8fff-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="b8fff-111">Le bouton peut-être toujours être grisé if : le **DocLockReplace** sur la **propriété DocumentSheet** est définie sur **TRUE**; la cellule **LockReplace** de la forme sélectionnée est définie sur **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="b8fff-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b8fff-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="b8fff-112">Remarks</span></span>

<span data-ttu-id="b8fff-113">Pour obtenir une référence à la cellule **PageLockReplace** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="b8fff-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8fff-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b8fff-114">Cell name:</span></span>  <br/> | <span data-ttu-id="b8fff-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="b8fff-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="b8fff-116">Pour obtenir une référence à la cellule **PageLockReplace** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b8fff-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8fff-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b8fff-117">Section index:</span></span>  <br/> |<span data-ttu-id="b8fff-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b8fff-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b8fff-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b8fff-119">Row index:</span></span>  <br/> |<span data-ttu-id="b8fff-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="b8fff-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="b8fff-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b8fff-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b8fff-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="b8fff-122">**visPageLockReplace**</span></span> <br/> |
   

