---
title: LockPreview, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348327"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="bb5c3-103">LockPreview, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="bb5c3-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="bb5c3-104">Détermine si un aperçu est enregistré chaque fois que vous enregistrez un dessin.</span><span class="sxs-lookup"><span data-stu-id="bb5c3-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="bb5c3-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="bb5c3-105">**Value**</span></span>|<span data-ttu-id="bb5c3-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="bb5c3-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="bb5c3-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bb5c3-107">TRUE</span></span>  <br/> | <span data-ttu-id="bb5c3-108">Un aperçu n'est pas enregistré chaque fois que vous enregistrez un dessin.</span><span class="sxs-lookup"><span data-stu-id="bb5c3-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="bb5c3-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="bb5c3-109">FALSE</span></span>  <br/> | <span data-ttu-id="bb5c3-110">Un aperçu est enregistré chaque fois que vous enregistrez un dessin.</span><span class="sxs-lookup"><span data-stu-id="bb5c3-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb5c3-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="bb5c3-111">Remarks</span></span>

<span data-ttu-id="bb5c3-112">Pour obtenir une référence à la cellule LockPreview par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="bb5c3-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb5c3-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bb5c3-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bb5c3-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="bb5c3-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="bb5c3-115">Pour obtenir une référence à la cellule LockPreview à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="bb5c3-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb5c3-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="bb5c3-116">Section index:</span></span>  <br/> |<span data-ttu-id="bb5c3-117">**Définis**</span><span class="sxs-lookup"><span data-stu-id="bb5c3-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bb5c3-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="bb5c3-118">Row index:</span></span>  <br/> |<span data-ttu-id="bb5c3-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="bb5c3-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="bb5c3-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="bb5c3-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bb5c3-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="bb5c3-121">**visDocLockPreview**</span></span> <br/> |
   

