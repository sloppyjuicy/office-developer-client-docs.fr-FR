---
title: OR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: Renvoie la valeur TRUE (1) si des expressions logiques transmises en tant que paramètres ont la valeur TRUE.
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337211"
---
# <a name="or-function"></a><span data-ttu-id="192e5-103">Fonction OR</span><span class="sxs-lookup"><span data-stu-id="192e5-103">OR Function</span></span>

<span data-ttu-id="192e5-104">Renvoie la valeur TRUE (1) si des expressions logiques transmises en tant que paramètres ont la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="192e5-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="192e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="192e5-105">Syntax</span></span>

<span data-ttu-id="192e5-106">ou (\* \* *logicalexpression1* \* \*, \* \* *logicalexpression2* \* \*,..., \* \* *logicalexpressionN* \* \*)</span><span class="sxs-lookup"><span data-stu-id="192e5-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="192e5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="192e5-107">Parameters</span></span>

|<span data-ttu-id="192e5-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="192e5-108">**Name**</span></span>|<span data-ttu-id="192e5-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="192e5-109">**Required/Optional**</span></span>|<span data-ttu-id="192e5-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="192e5-110">**Data Type**</span></span>|<span data-ttu-id="192e5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="192e5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="192e5-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="192e5-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="192e5-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="192e5-113">Required</span></span>  <br/> |<span data-ttu-id="192e5-114">**String**</span><span class="sxs-lookup"><span data-stu-id="192e5-114">**String**</span></span> <br/> |<span data-ttu-id="192e5-115">Première expression dont vous souhaitez évaluer la véracité.</span><span class="sxs-lookup"><span data-stu-id="192e5-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="192e5-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="192e5-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="192e5-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="192e5-117">Required</span></span>  <br/> |<span data-ttu-id="192e5-118">**String**</span><span class="sxs-lookup"><span data-stu-id="192e5-118">**String**</span></span> <br/> |<span data-ttu-id="192e5-119">Deuxième expression dont vous souhaitez évaluer la véracité.</span><span class="sxs-lookup"><span data-stu-id="192e5-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="192e5-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="192e5-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="192e5-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="192e5-121">Required</span></span>  <br/> |<span data-ttu-id="192e5-122">**String**</span><span class="sxs-lookup"><span data-stu-id="192e5-122">**String**</span></span> <br/> |<span data-ttu-id="192e5-123">Nième expression dont vous souhaitez évaluer la véracité.</span><span class="sxs-lookup"><span data-stu-id="192e5-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="192e5-124">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="192e5-124">Return value</span></span>

<span data-ttu-id="192e5-125">Booléen</span><span class="sxs-lookup"><span data-stu-id="192e5-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="192e5-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="192e5-126">Remarks</span></span>

<span data-ttu-id="192e5-p101">Une expression dont le calcul produit une valeur différente de zéro est considérée comme vraie (TRUE). Si toutes les expressions logiques sont fausses ou égales à 0, la fonction OR renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="192e5-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="192e5-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="192e5-129">Example</span></span>

<span data-ttu-id="192e5-130">OU (hauteur \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="192e5-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="192e5-131">Renvoie TRUE (1) si l’une des expressions au moins a la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="192e5-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="192e5-132">Renvoie FALSE (0) seulement si les deux expressions sont fausses.</span><span class="sxs-lookup"><span data-stu-id="192e5-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

