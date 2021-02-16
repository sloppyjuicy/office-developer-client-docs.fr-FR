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
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426505"
---
# <a name="previewscope-cell-document-properties-section"></a><span data-ttu-id="aba70-104">PreviewScope, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="aba70-104">PreviewScope Cell (Document Properties Section)</span></span>

<span data-ttu-id="aba70-p102">Détermine si le dessin inclut un aperçu. Si c'est le cas, cette cellule détermine également si l'aperçu ne représente que la première page du dessin ou toutes ses pages.</span><span class="sxs-lookup"><span data-stu-id="aba70-p102">Determines whether your drawing includes a preview. If your drawing does include a preview, it determines whether the preview shows the first page only or all of the pages in the drawing.</span></span>
  
|<span data-ttu-id="aba70-107">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="aba70-107">**Value**</span></span>|<span data-ttu-id="aba70-108">**Portée de l'aperçu**</span><span class="sxs-lookup"><span data-stu-id="aba70-108">**Preview scope**</span></span>|<span data-ttu-id="aba70-109">**Constante d'automation**</span><span class="sxs-lookup"><span data-stu-id="aba70-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="aba70-110">0</span><span class="sxs-lookup"><span data-stu-id="aba70-110">0</span></span>  <br/> | <span data-ttu-id="aba70-111">Première page</span><span class="sxs-lookup"><span data-stu-id="aba70-111">First page</span></span>  <br/> |<span data-ttu-id="aba70-112">**visDocPreviewScope1stPage**</span><span class="sxs-lookup"><span data-stu-id="aba70-112">**visDocPreviewScope1stPage**</span></span> <br/> |
| <span data-ttu-id="aba70-113">1 </span><span class="sxs-lookup"><span data-stu-id="aba70-113">1</span></span>  <br/> | <span data-ttu-id="aba70-114">Aucun</span><span class="sxs-lookup"><span data-stu-id="aba70-114">None</span></span>  <br/> |<span data-ttu-id="aba70-115">**visDocPreviewScopeNone**</span><span class="sxs-lookup"><span data-stu-id="aba70-115">**visDocPreviewScopeNone**</span></span> <br/> |
| <span data-ttu-id="aba70-116">2 </span><span class="sxs-lookup"><span data-stu-id="aba70-116">2</span></span>  <br/> | <span data-ttu-id="aba70-117">Toutes les pages</span><span class="sxs-lookup"><span data-stu-id="aba70-117">All pages</span></span>  <br/> |<span data-ttu-id="aba70-118">**visDocPreviewScopeAllPages**</span><span class="sxs-lookup"><span data-stu-id="aba70-118">**visDocPreviewScopeAllPages**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aba70-119">Remarques</span><span class="sxs-lookup"><span data-stu-id="aba70-119">Remarks</span></span>

<span data-ttu-id="aba70-120">Vous pouvez également définir  cette valeur sous  l’onglet Résumé dans la  boîte de dialogue Propriétés (cliquez sur le bouton **Office,** sur l’onglet Informations, sur Propriétés du **document,** puis sur Propriétés **avancées).**</span><span class="sxs-lookup"><span data-stu-id="aba70-120">You can also set this value on the **Summary** tab in the **Properties** dialog box (click the **Office** button, click the **Info** tab, click **Document Properties**, and then click **Advanced Properties**).</span></span>
  
<span data-ttu-id="aba70-121">Pour obtenir une référence à la cellule PreviewScope par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="aba70-121">To get a reference to the PreviewScope cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aba70-122">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aba70-122">Cell name:</span></span>  <br/> | <span data-ttu-id="aba70-123">PreviewScope</span><span class="sxs-lookup"><span data-stu-id="aba70-123">PreviewScope</span></span>  <br/> |
   
<span data-ttu-id="aba70-124">Pour obtenir une référence à la cellule PreviewScope à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="aba70-124">To get a reference to the PreviewScope cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aba70-125">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="aba70-125">Section index:</span></span>  <br/> |<span data-ttu-id="aba70-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aba70-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aba70-127">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="aba70-127">Row index:</span></span>  <br/> |<span data-ttu-id="aba70-128">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="aba70-128">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="aba70-129">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="aba70-129">Cell index:</span></span>  <br/> |<span data-ttu-id="aba70-130">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="aba70-130">**visDocPreviewScope**</span></span> <br/> |
   

