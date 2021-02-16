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
ms.openlocfilehash: b52da8244bf31e75bacbb6f24f73eba6ee8c6e5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404630"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="18b46-103">Invisible, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="18b46-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="18b46-104">Indique si un lien hypertexte apparaît dans le menu contextuel pour une forme ou une page.</span><span class="sxs-lookup"><span data-stu-id="18b46-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="18b46-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="18b46-105">**Value**</span></span>|<span data-ttu-id="18b46-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="18b46-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="18b46-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="18b46-107">TRUE</span></span>  <br/> |<span data-ttu-id="18b46-108">Le lien hypertexte n'apparaît pas comme un élément de menu dans le menu contextuel.</span><span class="sxs-lookup"><span data-stu-id="18b46-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="18b46-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="18b46-109">FALSE</span></span>  <br/> |<span data-ttu-id="18b46-110">Le lien hypertexte apparaît comme un élément de menu dans le menu contextuel (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="18b46-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18b46-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="18b46-111">Remarks</span></span>

<span data-ttu-id="18b46-112">Pour obtenir une référence à la cellule Invisible par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="18b46-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18b46-113">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="18b46-113">Cell name:</span></span>  <br/> |<span data-ttu-id="18b46-114">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="18b46-114">Hyperlink.</span></span> <span data-ttu-id="18b46-115">*nom*  . Invisible où Hyperlink  *.name*  est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="18b46-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="18b46-116">Pour obtenir une référence à la cellule Invisible à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="18b46-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18b46-117">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="18b46-117">Section index:</span></span>  <br/> |<span data-ttu-id="18b46-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="18b46-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="18b46-119">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="18b46-119">Row index:</span></span>  <br/> |<span data-ttu-id="18b46-120">**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="18b46-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="18b46-121">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="18b46-121">Cell index:</span></span>  <br/> |<span data-ttu-id="18b46-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="18b46-122">**visHLinkInvisible**</span></span> <br/> |
   

