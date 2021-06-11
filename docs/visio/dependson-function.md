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
ms.openlocfilehash: 26e7f5fb0620a5f1812d878f02d5bedd43afe524
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423467"
---
# <a name="dependson-function"></a><span data-ttu-id="cf9d9-103">Fonction DEPENDSON</span><span class="sxs-lookup"><span data-stu-id="cf9d9-103">DEPENDSON Function</span></span>

<span data-ttu-id="cf9d9-104">Crée une dépendance de référence de cellule.</span><span class="sxs-lookup"><span data-stu-id="cf9d9-104">Creates a cell reference dependency.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cf9d9-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cf9d9-105">Syntax</span></span>

<span data-ttu-id="cf9d9-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span><span class="sxs-lookup"><span data-stu-id="cf9d9-106">DEPENDSON(\*\* *cellref* \*\* [, \*\* *cellref2* \*\*,...])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cf9d9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cf9d9-107">Parameters</span></span>

|<span data-ttu-id="cf9d9-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cf9d9-108">**Name**</span></span>|<span data-ttu-id="cf9d9-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="cf9d9-109">**Required/Optional**</span></span>|<span data-ttu-id="cf9d9-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="cf9d9-110">**Data Type**</span></span>|<span data-ttu-id="cf9d9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="cf9d9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cf9d9-112">_cellref_</span><span class="sxs-lookup"><span data-stu-id="cf9d9-112">_cellref_</span></span> <br/> |<span data-ttu-id="cf9d9-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cf9d9-113">Required</span></span>  <br/> |<span data-ttu-id="cf9d9-114">**String**</span><span class="sxs-lookup"><span data-stu-id="cf9d9-114">**String**</span></span> <br/> |<span data-ttu-id="cf9d9-115">Première référence de cellule.</span><span class="sxs-lookup"><span data-stu-id="cf9d9-115">The first cell reference.</span></span>  <br/> |
| <span data-ttu-id="cf9d9-116">_cellref2_</span><span class="sxs-lookup"><span data-stu-id="cf9d9-116">_cellref2_</span></span> <br/> |<span data-ttu-id="cf9d9-117">Facultatif</span><span class="sxs-lookup"><span data-stu-id="cf9d9-117">Optional</span></span>  <br/> |<span data-ttu-id="cf9d9-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="cf9d9-118">**String**</span></span> <br/> |<span data-ttu-id="cf9d9-119">Deuxième référence de cellule.</span><span class="sxs-lookup"><span data-stu-id="cf9d9-119">The second cell reference.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf9d9-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="cf9d9-120">Remarks</span></span>

<span data-ttu-id="cf9d9-p101">Cette fonction renvoie toujours la valeur FALSE. Elle n’a pas d’effet lorsqu’elle est utilisée dans une ligne Event ou dans une cellule Action.</span><span class="sxs-lookup"><span data-stu-id="cf9d9-p101">This function always returns FALSE. It has no effect when used in an Event row or an Action cell.</span></span> 
  
## <a name="example"></a><span data-ttu-id="cf9d9-123">Exemple</span><span class="sxs-lookup"><span data-stu-id="cf9d9-123">Example</span></span>

<span data-ttu-id="cf9d9-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="cf9d9-124">OPENTEXTWIN() + DEPENDSON(PinX,PinY)</span></span> 
  
<span data-ttu-id="cf9d9-125">Ouvre le bloc de texte d’une forme lorsque les cellules PinX ou PinY de la forme sont modifiées.</span><span class="sxs-lookup"><span data-stu-id="cf9d9-125">Opens the text block for a shape whenever the shape's PinX or PinY cells change.</span></span> 
  

