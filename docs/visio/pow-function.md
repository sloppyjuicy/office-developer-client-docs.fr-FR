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
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789347"
---
# <a name="pow-function"></a><span data-ttu-id="02bc5-103">POW, fonction</span><span class="sxs-lookup"><span data-stu-id="02bc5-103">POW Function</span></span>

<span data-ttu-id="02bc5-104">Renvoie un nombre élevé à la puissance d’un exposant.</span><span class="sxs-lookup"><span data-stu-id="02bc5-104">Returns a number raised to the power of an exponent.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="02bc5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02bc5-105">Syntax</span></span>

<span data-ttu-id="02bc5-106">POW (** *numéro* **, ** *exposant* **)</span><span class="sxs-lookup"><span data-stu-id="02bc5-106">POW(** *number* **, ** *exponent* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="02bc5-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="02bc5-107">Parameters</span></span>

|<span data-ttu-id="02bc5-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="02bc5-108">**Name**</span></span>|<span data-ttu-id="02bc5-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="02bc5-109">**Required/Optional**</span></span>|<span data-ttu-id="02bc5-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="02bc5-110">**Data Type**</span></span>|<span data-ttu-id="02bc5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="02bc5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="02bc5-112">_number_</span><span class="sxs-lookup"><span data-stu-id="02bc5-112">_number_</span></span> <br/> |<span data-ttu-id="02bc5-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="02bc5-113">Required</span></span>  <br/> |<span data-ttu-id="02bc5-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="02bc5-114">**Number**</span></span> <br/> |<span data-ttu-id="02bc5-115">Nombre à élever à la puissance d’un exposant</span><span class="sxs-lookup"><span data-stu-id="02bc5-115">The number to raise to the power of an exponent.</span></span>  <br/> |
| <span data-ttu-id="02bc5-116">_exposant_</span><span class="sxs-lookup"><span data-stu-id="02bc5-116">_exponent_</span></span> <br/> |<span data-ttu-id="02bc5-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="02bc5-117">Required</span></span>  <br/> |<span data-ttu-id="02bc5-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="02bc5-118">**Number**</span></span> <br/> |<span data-ttu-id="02bc5-119">Exposant</span><span class="sxs-lookup"><span data-stu-id="02bc5-119">The exponent.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02bc5-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="02bc5-120">Remarks</span></span>

<span data-ttu-id="02bc5-121">_Nombre_ et _exposant_ peuvent être des nombres entiers non, et ils peuvent être négatives.</span><span class="sxs-lookup"><span data-stu-id="02bc5-121">Both  _number_ and  _exponent_ may be non-integers, and they may be negative.</span></span> <span data-ttu-id="02bc5-122">Si _nombre_ n’est pas 0 et _exposant_ est 0, cette fonction renvoie la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="02bc5-122">If  _number_ is not 0 and  _exponent_ is 0, this function returns 1.</span></span> <span data-ttu-id="02bc5-123">Si _nombre_ est 0 et _exposant_ est négatif, cette fonction renvoie 0,0.</span><span class="sxs-lookup"><span data-stu-id="02bc5-123">If  _number_ is 0 and  _exponent_ is negative, this function returns 0.0.</span></span> <span data-ttu-id="02bc5-124">Si _nombre_ et _exposant_ sont égales à 0 ou si _nombre_ est négatif et _exposant_ n’est pas un entier, la fonction renvoie 0,0.</span><span class="sxs-lookup"><span data-stu-id="02bc5-124">If both  _number_ and  _exponent_ are 0, or if  _number_ is negative and  _exponent_ is not an integer, this function returns 0.0.</span></span> <span data-ttu-id="02bc5-125">Si _nombre_ et _exposant_ sont négatifs, la fonction renvoie -1. #IND.</span><span class="sxs-lookup"><span data-stu-id="02bc5-125">If both  _number_ and  _exponent_ are negative, this function returns -1.#IND.</span></span> 
  
## <a name="example"></a><span data-ttu-id="02bc5-126">Exemple</span><span class="sxs-lookup"><span data-stu-id="02bc5-126">Example</span></span>

<span data-ttu-id="02bc5-127">POW(5;2)</span><span class="sxs-lookup"><span data-stu-id="02bc5-127">POW(5,2)</span></span> 
  
<span data-ttu-id="02bc5-128">Renvoie 25.</span><span class="sxs-lookup"><span data-stu-id="02bc5-128">Returns 25.</span></span> 
  

