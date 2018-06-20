---
title: GETREF, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251884
localization_priority: Normal
ms.assetid: 25c9f817-d22b-28c9-1339-dc9f27d0dd41
description: Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencée change.
ms.openlocfilehash: 454314b1f156f560c237f22a45492978ca3c31ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788716"
---
# <a name="getref-function"></a><span data-ttu-id="3f154-103">GETREF, fonction</span><span class="sxs-lookup"><span data-stu-id="3f154-103">GETREF Function</span></span>

<span data-ttu-id="3f154-104">Fait référence à une cellule et ne recalcule pas la formule lorsque la cellule référencée change.</span><span class="sxs-lookup"><span data-stu-id="3f154-104">References a cell and doesn't recalculate the formula when the referenced cell changes.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="3f154-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3f154-105">Syntax</span></span>

<span data-ttu-id="3f154-106">GETREF (** *cellname* **)</span><span class="sxs-lookup"><span data-stu-id="3f154-106">GETREF(** *cellname* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3f154-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3f154-107">Parameters</span></span>

|<span data-ttu-id="3f154-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="3f154-108">**Name**</span></span>|<span data-ttu-id="3f154-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3f154-109">**Required/Optional**</span></span>|<span data-ttu-id="3f154-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3f154-110">**Data Type**</span></span>|<span data-ttu-id="3f154-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3f154-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3f154-112">_cellName_</span><span class="sxs-lookup"><span data-stu-id="3f154-112">_cellname_</span></span> <br/> |<span data-ttu-id="3f154-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3f154-113">Required</span></span>  <br/> |<span data-ttu-id="3f154-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="3f154-114">**String**</span></span> <br/> |<span data-ttu-id="3f154-115">Le nom de la cellule pour obtenir une référence à.</span><span class="sxs-lookup"><span data-stu-id="3f154-115">The name of the cell to get a reference to.</span></span>  <br/> |
   
## <a name="example"></a><span data-ttu-id="3f154-116">Exemple</span><span class="sxs-lookup"><span data-stu-id="3f154-116">Example</span></span>

<span data-ttu-id="3f154-117">SETF(GETREF(PinX),5.1)</span><span class="sxs-lookup"><span data-stu-id="3f154-117">SETF(GETREF(PinX),5.1)</span></span> 
  
<span data-ttu-id="3f154-118">Donne à la formule de la cellule PinX la valeur 5,1.</span><span class="sxs-lookup"><span data-stu-id="3f154-118">Sets the formula of the PinX cell to 5.1.</span></span> 
  

