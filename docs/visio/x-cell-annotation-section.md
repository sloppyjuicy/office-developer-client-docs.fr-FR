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
description: Le - coordonnée x de la marque de commentaire en coordonnées de page.
ms.openlocfilehash: 454c28c6f15c705148155751d533a516aae7d2d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790045"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="31277-103">X, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="31277-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="31277-104">*X* -coordonnées de la marque de commentaire en coordonnées de page.</span><span class="sxs-lookup"><span data-stu-id="31277-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="31277-105">Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd.</span><span class="sxs-lookup"><span data-stu-id="31277-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="31277-106">Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="31277-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="31277-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="31277-107">Remarks</span></span>

<span data-ttu-id="31277-108">Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="31277-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31277-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="31277-109">Cell name:</span></span>  <br/> | <span data-ttu-id="31277-110">Annotation.X [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="31277-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="31277-111">Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="31277-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31277-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="31277-112">Section index:</span></span>  <br/> |<span data-ttu-id="31277-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="31277-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="31277-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="31277-114">Row index:</span></span>  <br/> |<span data-ttu-id="31277-115">**visRowAnnotation** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="31277-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="31277-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="31277-116">Cell index:</span></span>  <br/> |<span data-ttu-id="31277-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="31277-117">**visAnnotationX**</span></span> <br/> |
   

