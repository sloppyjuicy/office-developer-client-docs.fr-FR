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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331324"
---
# <a name="userui-function"></a><span data-ttu-id="5d2a4-103">Fonction USERUI</span><span class="sxs-lookup"><span data-stu-id="5d2a4-103">USERUI Function</span></span>

<span data-ttu-id="5d2a4-104">Évalue l'une des deux expressions en fonction de la valeur de _State_.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="5d2a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5d2a4-105">Syntax</span></span>

<span data-ttu-id="5d2a4-106">USERUI (\* \* *État* \* \*, \* \* *DefaultExpression* \* \*, \* \* *userexpression* \* \*)</span><span class="sxs-lookup"><span data-stu-id="5d2a4-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5d2a4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5d2a4-107">Parameters</span></span>

|<span data-ttu-id="5d2a4-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-108">**Name**</span></span>|<span data-ttu-id="5d2a4-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-109">**Required/Optional**</span></span>|<span data-ttu-id="5d2a4-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-110">**Data Type**</span></span>|<span data-ttu-id="5d2a4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5d2a4-112">_state_</span><span class="sxs-lookup"><span data-stu-id="5d2a4-112">_state_</span></span> <br/> |<span data-ttu-id="5d2a4-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5d2a4-113">Required</span></span>  <br/> |<span data-ttu-id="5d2a4-114">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-114">**Boolean**</span></span> <br/> |<span data-ttu-id="5d2a4-115">Détermine l'expression à évaluer.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="5d2a4-116">_DefaultExpression_</span><span class="sxs-lookup"><span data-stu-id="5d2a4-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="5d2a4-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5d2a4-117">Required</span></span>  <br/> |<span data-ttu-id="5d2a4-118">**String**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-118">**String**</span></span> <br/> |<span data-ttu-id="5d2a4-119">Expression par défaut.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="5d2a4-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="5d2a4-120">_userexpression_</span></span> <br/> |<span data-ttu-id="5d2a4-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5d2a4-121">Required</span></span>  <br/> |<span data-ttu-id="5d2a4-122">**String**</span><span class="sxs-lookup"><span data-stu-id="5d2a4-122">**String**</span></span> <br/> |<span data-ttu-id="5d2a4-123">Expression fournie par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d2a4-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="5d2a4-124">Remarks</span></span>

<span data-ttu-id="5d2a4-125">Si _State_ est égal à 0, la fonction USERUI évalue la _DefaultExpression_.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="5d2a4-126">Si _State_ est égal à 1, il évalue le _userexpression_.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="5d2a4-127">Exemple</span><span class="sxs-lookup"><span data-stu-id="5d2a4-127">Example</span></span>

<span data-ttu-id="5d2a4-128">USERUI (1, si (largeur\>6in, 6In, largeur), largeur\*0,75)</span><span class="sxs-lookup"><span data-stu-id="5d2a4-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="5d2a4-129">Évalue la largeur\*de l'expression 075 et renvoie le résultat.</span><span class="sxs-lookup"><span data-stu-id="5d2a4-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

