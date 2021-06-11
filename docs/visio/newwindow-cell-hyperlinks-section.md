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
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342230"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="812e1-103">NewWindow, cellule (section Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="812e1-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="812e1-104">Définit si le lien hypertexte doit être ouvert dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="812e1-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="812e1-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="812e1-105">**Value**</span></span>|<span data-ttu-id="812e1-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="812e1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="812e1-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="812e1-107">TRUE</span></span>  <br/> | <span data-ttu-id="812e1-108">Ouvrez la page liée, le document ou le site web dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="812e1-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="812e1-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="812e1-109">FALSE</span></span>  <br/> | <span data-ttu-id="812e1-p101">Valeur par défaut. Le lien hypertexte n'est pas ouvert dans une nouvelle fenêtre.</span><span class="sxs-lookup"><span data-stu-id="812e1-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="812e1-112">Remarques</span><span class="sxs-lookup"><span data-stu-id="812e1-112">Remarks</span></span>

<span data-ttu-id="812e1-113">Pour obtenir une référence à la cellule NewWindow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="812e1-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="812e1-114">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="812e1-114">Cell name:</span></span>  <br/> | <span data-ttu-id="812e1-115">Lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="812e1-115">Hyperlink.</span></span>  <span data-ttu-id="812e1-116">*Nom*  . NewWindow où Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="812e1-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="812e1-117">*Le nom*  est le nom de la ligne</span><span class="sxs-lookup"><span data-stu-id="812e1-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="812e1-118">Pour obtenir une référence à la cellule NewWindow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="812e1-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="812e1-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="812e1-119">Section index:</span></span>  <br/> |<span data-ttu-id="812e1-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="812e1-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="812e1-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="812e1-121">Row index:</span></span>  <br/> |<span data-ttu-id="812e1-122">**visRow1stHyperlink**  +   *i* où *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="812e1-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="812e1-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="812e1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="812e1-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="812e1-124">**visHLinkNewWin**</span></span> <br/> |
   

