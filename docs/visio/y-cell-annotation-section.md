---
title: Y, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Coordonnée y du marqueur de commentaire en coordonnées de page.
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429200"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="cadd8-103">Y, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="cadd8-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="cadd8-104">Coordonnée  *y*  du marqueur de commentaire en coordonnées de page.</span><span class="sxs-lookup"><span data-stu-id="cadd8-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cadd8-105">Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd.</span><span class="sxs-lookup"><span data-stu-id="cadd8-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="cadd8-106">Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="cadd8-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cadd8-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="cadd8-107">Remarks</span></span>

<span data-ttu-id="cadd8-108">Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="cadd8-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cadd8-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="cadd8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="cadd8-110">Annotation.Y [  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="cadd8-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="cadd8-111">Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="cadd8-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cadd8-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="cadd8-112">Section index:</span></span>  <br/> |<span data-ttu-id="cadd8-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="cadd8-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="cadd8-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="cadd8-114">Row index:</span></span>  <br/> |<span data-ttu-id="cadd8-115">**visRowAnnotation**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cadd8-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cadd8-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="cadd8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="cadd8-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="cadd8-117">**visAnnotationY**</span></span> <br/> |
   

