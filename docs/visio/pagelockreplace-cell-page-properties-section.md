---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indique si le bouton Remplacer la forme doit être désactivé pour cette page.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433100"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="5ca2c-103">PageLockReplace Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="5ca2c-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="5ca2c-104">Indique si le bouton **Remplacer la** forme doit être désactivé pour cette page.</span><span class="sxs-lookup"><span data-stu-id="5ca2c-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="5ca2c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="5ca2c-105">**Value**</span></span>|<span data-ttu-id="5ca2c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="5ca2c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5ca2c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5ca2c-107">TRUE</span></span>  <br/> |<span data-ttu-id="5ca2c-108">Le **bouton Modifier la** forme est grisé lorsque cette page est active.</span><span class="sxs-lookup"><span data-stu-id="5ca2c-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="5ca2c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ca2c-109">FALSE</span></span>  <br/> |<span data-ttu-id="5ca2c-110">Le **bouton Modifier la** forme n’est pas désactivé par cette page.</span><span class="sxs-lookup"><span data-stu-id="5ca2c-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="5ca2c-111">Le bouton peut encore être grisé si : le **DocLockReplace** de la feuille de **document** est définie sur **TRUE**; la **cellule LockReplace** de la forme sélectionnée est définie sur **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="5ca2c-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ca2c-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="5ca2c-112">Remarks</span></span>

<span data-ttu-id="5ca2c-113">Pour obtenir une référence à la cellule **PageLockReplace** par un nom à partir d’une autre formule, de l’attribut **N** d’un élément **Cell** ou d’un programme en faisant appel à la propriété **CellsU,** utilisez :</span><span class="sxs-lookup"><span data-stu-id="5ca2c-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ca2c-114">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="5ca2c-114">Cell name:</span></span>  <br/> | <span data-ttu-id="5ca2c-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="5ca2c-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="5ca2c-116">Pour obtenir une référence à la **cellule PageLockReplace** à l’aide d’un index à partir d’un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="5ca2c-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ca2c-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="5ca2c-117">Section index:</span></span>  <br/> |<span data-ttu-id="5ca2c-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ca2c-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ca2c-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="5ca2c-119">Row index:</span></span>  <br/> |<span data-ttu-id="5ca2c-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5ca2c-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="5ca2c-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="5ca2c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="5ca2c-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="5ca2c-122">**visPageLockReplace**</span></span> <br/> |
   

