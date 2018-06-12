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
ms.openlocfilehash: f2f290564d49a056bc3366707b25a7991f8c4401
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789795"
---
# <a name="spline-cell-paragraph-section"></a><span data-ttu-id="004a5-103">SpLine, cellule (section Paragraph)</span><span class="sxs-lookup"><span data-stu-id="004a5-103">SpLine Cell (Paragraph Section)</span></span>

<span data-ttu-id="004a5-104">Détermine la distance séparant une ligne de texte de la suivante, exprimée en pourcentage, où 100 % représente la hauteur d'une ligne de texte.</span><span class="sxs-lookup"><span data-stu-id="004a5-104">Determines the distance between one line of text and the next, expressed as a percentage, where 100% is the height of a text line.</span></span>
  
|<span data-ttu-id="004a5-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="004a5-105">**Value**</span></span>|<span data-ttu-id="004a5-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="004a5-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="004a5-107">\>0</span><span class="sxs-lookup"><span data-stu-id="004a5-107">\>0</span></span>  <br/> | <span data-ttu-id="004a5-108">Espacement absolu, quelle que soit la taille en points des caractères</span><span class="sxs-lookup"><span data-stu-id="004a5-108">Absolute spacing, regardless of font size</span></span>  <br/> |
| <span data-ttu-id="004a5-109">=0</span><span class="sxs-lookup"><span data-stu-id="004a5-109">=0</span></span>  <br/> | <span data-ttu-id="004a5-110">Total (espacement = 100 % de la taille des caractères)</span><span class="sxs-lookup"><span data-stu-id="004a5-110">Set solid (spacing = 100% of font size)</span></span>  <br/> |
| <span data-ttu-id="004a5-111">\<0</span><span class="sxs-lookup"><span data-stu-id="004a5-111">\<0</span></span>  <br/> | <span data-ttu-id="004a5-112">Un pourcentage de la taille des caractères (par exemple, -120 % donne un espacement de 120 %)</span><span class="sxs-lookup"><span data-stu-id="004a5-112">A percentage of font size (for example, -120% yields 120% spacing)</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="004a5-113">Note</span><span class="sxs-lookup"><span data-stu-id="004a5-113">Remarks</span></span>

<span data-ttu-id="004a5-114">Pour obtenir une référence à la cellule SpLine par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="004a5-114">To get a reference to the SpLine cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="004a5-115">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="004a5-115">Cell name:</span></span>  <br/> | <span data-ttu-id="004a5-116">Paragraphe.</span><span class="sxs-lookup"><span data-stu-id="004a5-116">Para.</span></span> <span data-ttu-id="004a5-117">SpLine [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="004a5-117">SpLine [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="004a5-118">Pour obtenir une référence à la cellule SpLine par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="004a5-118">To get a reference to the SpLine cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="004a5-119">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="004a5-119">Section index:</span></span>  <br/> |<span data-ttu-id="004a5-120">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="004a5-120">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="004a5-121">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="004a5-121">Row index:</span></span>  <br/> |<span data-ttu-id="004a5-122">**visRowParagraph** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="004a5-122">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="004a5-123">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="004a5-123">Cell index:</span></span>  <br/> |<span data-ttu-id="004a5-124">**visSpaceLine**</span><span class="sxs-lookup"><span data-stu-id="004a5-124">**visSpaceLine**</span></span> <br/> |
   

