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
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416404"
---
# <a name="viewmarkup-cell-document-properties-section"></a><span data-ttu-id="37353-103">ViewMarkup, cellule (section Document Properties)</span><span class="sxs-lookup"><span data-stu-id="37353-103">ViewMarkup Cell (Document Properties Section)</span></span>

<span data-ttu-id="37353-104">Détermine si les marques de révision apparaissent dans la fenêtre de dessin.</span><span class="sxs-lookup"><span data-stu-id="37353-104">Determines whether markup appears in the drawing window.</span></span> 
  
|<span data-ttu-id="37353-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="37353-105">**Value**</span></span>|<span data-ttu-id="37353-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="37353-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="37353-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="37353-107">TRUE</span></span>  <br/> |<span data-ttu-id="37353-108">La marque de révision est affichée dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="37353-108">Markup is displayed on the drawing.</span></span>  <br/> |
|<span data-ttu-id="37353-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="37353-109">FALSE</span></span>  <br/> |<span data-ttu-id="37353-110">La marque de révision n'est pas affichée (valeur par défaut).</span><span class="sxs-lookup"><span data-stu-id="37353-110">Markup is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="37353-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="37353-111">Remarks</span></span>

 <span data-ttu-id="37353-112">Lorsque le suivi des modifications est activé (la cellule AddMarkup a la valeur TRUE), la cellule ViewMarkup est automatiquement définie sur TRUE et reste TRUE même si le suivi des révisions a été désactivé (la cellule AddMarkup a la valeur FALSe).</span><span class="sxs-lookup"><span data-stu-id="37353-112">When markup tracking is turned on (AddMarkup cell is TRUE), the ViewMarkup cell is automatically set to TRUE and remains TRUE even after markup tracking has been turned off (AddMarkup cell is FALSE).</span></span> <span data-ttu-id="37353-113">La valeur de la cellule ViewMarkup n'est pas prise en compte lorsque la cellule AddMarkup est définie sur TRUE.</span><span class="sxs-lookup"><span data-stu-id="37353-113">The value in the ViewMarkup cell is ignored when the AddMarkup cell is TRUE.</span></span> 
  
<span data-ttu-id="37353-114">La cellule ViewMarkup est également définie sur TRUE lorsque les commentaires sont insérés dans un dessin (que le suivi des révisions soit activé ou non). Elle doit être également définie sur TRUE pour afficher les commentaires dans le dessin.</span><span class="sxs-lookup"><span data-stu-id="37353-114">The ViewMarkup cell is also set to TRUE when comments are inserted in a drawing (whether or not markup tracking is turned on) and must be TRUE to see comments in the drawing.</span></span>
  
<span data-ttu-id="37353-115">Cette cellule correspond à la commande **Afficher les marques** dans le groupe **Marques** de l’onglet **Révision**.</span><span class="sxs-lookup"><span data-stu-id="37353-115">This cell corresponds to the **Show Markup** command in the **Markup** group on the **Review** tab.</span></span> 
  
<span data-ttu-id="37353-116">Pour obtenir une référence à la cellule ViewMarkup par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="37353-116">To get a reference to the ViewMarkup cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37353-117">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="37353-117">Cell name:</span></span>  <br/> |<span data-ttu-id="37353-118">ViewMarkup</span><span class="sxs-lookup"><span data-stu-id="37353-118">ViewMarkup</span></span>  <br/> |
   
<span data-ttu-id="37353-119">Pour obtenir une référence à la cellule ViewMarkup à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="37353-119">To get a reference to the ViewMarkup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="37353-120">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="37353-120">Section index:</span></span>  <br/> |<span data-ttu-id="37353-121">**Définis**</span><span class="sxs-lookup"><span data-stu-id="37353-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="37353-122">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="37353-122">Row index:</span></span>  <br/> |<span data-ttu-id="37353-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="37353-123">**visRowDoc**</span></span> <br/> |
|<span data-ttu-id="37353-124">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="37353-124">Cell index:</span></span>  <br/> |<span data-ttu-id="37353-125">**visDocViewMarkup**</span><span class="sxs-lookup"><span data-stu-id="37353-125">**visDocViewMarkup**</span></span> <br/> |
   

