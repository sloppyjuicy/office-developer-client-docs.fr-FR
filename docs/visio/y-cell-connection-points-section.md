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
description: Représente la coordonnée y d'un point de connexion en coordonnées locales.
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410846"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="b7196-103">Y, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="b7196-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="b7196-104">Représente la coordonnée *y* d'un point de connexion en coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="b7196-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b7196-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="b7196-105">Remarks</span></span>

<span data-ttu-id="b7196-106">Pour obtenir une référence à la cellule Y à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="b7196-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7196-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="b7196-107">Cell name:</span></span>  <br/> | <span data-ttu-id="b7196-108">Connections. Y *i i* = <1>, 2, 3... \*\*</span><span class="sxs-lookup"><span data-stu-id="b7196-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b7196-109">Pour obtenir une référence à la cellule Y à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="b7196-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b7196-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="b7196-110">Section index:</span></span>  <br/> |<span data-ttu-id="b7196-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="b7196-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="b7196-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="b7196-112">Row index:</span></span>  <br/> |<span data-ttu-id="b7196-113">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b7196-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b7196-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="b7196-114">Cell index:</span></span>  <br/> |<span data-ttu-id="b7196-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="b7196-115">**visY**</span></span> <br/> |
   

