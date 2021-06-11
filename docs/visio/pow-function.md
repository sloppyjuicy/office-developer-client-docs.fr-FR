---
title: POW, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: Renvoie un nombre élevé à la puissance d’un exposant.
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406310"
---
# <a name="pow-function"></a><span data-ttu-id="1bde4-103">Fonction POW</span><span class="sxs-lookup"><span data-stu-id="1bde4-103">POW Function</span></span>

<span data-ttu-id="1bde4-104">Renvoie un nombre élevé à la puissance d’un exposant.</span><span class="sxs-lookup"><span data-stu-id="1bde4-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="1bde4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1bde4-105">Syntax</span></span>

<span data-ttu-id="1bde4-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span><span class="sxs-lookup"><span data-stu-id="1bde4-106">POW(\*\* *number* \*\*, \*\* *exponent* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1bde4-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1bde4-107">Parameters</span></span>

|<span data-ttu-id="1bde4-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="1bde4-108">**Name**</span></span>|<span data-ttu-id="1bde4-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="1bde4-109">**Required/Optional**</span></span>|<span data-ttu-id="1bde4-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="1bde4-110">**Data Type**</span></span>|<span data-ttu-id="1bde4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="1bde4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1bde4-112">_number_</span><span class="sxs-lookup"><span data-stu-id="1bde4-112">_number_</span></span> <br/> |<span data-ttu-id="1bde4-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1bde4-113">Required</span></span>  <br/> |<span data-ttu-id="1bde4-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="1bde4-114">**Number**</span></span> <br/> |<span data-ttu-id="1bde4-115">Nombre à élever à la puissance d’un exposant</span><span class="sxs-lookup"><span data-stu-id="1bde4-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="1bde4-116">_exposant_</span><span class="sxs-lookup"><span data-stu-id="1bde4-116">_exponent_</span></span> <br/> |<span data-ttu-id="1bde4-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="1bde4-117">Required</span></span>  <br/> |<span data-ttu-id="1bde4-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="1bde4-118">**Number**</span></span> <br/> |<span data-ttu-id="1bde4-119">Exposant</span><span class="sxs-lookup"><span data-stu-id="1bde4-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1bde4-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="1bde4-120">Remarks</span></span>

<span data-ttu-id="1bde4-121">Le  _nombre_ et  _l’exposant_ peuvent être des nombres non-nombres et être négatifs.</span><span class="sxs-lookup"><span data-stu-id="1bde4-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="1bde4-122">Si  _le nombre_ n’est pas 0 et  _l’exposant_ est 0, cette fonction renvoie 1.</span><span class="sxs-lookup"><span data-stu-id="1bde4-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="1bde4-123">Si  _le nombre_ est 0 et que  _l’exposant_ est négatif, cette fonction renvoie 0,0.</span><span class="sxs-lookup"><span data-stu-id="1bde4-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="1bde4-124">Si le _nombre et_ l’exposant  sont tous  les deux 0, ou si le nombre est négatif et qu’il n’est pas un nombre d’exposants, cette fonction renvoie 0,0. </span><span class="sxs-lookup"><span data-stu-id="1bde4-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="1bde4-125">Si le  _nombre et_  _l’exposant_ sont négatifs, cette fonction renvoie -1,#IND.</span><span class="sxs-lookup"><span data-stu-id="1bde4-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1bde4-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="1bde4-126">Example</span></span>

<span data-ttu-id="1bde4-127">POW(5,2)</span><span class="sxs-lookup"><span data-stu-id="1bde4-127">POW(5,2)</span></span> 
  
<span data-ttu-id="1bde4-128">Renvoie 25.</span><span class="sxs-lookup"><span data-stu-id="1bde4-128">Returns 25.</span></span> 
  

