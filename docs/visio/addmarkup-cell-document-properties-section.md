---
title: AddMarkup, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030801
localization_priority: Normal
ms.assetid: 46146424-b4c9-2240-36c0-19bb35ec51d1
description: Indique si le document est en révision pour marque de révision.
ms.openlocfilehash: 4e0860639b0d89fce2c35a8947bd5ac00fcc63e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427632"
---
# <a name="addmarkup-cell-document-properties-section"></a><span data-ttu-id="a8c1a-103">AddMarkup, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="a8c1a-103">AddMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="a8c1a-104">Indique si le document est en révision pour marque de révision.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-104">Indicates whether the document is being reviewed for markup.</span></span>
  
|<span data-ttu-id="a8c1a-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="a8c1a-105">**Value**</span></span>|<span data-ttu-id="a8c1a-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="a8c1a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8c1a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a8c1a-107">TRUE</span></span>  <br/> |<span data-ttu-id="a8c1a-108">Document en révision.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-108">Document is being reviewed.</span></span>  <br/> |
|<span data-ttu-id="a8c1a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a8c1a-109">FALSE</span></span>  <br/> |<span data-ttu-id="a8c1a-110">Document pas en révision (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="a8c1a-110">Document is not being reviewed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a8c1a-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="a8c1a-111">Remarks</span></span>

<span data-ttu-id="a8c1a-112">Lorsque la cellule AddMarkup est définie sur TRUE, le réviseur ajoute une marque de révision et des modifications sont apportées pour marquer les pages qui se superposent, pas les pages de dessin d'origine.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-112">When the AddMarkup cell is set to TRUE, the reviewer is adding markup and changes are applied to markup overlay pages, not to original drawing pages.</span></span> <span data-ttu-id="a8c1a-113">Lorsque la cellule AddMarkup est définie sur FALSE, le suivi des révisions est désactivé et les modifications sont appliquées aux pages de dessin d'origine.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-113">When the AddMarkup cell is FALSE, markup tracking is off and changes are applied to the original drawing pages.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a8c1a-114">Vous pouvez empêcher le markup sur vos documents à l’aide de la fonction GUARD.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-114">You can prevent markup on your documents by using the GUARD function.</span></span> <span data-ttu-id="a8c1a-115">Si la cellule AddMarkup contient la formule =GUARD(FALSE), la commande **De** suivi est désactivée.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-115">If the AddMarkup cell contains the formula =GUARD(FALSE), the **Track Markup** command is disabled.</span></span> 
  
<span data-ttu-id="a8c1a-116">Ce paramètre correspond à la commande **Suivi des révisions** dans le groupe **Marque de révision** de l’onglet **Révision**.</span><span class="sxs-lookup"><span data-stu-id="a8c1a-116">This setting corresponds to the **Track Markup** command setting in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="a8c1a-117">Pour obtenir une référence à la cellule AddMarkup par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="a8c1a-117">To get a reference to the AddMarkup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c1a-118">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="a8c1a-118">Cell name:</span></span>  <br/> |<span data-ttu-id="a8c1a-119">AddMarkup</span><span class="sxs-lookup"><span data-stu-id="a8c1a-119">AddMarkup</span></span>  <br/> |
   
<span data-ttu-id="a8c1a-120">Pour obtenir une référence à la cellule AddMarkup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="a8c1a-120">To get a reference to the AddMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8c1a-121">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="a8c1a-121">Section index:</span></span>  <br/> |<span data-ttu-id="a8c1a-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a8c1a-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a8c1a-123">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="a8c1a-123">Row index:</span></span>  <br/> |<span data-ttu-id="a8c1a-124">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="a8c1a-124">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="a8c1a-125">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="a8c1a-125">Cell index:</span></span>  <br/> |<span data-ttu-id="a8c1a-126">**visDocAddMarkup**</span><span class="sxs-lookup"><span data-stu-id="a8c1a-126">**visDocAddMarkup**</span></span> <br/> |
   

