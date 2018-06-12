---
title: DEPENDSON, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251420
localization_priority: Normal
ms.assetid: 8fcfcfdd-69e2-b061-fdb6-d29389d14403
description: Crée une dépendance de référence de cellule.
ms.openlocfilehash: 07c0d79668230cbf2b1e8d51b50e67835c87e2f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788458"
---
# <a name="dependson-function"></a><span data-ttu-id="95db6-103">DEPENDSON, fonction</span><span class="sxs-lookup"><span data-stu-id="95db6-103">DEPENDSON Function</span></span>

<span data-ttu-id="95db6-104">Crée une dépendance de référence de cellule.</span><span class="sxs-lookup"><span data-stu-id="95db6-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="95db6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95db6-105">Syntax</span></span>

<span data-ttu-id="95db6-106">DEPENDSON (** *cellref* ** [, ** *cellref2* **,...])</span><span class="sxs-lookup"><span data-stu-id="95db6-106">DEPENDSON(** *cellref* ** [, ** *cellref2* **,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95db6-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95db6-107">Parameters</span></span>

|<span data-ttu-id="95db6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="95db6-108">**Name**</span></span>|<span data-ttu-id="95db6-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="95db6-109">**Required/Optional**</span></span>|<span data-ttu-id="95db6-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="95db6-110">**Data Type**</span></span>|<span data-ttu-id="95db6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="95db6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95db6-112">_CellRef_</span><span class="sxs-lookup"><span data-stu-id="95db6-112">_cellref_</span></span> <br/> |<span data-ttu-id="95db6-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="95db6-113">Required</span></span>  <br/> |<span data-ttu-id="95db6-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="95db6-114">**String**</span></span> <br/> |<span data-ttu-id="95db6-115">Première référence de cellule.</span><span class="sxs-lookup"><span data-stu-id="95db6-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="95db6-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="95db6-116">_cellref2_</span></span> <br/> |<span data-ttu-id="95db6-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="95db6-117">Optional</span></span>  <br/> |<span data-ttu-id="95db6-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="95db6-118">**String**</span></span> <br/> |<span data-ttu-id="95db6-119">Deuxième référence de cellule.</span><span class="sxs-lookup"><span data-stu-id="95db6-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95db6-120">Note</span><span class="sxs-lookup"><span data-stu-id="95db6-120">Remarks</span></span>

<span data-ttu-id="95db6-p101">Cette fonction renvoie toujours la valeur FALSE. Elle n’a pas d’effet lorsqu’elle est utilisée dans une ligne Event ou dans une cellule Action.</span><span class="sxs-lookup"><span data-stu-id="95db6-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="95db6-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="95db6-123">Example</span></span>

<span data-ttu-id="95db6-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="95db6-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="95db6-125">Ouvre le bloc de texte d’une forme lorsque les cellules PinX ou PinY de la forme sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="95db6-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

