---
title: NewWindow, cellule (section Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789165"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="62220-103">NewWindow, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="62220-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="62220-104">Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="62220-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="62220-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="62220-105">**Value**</span></span>|<span data-ttu-id="62220-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="62220-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="62220-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="62220-107">TRUE</span></span>  <br/> | <span data-ttu-id="62220-108">La page, le document ou le site Web est ouvert dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="62220-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="62220-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="62220-109">FALSE</span></span>  <br/> | <span data-ttu-id="62220-p101">Valeur par défaut. Le lien hypertexte n'est pas ouvert dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="62220-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62220-112">Note</span><span class="sxs-lookup"><span data-stu-id="62220-112">Remarks</span></span>

<span data-ttu-id="62220-113">Pour obtenir une référence à la cellule NewWindow par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="62220-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62220-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="62220-114">Cell name:</span></span>  <br/> | <span data-ttu-id="62220-115">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="62220-115">Hyperlink.</span></span>  <span data-ttu-id="62220-116">*Nom* . NewWindow où un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="62220-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="62220-117">*Name* est le nom de ligne</span><span class="sxs-lookup"><span data-stu-id="62220-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="62220-118">Pour obtenir une référence à la cellule NewWindow par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="62220-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62220-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="62220-119">Section index:</span></span>  <br/> |<span data-ttu-id="62220-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="62220-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="62220-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="62220-121">Row index:</span></span>  <br/> |<span data-ttu-id="62220-122">**visRow1stHyperlink** +  *i* où *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="62220-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="62220-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="62220-123">Cell index:</span></span>  <br/> |<span data-ttu-id="62220-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="62220-124">**visHLinkNewWin**</span></span> <br/> |
   

