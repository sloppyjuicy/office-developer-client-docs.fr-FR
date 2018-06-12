---
title: GETVAL, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251885
localization_priority: Normal
ms.assetid: 1da42991-5791-ebab-84cc-286cfe984a61
description: Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de cellule est modifiée.
ms.openlocfilehash: b4c8ea14b7184101a360c9f5ee4af03fd178aa6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788718"
---
# <a name="getval-function"></a><span data-ttu-id="aa5c5-103">GETVAL, fonction</span><span class="sxs-lookup"><span data-stu-id="aa5c5-103">GETVAL Function</span></span>

<span data-ttu-id="aa5c5-104">Obtient la valeur d’une cellule et ne recalcule pas la formule lorsque la valeur de cellule est modifiée.</span><span class="sxs-lookup"><span data-stu-id="aa5c5-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aa5c5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aa5c5-105">Syntax</span></span>

<span data-ttu-id="aa5c5-106">GETVAL (** *cellname* **)</span><span class="sxs-lookup"><span data-stu-id="aa5c5-106">GETVAL(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aa5c5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="aa5c5-107">Parameters</span></span>

|<span data-ttu-id="aa5c5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="aa5c5-108">**Name**</span></span>|<span data-ttu-id="aa5c5-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="aa5c5-109">**Required/Optional**</span></span>|<span data-ttu-id="aa5c5-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="aa5c5-110">**Data Type**</span></span>|<span data-ttu-id="aa5c5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="aa5c5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aa5c5-112">_cellName_</span><span class="sxs-lookup"><span data-stu-id="aa5c5-112">_cellname_</span></span> <br/> |<span data-ttu-id="aa5c5-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="aa5c5-113">Required</span></span>  <br/> |<span data-ttu-id="aa5c5-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="aa5c5-114">**String**</span></span> <br/> |<span data-ttu-id="aa5c5-115">Nom de la cellule dont la valeur doit être obtenue.</span><span class="sxs-lookup"><span data-stu-id="aa5c5-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="aa5c5-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="aa5c5-116">Example</span></span>

<span data-ttu-id="aa5c5-117">GETVAL(PinX) + GETVAL(VY) + Width</span><span class="sxs-lookup"><span data-stu-id="aa5c5-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="aa5c5-118">Renvoie la somme des valeurs des cellules PinX, PinY et Width.</span><span class="sxs-lookup"><span data-stu-id="aa5c5-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

