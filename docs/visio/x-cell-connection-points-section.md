---
title: X, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Représente le x-coordonnées d’un point de connexion dans le système de coordonnées local.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790051"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="46fa6-103">X, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="46fa6-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="46fa6-104">Représente le *x* -coordonnées d’un point de connexion dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="46fa6-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="46fa6-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="46fa6-105">Remarks</span></span>

<span data-ttu-id="46fa6-106">Pour obtenir une référence à la cellule X par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="46fa6-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="46fa6-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="46fa6-107">Cell name:</span></span>  <br/> | <span data-ttu-id="46fa6-108">Connections.X *i* où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="46fa6-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="46fa6-109">Pour obtenir une référence à la cellule X par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="46fa6-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="46fa6-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="46fa6-110">Section index:</span></span>  <br/> |<span data-ttu-id="46fa6-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="46fa6-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="46fa6-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="46fa6-112">Row index:</span></span>  <br/> |<span data-ttu-id="46fa6-113">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="46fa6-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="46fa6-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="46fa6-114">Cell index:</span></span>  <br/> |<span data-ttu-id="46fa6-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="46fa6-115">**visX**</span></span> <br/> |
   

