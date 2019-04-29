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
description: Obtient la valeur d'une cellule et ne recalcule pas la formule lors de la modification de la valeur de la cellule.
ms.openlocfilehash: 9449ccd8f849b23faf08ee25826301a1b6efe6d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416887"
---
# <a name="getval-function"></a><span data-ttu-id="176e7-103">Fonction GETVAL</span><span class="sxs-lookup"><span data-stu-id="176e7-103">GETVAL Function</span></span>

<span data-ttu-id="176e7-104">Obtient la valeur d'une cellule et ne recalcule pas la formule lors de la modification de la valeur de la cellule.</span><span class="sxs-lookup"><span data-stu-id="176e7-104">Gets the value of a cell and doesn't recalculate the formula when the cell's value changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="176e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="176e7-105">Syntax</span></span>

<span data-ttu-id="176e7-106">GETVAL (\* \* *cellName* \* \*)</span><span class="sxs-lookup"><span data-stu-id="176e7-106">GETVAL(\*\* *cellname* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="176e7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="176e7-107">Parameters</span></span>

|<span data-ttu-id="176e7-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="176e7-108">**Name**</span></span>|<span data-ttu-id="176e7-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="176e7-109">**Required/Optional**</span></span>|<span data-ttu-id="176e7-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="176e7-110">**Data Type**</span></span>|<span data-ttu-id="176e7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="176e7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="176e7-112">_cellName_</span><span class="sxs-lookup"><span data-stu-id="176e7-112">_cellname_</span></span> <br/> |<span data-ttu-id="176e7-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="176e7-113">Required</span></span>  <br/> |<span data-ttu-id="176e7-114">**String**</span><span class="sxs-lookup"><span data-stu-id="176e7-114">**String**</span></span> <br/> |<span data-ttu-id="176e7-115">Nom de la cellule dont la valeur doit être obtenue.</span><span class="sxs-lookup"><span data-stu-id="176e7-115">The name of the cell to get the value of.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="176e7-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="176e7-116">Example</span></span>

<span data-ttu-id="176e7-117">GETVAL(PinX) + GETVAL(VY) + Width</span><span class="sxs-lookup"><span data-stu-id="176e7-117">GETVAL(PinX) + GETVAL(PinY) + Width</span></span> 
  
<span data-ttu-id="176e7-118">Renvoie la somme des valeurs des cellules PinX, PinY et Width.</span><span class="sxs-lookup"><span data-stu-id="176e7-118">Returns the sum of the value of the PinX, PinY, and Width cells.</span></span> 
  

