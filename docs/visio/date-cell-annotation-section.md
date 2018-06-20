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
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788427"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="12610-103">Date, cellule (section Annotation)</span><span class="sxs-lookup"><span data-stu-id="12610-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="12610-104">Contient la date et l'heure du dernier commentaire modifié.</span><span class="sxs-lookup"><span data-stu-id="12610-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="12610-105">Cette cellule est utilisée pour le suivi des commentaires uniquement lors de l’ouverture d’un fichier .vsd dans Microsoft Visio 2013 ou lors de l’enregistrement d’un fichier .vsdx au format de fichier .vsd.</span><span class="sxs-lookup"><span data-stu-id="12610-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="12610-106">Il n’est pas utilisé pour le suivi des commentaires dans des documents .vsdx dans Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="12610-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="12610-107">Remarques</span><span class="sxs-lookup"><span data-stu-id="12610-107">Remarks</span></span>

<span data-ttu-id="12610-108">Seule la date apparaît dans la zone de commentaires dans l'interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="12610-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="12610-109">Pour obtenir une référence à la cellule Date par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="12610-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12610-110">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="12610-110">Cell name:</span></span>  <br/> | <span data-ttu-id="12610-111">Annotation.Date [ *i* ] où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="12610-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="12610-112">Pour obtenir une référence à la cellule Date par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="12610-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="12610-113">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="12610-113">Section index:</span></span>  <br/> |<span data-ttu-id="12610-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="12610-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="12610-115">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="12610-115">Row index:</span></span>  <br/> |<span data-ttu-id="12610-116">**visRowAnnotation** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="12610-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="12610-117">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="12610-117">Cell index:</span></span>  <br/> |<span data-ttu-id="12610-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="12610-118">**visAnnotationDate**</span></span> <br/> |
   

