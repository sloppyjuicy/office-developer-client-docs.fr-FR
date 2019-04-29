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
description: Représente la coordonnée x d'un point de connexion en coordonnées locales.
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436782"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="6d63b-103">X, cellule (section Connection Points)</span><span class="sxs-lookup"><span data-stu-id="6d63b-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="6d63b-104">Représente la coordonnée *x* d'un point de connexion en coordonnées locales.</span><span class="sxs-lookup"><span data-stu-id="6d63b-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6d63b-105">Remarques</span><span class="sxs-lookup"><span data-stu-id="6d63b-105">Remarks</span></span>

<span data-ttu-id="6d63b-106">Pour obtenir une référence à la cellule X à l'aide d'un nom à partir d'une autre formule ou programme en faisant appel à la propriété **CellsU**, utilisez :</span><span class="sxs-lookup"><span data-stu-id="6d63b-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d63b-107">Nom de cellule :</span><span class="sxs-lookup"><span data-stu-id="6d63b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="6d63b-108">Connections. X *i* = <1>, 2, 3... \*\*</span><span class="sxs-lookup"><span data-stu-id="6d63b-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6d63b-109">Pour obtenir une référence à la cellule X à l'aide d'un index à partir d'un programme, utilisez la propriété **CellsSRC** avec les arguments suivants :</span><span class="sxs-lookup"><span data-stu-id="6d63b-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6d63b-110">Index de la section :</span><span class="sxs-lookup"><span data-stu-id="6d63b-110">Section index:</span></span>  <br/> |<span data-ttu-id="6d63b-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="6d63b-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="6d63b-112">Index de la ligne :</span><span class="sxs-lookup"><span data-stu-id="6d63b-112">Row index:</span></span>  <br/> |<span data-ttu-id="6d63b-113">**visRowConnectionPts** +  *i* où *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6d63b-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6d63b-114">Index de la cellule :</span><span class="sxs-lookup"><span data-stu-id="6d63b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="6d63b-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="6d63b-115">**visX**</span></span> <br/> |
   

