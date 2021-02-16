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
description: Évalue l’une des deux expressions en fonction de la valeur de l’état.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420345"
---
# <a name="userui-function"></a><span data-ttu-id="a2e26-103">Fonction USERUI</span><span class="sxs-lookup"><span data-stu-id="a2e26-103">USERUI Function</span></span>

<span data-ttu-id="a2e26-104">Évalue l’une des deux expressions en fonction de la valeur de  _l’état_.</span><span class="sxs-lookup"><span data-stu-id="a2e26-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a2e26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2e26-105">Syntax</span></span>

<span data-ttu-id="a2e26-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a2e26-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a2e26-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2e26-107">Parameters</span></span>

|<span data-ttu-id="a2e26-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="a2e26-108">**Name**</span></span>|<span data-ttu-id="a2e26-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="a2e26-109">**Required/Optional**</span></span>|<span data-ttu-id="a2e26-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="a2e26-110">**Data Type**</span></span>|<span data-ttu-id="a2e26-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a2e26-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a2e26-112">_state_</span><span class="sxs-lookup"><span data-stu-id="a2e26-112">_state_</span></span> <br/> |<span data-ttu-id="a2e26-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2e26-113">Required</span></span>  <br/> |<span data-ttu-id="a2e26-114">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="a2e26-114">**Boolean**</span></span> <br/> |<span data-ttu-id="a2e26-115">Détermine l’expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="a2e26-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a2e26-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="a2e26-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="a2e26-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2e26-117">Required</span></span>  <br/> |<span data-ttu-id="a2e26-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a2e26-118">**String**</span></span> <br/> |<span data-ttu-id="a2e26-119">Expression par défaut.</span><span class="sxs-lookup"><span data-stu-id="a2e26-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="a2e26-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="a2e26-120">_userexpression_</span></span> <br/> |<span data-ttu-id="a2e26-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a2e26-121">Required</span></span>  <br/> |<span data-ttu-id="a2e26-122">**String**</span><span class="sxs-lookup"><span data-stu-id="a2e26-122">**String**</span></span> <br/> |<span data-ttu-id="a2e26-123">Expression fournie par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a2e26-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2e26-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="a2e26-124">Remarks</span></span>

<span data-ttu-id="a2e26-125">Si _l’état_ est 0, la fonction USERUI évalue _l’expression par défaut._</span><span class="sxs-lookup"><span data-stu-id="a2e26-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="a2e26-126">Si  _l’état_ est 1, il évalue  _l’expression utilisateur_.</span><span class="sxs-lookup"><span data-stu-id="a2e26-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="a2e26-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="a2e26-127">Example</span></span>

<span data-ttu-id="a2e26-128">USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75)</span><span class="sxs-lookup"><span data-stu-id="a2e26-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="a2e26-129">Évalue l’expression Width \* .075 et renvoie le résultat.</span><span class="sxs-lookup"><span data-stu-id="a2e26-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

