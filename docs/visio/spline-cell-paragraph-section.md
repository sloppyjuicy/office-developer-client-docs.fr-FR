---
title: SpLine, cellule (section Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm970
localization_priority: Normal
ms.assetid: 84f4e5f1-7c28-9e83-8644-28d117bb10a5
description: Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.
ms.openlocfilehash: 82b2604a62608c0cc4333892d678b1eb886a9c7d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434913"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="d7b45-103">SpLine, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="d7b45-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="d7b45-104">Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="d7b45-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="d7b45-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="d7b45-105">**Value**</span></span>|<span data-ttu-id="d7b45-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="d7b45-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d7b45-107">\>0</span><span class="sxs-lookup"><span data-stu-id="d7b45-107">\>0</span></span>  <br/> | <span data-ttu-id="d7b45-108">Espacement absolu, quelle que soit la taille en points des caractères</span><span class="sxs-lookup"><span data-stu-id="d7b45-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="d7b45-109">=0</span><span class="sxs-lookup"><span data-stu-id="d7b45-109">=0</span></span>  <br/> | <span data-ttu-id="d7b45-110">Total (espacement = 100 % de la taille des caractères)</span><span class="sxs-lookup"><span data-stu-id="d7b45-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="d7b45-111">\<0</span><span class="sxs-lookup"><span data-stu-id="d7b45-111">\<0</span></span>  <br/> | <span data-ttu-id="d7b45-112">Un pourcentage de la taille des caractères (par exemple, -120 % donne un espacement de 120 %)</span><span class="sxs-lookup"><span data-stu-id="d7b45-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d7b45-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="d7b45-113">Remarks</span></span>

<span data-ttu-id="d7b45-114">Pour obtenir une référence à la cellule SpLine par un nom dans une autre formule ou dans un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d7b45-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7b45-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d7b45-115">Cell name:</span></span>  <br/> | <span data-ttu-id="d7b45-116">Para.</span><span class="sxs-lookup"><span data-stu-id="d7b45-116">Para.</span></span> <span data-ttu-id="d7b45-117">SpLine [  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d7b45-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d7b45-118">Pour obtenir une référence à la cellule SpLine dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d7b45-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7b45-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d7b45-119">Section index:</span></span>  <br/> |<span data-ttu-id="d7b45-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="d7b45-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="d7b45-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d7b45-121">Row index:</span></span>  <br/> |<span data-ttu-id="d7b45-122">**visRowParagraph**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7b45-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d7b45-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d7b45-123">Cell index:</span></span>  <br/> |<span data-ttu-id="d7b45-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="d7b45-124">**visSpaceLine**</span></span> <br/> |
   

