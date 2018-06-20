---
title: Y, cellule (section Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Représente la valeur y-coordonnées d’un point de connexion dans le système de coordonnées local.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790065"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="1735f-103">Y, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="1735f-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="1735f-104">Représente la valeur *y* -coordonnées d’un point de connexion dans le système de coordonnées local.</span><span class="sxs-lookup"><span data-stu-id="1735f-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1735f-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="1735f-105">Remarks</span></span>

<span data-ttu-id="1735f-106">Pour obtenir une référence à la cellule Y par un nom à partir d’une autre formule ou d’un programme à la propriété **CellsU** , utilisez :</span><span class="sxs-lookup"><span data-stu-id="1735f-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1735f-107">Nom de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1735f-107">Cell name:</span></span>  <br/> | <span data-ttu-id="1735f-108">Connections.Y *i* où *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1735f-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1735f-109">Pour obtenir une référence à la cellule Y par index dans un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="1735f-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1735f-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="1735f-110">Section index:</span></span>  <br/> |<span data-ttu-id="1735f-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="1735f-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="1735f-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="1735f-112">Row index:</span></span>  <br/> |<span data-ttu-id="1735f-113">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1735f-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1735f-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="1735f-114">Cell index:</span></span>  <br/> |<span data-ttu-id="1735f-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="1735f-115">**visY**</span></span> <br/> |
   

