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
description: Évalue l'une des deux expressions en fonction de la valeur de State.
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420345"
---
# <a name="userui-function"></a><span data-ttu-id="c0b51-103">Fonction USERUI</span><span class="sxs-lookup"><span data-stu-id="c0b51-103">USERUI Function</span></span>

<span data-ttu-id="c0b51-104">Évalue l'une des deux expressions en fonction de la valeur de _State_.</span><span class="sxs-lookup"><span data-stu-id="c0b51-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c0b51-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0b51-105">Syntax</span></span>

<span data-ttu-id="c0b51-106">USERUI (\* \* *État* \* \*, \* \* *DefaultExpression* \* \*, \* \* *userexpression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c0b51-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c0b51-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c0b51-107">Parameters</span></span>

|<span data-ttu-id="c0b51-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="c0b51-108">**Name**</span></span>|<span data-ttu-id="c0b51-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="c0b51-109">**Required/Optional**</span></span>|<span data-ttu-id="c0b51-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="c0b51-110">**Data Type**</span></span>|<span data-ttu-id="c0b51-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="c0b51-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c0b51-112">_state_</span><span class="sxs-lookup"><span data-stu-id="c0b51-112">_state_</span></span> <br/> |<span data-ttu-id="c0b51-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0b51-113">Required</span></span>  <br/> |<span data-ttu-id="c0b51-114">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="c0b51-114">**Boolean**</span></span> <br/> |<span data-ttu-id="c0b51-115">Détermine l'expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="c0b51-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="c0b51-116">_DefaultExpression_</span><span class="sxs-lookup"><span data-stu-id="c0b51-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="c0b51-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0b51-117">Required</span></span>  <br/> |<span data-ttu-id="c0b51-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c0b51-118">**String**</span></span> <br/> |<span data-ttu-id="c0b51-119">Expression par défaut.</span><span class="sxs-lookup"><span data-stu-id="c0b51-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="c0b51-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="c0b51-120">_userexpression_</span></span> <br/> |<span data-ttu-id="c0b51-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c0b51-121">Required</span></span>  <br/> |<span data-ttu-id="c0b51-122">**String**</span><span class="sxs-lookup"><span data-stu-id="c0b51-122">**String**</span></span> <br/> |<span data-ttu-id="c0b51-123">Expression fournie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c0b51-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c0b51-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="c0b51-124">Remarks</span></span>

<span data-ttu-id="c0b51-125">Si _State_ est égal à 0, la fonction USERUI évalue la _DefaultExpression_.</span><span class="sxs-lookup"><span data-stu-id="c0b51-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="c0b51-126">Si _State_ est égal à 1, il évalue le _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="c0b51-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="c0b51-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="c0b51-127">Example</span></span>

<span data-ttu-id="c0b51-128">USERUI (1, si (largeur\>6in, 6In, largeur), largeur\*0,75)</span><span class="sxs-lookup"><span data-stu-id="c0b51-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="c0b51-129">Évalue la largeur\*de l'expression 075 et renvoie le résultat.</span><span class="sxs-lookup"><span data-stu-id="c0b51-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

