---
title: PageLockDuplicate, cellule (Section Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Détermine si la page peut être dupliquée, comme une valeur booléenne.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789204"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="35a79-103">PageLockDuplicate, cellule (Section Page Properties)</span><span class="sxs-lookup"><span data-stu-id="35a79-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="35a79-104">Détermine si la page peut être dupliquée, comme une valeur booléenne.</span><span class="sxs-lookup"><span data-stu-id="35a79-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="35a79-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="35a79-105">TRUE</span></span>  <br/> |<span data-ttu-id="35a79-106">**En double** dans le menu contextuel de page et la méthode d’automation **Page.Duplicate** sont tous deux désactivés pour la page.</span><span class="sxs-lookup"><span data-stu-id="35a79-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="35a79-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="35a79-107">FALSE</span></span>  <br/> |<span data-ttu-id="35a79-108">La page peut être dupliquée.</span><span class="sxs-lookup"><span data-stu-id="35a79-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="35a79-109">Remarques</span><span class="sxs-lookup"><span data-stu-id="35a79-109">Remarks</span></span>

<span data-ttu-id="35a79-110">Pour obtenir une référence à la cellule **PageLockDuplicate** par un nom à partir d’une autre formule, par la valeur de l’attribut **N** d’un élément de **cellule** ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="35a79-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35a79-111">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="35a79-111">Cell name:</span></span>  <br/> | <span data-ttu-id="35a79-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="35a79-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="35a79-113">Pour obtenir une référence à la cellule **PageLockDuplicate** par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="35a79-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="35a79-114">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="35a79-114">Section index:</span></span>  <br/> |<span data-ttu-id="35a79-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="35a79-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="35a79-116">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="35a79-116">Row index:</span></span>  <br/> |<span data-ttu-id="35a79-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="35a79-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="35a79-118">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="35a79-118">Cell index:</span></span>  <br/> |<span data-ttu-id="35a79-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="35a79-119">**visPageLockDuplicate**</span></span> <br/> |
   

