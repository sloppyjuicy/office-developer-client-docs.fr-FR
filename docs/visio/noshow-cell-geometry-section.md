---
title: NoShow, cellule (section Geometry)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: Indique si un chemin est affiché sur la page de dessin.
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410349"
---
# <a name="noshow-cell-geometry-section"></a><span data-ttu-id="53001-103">NoShow, cellule (section Geometry)</span><span class="sxs-lookup"><span data-stu-id="53001-103">NoShow Cell (Geometry Section)</span></span>

<span data-ttu-id="53001-104">Indique si un chemin est affiché sur la page de dessin.</span><span class="sxs-lookup"><span data-stu-id="53001-104">Indicates whether a path is displayed on the drawing page.</span></span>
  
|<span data-ttu-id="53001-105">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="53001-105">**Value**</span></span>|<span data-ttu-id="53001-106">**Description**</span><span class="sxs-lookup"><span data-stu-id="53001-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="53001-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="53001-107">TRUE</span></span>  <br/> | <span data-ttu-id="53001-108">Le trait et le remplissage du chemin représentés par cette section sont masqués.</span><span class="sxs-lookup"><span data-stu-id="53001-108">The stroke and fill of the path represented by the section is hidden.</span></span>  <br/> |
| <span data-ttu-id="53001-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="53001-109">FALSE</span></span>  <br/> | <span data-ttu-id="53001-110">Le trait et le remplissage du chemin sont affichés.</span><span class="sxs-lookup"><span data-stu-id="53001-110">The stroke and fill of the path is shown.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53001-111">Remarques</span><span class="sxs-lookup"><span data-stu-id="53001-111">Remarks</span></span>

<span data-ttu-id="53001-112">Pour obtenir une référence à la cellule NoShow par un nom à partir d'une autre formule ou d'un programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="53001-112">To get a reference to the NoShow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53001-113">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="53001-113">Cell name:</span></span>  <br/> | <span data-ttu-id="53001-114">Geometry  *i*  . NoShow où  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="53001-114">Geometry  *i*  .NoShow            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="53001-115">Pour obtenir une référence à la cellule NoShow à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="53001-115">To get a reference to the NoShow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="53001-116">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="53001-116">Section index:</span></span>  <br/> |<span data-ttu-id="53001-117">**visSectionFirstComponent**  +   *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="53001-117">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="53001-118">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="53001-118">Row index:</span></span>  <br/> |<span data-ttu-id="53001-119">**visRowComponent**</span><span class="sxs-lookup"><span data-stu-id="53001-119">**visRowComponent**</span></span> <br/> |
| <span data-ttu-id="53001-120">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="53001-120">Cell index:</span></span>  <br/> |<span data-ttu-id="53001-121">**visCompNoShow**</span><span class="sxs-lookup"><span data-stu-id="53001-121">**visCompNoShow**</span></span> <br/> |
   

