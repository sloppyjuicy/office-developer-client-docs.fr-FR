---
title: Date, cellule (section Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contient la date et l'heure du dernier commentaire modifié.
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360339"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="33599-103">Date, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="33599-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="33599-104">Contient la date et l'heure du dernier commentaire modifié.</span><span class="sxs-lookup"><span data-stu-id="33599-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="33599-105">Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l'ouverture d'un fichier. VSD dans Microsoft Visio 2013 ou lors de l'enregistrement d'un fichier. vsdx au format de fichier. VSD.</span><span class="sxs-lookup"><span data-stu-id="33599-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="33599-106">Il n'est pas utilisé pour suivre les commentaires dans les documents. vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="33599-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="33599-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="33599-107">Remarks</span></span>

<span data-ttu-id="33599-108">Seule la date apparaît dans la zone de commentaires dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="33599-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="33599-109">Pour obtenir une référence à la cellule Date par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="33599-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33599-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33599-110">Cell name:</span></span>  <br/> | <span data-ttu-id="33599-111">Annotation. date [ *i* ] où *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="33599-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="33599-112">Pour obtenir une référence à la cellule Date à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="33599-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33599-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="33599-113">Section index:</span></span>  <br/> |<span data-ttu-id="33599-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="33599-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="33599-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="33599-115">Row index:</span></span>  <br/> |<span data-ttu-id="33599-116">**visRowAnnotation** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="33599-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="33599-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="33599-117">Cell index:</span></span>  <br/> |<span data-ttu-id="33599-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="33599-118">**visAnnotationDate**</span></span> <br/> |
   

