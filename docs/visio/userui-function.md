---
title: USERUI, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: Calcule l’une des deux expressions en fonction de la valeur d’état.
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789992"
---
# <a name="userui-function"></a><span data-ttu-id="95fb7-103">USERUI, fonction</span><span class="sxs-lookup"><span data-stu-id="95fb7-103">USERUI Function</span></span>

<span data-ttu-id="95fb7-104">Calcule l’une des deux expressions en fonction de la valeur _d’état_.</span><span class="sxs-lookup"><span data-stu-id="95fb7-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="95fb7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="95fb7-105">Syntax</span></span>

<span data-ttu-id="95fb7-106">USERUI (** *état* **, ** *expressiondéfaut* **, ** *expressionutil* **)</span><span class="sxs-lookup"><span data-stu-id="95fb7-106">USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="95fb7-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="95fb7-107">Parameters</span></span>

|<span data-ttu-id="95fb7-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="95fb7-108">**Name**</span></span>|<span data-ttu-id="95fb7-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="95fb7-109">**Required/Optional**</span></span>|<span data-ttu-id="95fb7-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="95fb7-110">**Data Type**</span></span>|<span data-ttu-id="95fb7-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="95fb7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="95fb7-112">_state_</span><span class="sxs-lookup"><span data-stu-id="95fb7-112">_state_</span></span> <br/> |<span data-ttu-id="95fb7-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="95fb7-113">Required</span></span>  <br/> |<span data-ttu-id="95fb7-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="95fb7-114">**Boolean**</span></span> <br/> |<span data-ttu-id="95fb7-115">Détermine l’expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="95fb7-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="95fb7-116">_expressiondéfaut_</span><span class="sxs-lookup"><span data-stu-id="95fb7-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="95fb7-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="95fb7-117">Required</span></span>  <br/> |<span data-ttu-id="95fb7-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fb7-118">**String**</span></span> <br/> |<span data-ttu-id="95fb7-119">L’expression par défaut.</span><span class="sxs-lookup"><span data-stu-id="95fb7-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="95fb7-120">_expressionutil_</span><span class="sxs-lookup"><span data-stu-id="95fb7-120">_userexpression_</span></span> <br/> |<span data-ttu-id="95fb7-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="95fb7-121">Required</span></span>  <br/> |<span data-ttu-id="95fb7-122">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="95fb7-122">**String**</span></span> <br/> |<span data-ttu-id="95fb7-123">Une expression est fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="95fb7-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95fb7-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="95fb7-124">Remarks</span></span>

<span data-ttu-id="95fb7-125">Si _l’état_ est 0, la fonction USERUI calcule _expressiondéfaut_.</span><span class="sxs-lookup"><span data-stu-id="95fb7-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="95fb7-126">Si _l’état_ est 1, elle évalue _expressionutil_.</span><span class="sxs-lookup"><span data-stu-id="95fb7-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="95fb7-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="95fb7-127">Example</span></span>

<span data-ttu-id="95fb7-128">USERUI (1, si (largeur\>en 6, 6 in, largeur), largeur\*0,75)</span><span class="sxs-lookup"><span data-stu-id="95fb7-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="95fb7-129">Évalue l’expression largeur\*.075 et renvoie le résultat.</span><span class="sxs-lookup"><span data-stu-id="95fb7-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

