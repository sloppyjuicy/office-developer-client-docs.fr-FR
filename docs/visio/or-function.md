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
description: Renvoie la valeur TRUE (1) si une des expressions logiques transmises en tant que paramètres est TRUE.
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789194"
---
# <a name="or-function"></a><span data-ttu-id="4e461-103">OR, fonction</span><span class="sxs-lookup"><span data-stu-id="4e461-103">OR Function</span></span>

<span data-ttu-id="4e461-104">Renvoie la valeur TRUE (1) si une des expressions logiques transmises en tant que paramètres est TRUE.</span><span class="sxs-lookup"><span data-stu-id="4e461-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4e461-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4e461-105">Syntax</span></span>

<span data-ttu-id="4e461-106">OU (** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* **)</span><span class="sxs-lookup"><span data-stu-id="4e461-106">OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4e461-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4e461-107">Parameters</span></span>

|<span data-ttu-id="4e461-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4e461-108">**Name**</span></span>|<span data-ttu-id="4e461-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="4e461-109">**Required/Optional**</span></span>|<span data-ttu-id="4e461-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="4e461-110">**Data Type**</span></span>|<span data-ttu-id="4e461-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="4e461-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4e461-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="4e461-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="4e461-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4e461-113">Required</span></span>  <br/> |<span data-ttu-id="4e461-114">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e461-114">**String**</span></span> <br/> |<span data-ttu-id="4e461-115">Première expression dont vous souhaitez évaluer la véracité.</span><span class="sxs-lookup"><span data-stu-id="4e461-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="4e461-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="4e461-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="4e461-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4e461-117">Required</span></span>  <br/> |<span data-ttu-id="4e461-118">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e461-118">**String**</span></span> <br/> |<span data-ttu-id="4e461-119">Deuxième expression dont vous souhaitez évaluer la véracité.</span><span class="sxs-lookup"><span data-stu-id="4e461-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="4e461-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="4e461-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="4e461-121">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4e461-121">Required</span></span>  <br/> |<span data-ttu-id="4e461-122">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="4e461-122">**String**</span></span> <br/> |<span data-ttu-id="4e461-123">Nième expression dont vous souhaitez évaluer la véracité.</span><span class="sxs-lookup"><span data-stu-id="4e461-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4e461-124">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="4e461-124">Return value</span></span>

<span data-ttu-id="4e461-125">Booléenne</span><span class="sxs-lookup"><span data-stu-id="4e461-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4e461-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e461-126">Remarks</span></span>

<span data-ttu-id="4e461-p101">Une expression dont le calcul produit une valeur différente de zéro est considérée comme vraie (TRUE). Si toutes les expressions logiques sont fausses ou égales à 0, la fonction OR renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="4e461-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="4e461-129">Exemple</span><span class="sxs-lookup"><span data-stu-id="4e461-129">Example</span></span>

<span data-ttu-id="4e461-130">OU (hauteur \> 1, PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="4e461-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="4e461-p102">Renvoie TRUE (1) si l’une des expressions au moins a la valeur TRUE. Renvoie FALSE (0) seulement si les deux expressions sont fausses.</span><span class="sxs-lookup"><span data-stu-id="4e461-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

