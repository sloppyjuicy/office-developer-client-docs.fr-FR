---
title: X, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: Coordonnée x de la marque de commentaire en coordonnées de page.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434479"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="1252d-103">X, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="1252d-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="1252d-104">Coordonnée  *x*  de la marque de commentaire en coordonnées de page.</span><span class="sxs-lookup"><span data-stu-id="1252d-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="1252d-105">Cette cellule est utilisée pour suivre les commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd.</span><span class="sxs-lookup"><span data-stu-id="1252d-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="1252d-106">Il n’est pas utilisé pour le suivi des commentaires dans les documents .vsdx Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="1252d-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1252d-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="1252d-107">Remarks</span></span>

<span data-ttu-id="1252d-108">Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="1252d-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1252d-109">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="1252d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1252d-110">Annotation.X[  *i*  ] où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1252d-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1252d-111">Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1252d-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1252d-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1252d-112">Section index:</span></span>  <br/> |<span data-ttu-id="1252d-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="1252d-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="1252d-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1252d-114">Row index:</span></span>  <br/> |<span data-ttu-id="1252d-115">**visRowAnnotation**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1252d-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1252d-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1252d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1252d-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="1252d-117">**visAnnotationX**</span></span> <br/> |
   

