---
title: Invisible, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788848"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="fcb3c-103">Invisible, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="fcb3c-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="fcb3c-104">Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="fcb3c-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="fcb3c-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="fcb3c-105">**Value**</span></span>|<span data-ttu-id="fcb3c-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="fcb3c-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcb3c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="fcb3c-107">TRUE</span></span>  <br/> |<span data-ttu-id="fcb3c-108">Le lien hypertexte n'apparaît pas comme un élément de menu dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="fcb3c-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="fcb3c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="fcb3c-109">FALSE</span></span>  <br/> |<span data-ttu-id="fcb3c-110">Le lien hypertexte apparaît comme un élément de menu dans le menu contextuel (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="fcb3c-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcb3c-111">Note</span><span class="sxs-lookup"><span data-stu-id="fcb3c-111">Remarks</span></span>

<span data-ttu-id="fcb3c-112">Pour obtenir une référence à la cellule Invisible par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="fcb3c-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcb3c-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fcb3c-113">Cell name:</span></span>  <br/> |<span data-ttu-id="fcb3c-114">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="fcb3c-114">Hyperlink.</span></span> <span data-ttu-id="fcb3c-115">*nom* . Invisible, où le lien hypertexte *.name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="fcb3c-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="fcb3c-116">Pour obtenir une référence à la cellule Invisible par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="fcb3c-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="fcb3c-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="fcb3c-117">Section index:</span></span>  <br/> |<span data-ttu-id="fcb3c-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="fcb3c-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="fcb3c-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="fcb3c-119">Row index:</span></span>  <br/> |<span data-ttu-id="fcb3c-120">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="fcb3c-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="fcb3c-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="fcb3c-121">Cell index:</span></span>  <br/> |<span data-ttu-id="fcb3c-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="fcb3c-122">**visHLinkInvisible**</span></span> <br/> |
   

