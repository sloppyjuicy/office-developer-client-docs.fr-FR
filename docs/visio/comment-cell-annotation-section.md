---
title: Comment, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contient le texte qui apparaît dans un commentaire.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359037"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="d2005-103">Comment, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="d2005-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="d2005-104">Contient le texte qui apparaît dans un commentaire.</span><span class="sxs-lookup"><span data-stu-id="d2005-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="d2005-105">Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l'ouverture d'un fichier. VSD dans Microsoft Visio 2013 ou lors de l'enregistrement d'un fichier. vsdx au format de fichier. VSD.</span><span class="sxs-lookup"><span data-stu-id="d2005-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="d2005-106">Il n'est pas utilisé pour suivre les commentaires dans les documents. vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d2005-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2005-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="d2005-107">Remarks</span></span>

<span data-ttu-id="d2005-108">Pour obtenir une référence à la cellule Comment par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="d2005-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2005-109">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2005-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d2005-110">Annotation. Comment [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d2005-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d2005-111">Pour obtenir une référence à la cellule Comment à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="d2005-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2005-112">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="d2005-112">Section index:</span></span>  <br/> |<span data-ttu-id="d2005-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="d2005-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="d2005-114">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="d2005-114">Row index:</span></span>  <br/> |<span data-ttu-id="d2005-115">**visRowAnnotation** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d2005-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d2005-116">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="d2005-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d2005-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="d2005-117">**visAnnotationComment**</span></span> <br/> |
   

