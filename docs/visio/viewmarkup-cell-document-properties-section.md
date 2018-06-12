---
title: ViewMarkup, cellule (section Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: Détermine si les marques de révision apparaissent dans la fenêtre de dessin.
ms.openlocfilehash: dda908595b243878ec755cf73351ec1fd672dc55
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790026"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="40d45-103">ViewMarkup, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="40d45-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="40d45-104">Détermine si les marques de révision apparaissent dans la fenêtre de dessin.</span><span class="sxs-lookup"><span data-stu-id="40d45-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="40d45-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="40d45-105">**Value**</span></span>|<span data-ttu-id="40d45-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="40d45-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40d45-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="40d45-107">TRUE</span></span>  <br/> |<span data-ttu-id="40d45-108">La marque de révision est affichée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="40d45-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="40d45-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="40d45-109">FALSE</span></span>  <br/> |<span data-ttu-id="40d45-110">La marque de révision n'est pas affichée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="40d45-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40d45-111">Note</span><span class="sxs-lookup"><span data-stu-id="40d45-111">Remarks</span></span>

 <span data-ttu-id="40d45-112">Lorsque le suivi des révisions sont activée (cellule AddMarkup a la valeur TRUE), la cellule ViewMarkup est automatiquement définie sur TRUE et conserve la valeur TRUE même une fois que le suivi des révisions a été désactivée (cellule AddMarkup a la valeur FALSE).</span><span class="sxs-lookup"><span data-stu-id="40d45-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="40d45-113">La valeur de la cellule ViewMarkup est ignorée lorsque la cellule AddMarkup est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="40d45-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="40d45-114">La cellule ViewMarkup est également définie sur TRUE lorsque les commentaires sont insérés dans un dessin (que le suivi des révisions soit activé ou non). Elle doit être également définie sur TRUE pour afficher les commentaires dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="40d45-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="40d45-115">Cette cellule correspond à la commande **Afficher les marques** dans le groupe de **balisage** sous l’onglet **révision** .</span><span class="sxs-lookup"><span data-stu-id="40d45-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="40d45-116">Pour obtenir une référence à la cellule ViewMarkup par un nom à partir d’une autre formule ou d’un programme en faisant appel à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="40d45-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40d45-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40d45-117">Cell name:</span></span>  <br/> |<span data-ttu-id="40d45-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="40d45-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="40d45-119">Pour obtenir une référence à la cellule ViewMarkup par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="40d45-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40d45-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="40d45-120">Section index:</span></span>  <br/> |<span data-ttu-id="40d45-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40d45-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="40d45-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="40d45-122">Row index:</span></span>  <br/> |<span data-ttu-id="40d45-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="40d45-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="40d45-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="40d45-124">Cell index:</span></span>  <br/> |<span data-ttu-id="40d45-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="40d45-125">**visDocViewMarkup**</span></span> <br/> |
   

