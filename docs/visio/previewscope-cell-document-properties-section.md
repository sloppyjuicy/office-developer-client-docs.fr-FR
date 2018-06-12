---
title: PreviewScope, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.
ms.openlocfilehash: 865da052f710481c146d3c2692ddf506018be789
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789344"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="c219c-104">PreviewScope, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="c219c-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="c219c-p102">Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.</span><span class="sxs-lookup"><span data-stu-id="c219c-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="c219c-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="c219c-107">**Value**</span></span>|<span data-ttu-id="c219c-108">**Portée de l’aperçu**</span><span class="sxs-lookup"><span data-stu-id="c219c-108">**Preview scope**</span></span>|<span data-ttu-id="c219c-109">**Constante d’Automation**</span><span class="sxs-lookup"><span data-stu-id="c219c-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c219c-110">0</span><span class="sxs-lookup"><span data-stu-id="c219c-110">0</span></span>  <br/> | <span data-ttu-id="c219c-111">Première page</span><span class="sxs-lookup"><span data-stu-id="c219c-111">First page</span></span>  <br/> |<span data-ttu-id="c219c-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="c219c-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="c219c-113">1</span><span class="sxs-lookup"><span data-stu-id="c219c-113">1</span></span>  <br/> | <span data-ttu-id="c219c-114">Aucune</span><span class="sxs-lookup"><span data-stu-id="c219c-114">None</span></span>  <br/> |<span data-ttu-id="c219c-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="c219c-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="c219c-116">2</span><span class="sxs-lookup"><span data-stu-id="c219c-116">2</span></span>  <br/> | <span data-ttu-id="c219c-117">Toutes les pages</span><span class="sxs-lookup"><span data-stu-id="c219c-117">All pages</span></span>  <br/> |<span data-ttu-id="c219c-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="c219c-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c219c-119">Note</span><span class="sxs-lookup"><span data-stu-id="c219c-119">Remarks</span></span>

<span data-ttu-id="c219c-120">Vous pouvez également définir cette valeur sur l’onglet **Résumé** de la boîte de dialogue **Propriétés** (cliquez sur le bouton **Office** , cliquez sur l’onglet **Infos** , cliquez sur **Propriétés du Document**, puis cliquez sur **Propriétés avancées**).</span><span class="sxs-lookup"><span data-stu-id="c219c-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="c219c-121">Pour obtenir une référence à la cellule PreviewScope par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="c219c-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c219c-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c219c-122">Cell name:</span></span>  <br/> | <span data-ttu-id="c219c-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="c219c-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="c219c-124">Pour obtenir une référence à la cellule PreviewScope par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="c219c-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c219c-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="c219c-125">Section index:</span></span>  <br/> |<span data-ttu-id="c219c-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c219c-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c219c-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="c219c-127">Row index:</span></span>  <br/> |<span data-ttu-id="c219c-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="c219c-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="c219c-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="c219c-129">Cell index:</span></span>  <br/> |<span data-ttu-id="c219c-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="c219c-130">**visDocPreviewScope**</span></span> <br/> |
   

