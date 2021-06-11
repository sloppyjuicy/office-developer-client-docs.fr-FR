---
title: TRUNC, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: Renvoie un nombre tronqué au nombre de chiffres spécifié.
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426498"
---
# <a name="trunc-function"></a><span data-ttu-id="cc8f2-103">Fonction TRUNC</span><span class="sxs-lookup"><span data-stu-id="cc8f2-103">TRUNC Function</span></span>

<span data-ttu-id="cc8f2-104">Renvoie un nombre tronqué au nombre de chiffres spécifié.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="cc8f2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cc8f2-105">Syntax</span></span>

<span data-ttu-id="cc8f2-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span><span class="sxs-lookup"><span data-stu-id="cc8f2-106">TRUNC(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="cc8f2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cc8f2-107">Parameters</span></span>

|<span data-ttu-id="cc8f2-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="cc8f2-108">**Name**</span></span>|<span data-ttu-id="cc8f2-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="cc8f2-109">**Required/Optional**</span></span>|<span data-ttu-id="cc8f2-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="cc8f2-110">**Data Type**</span></span>|<span data-ttu-id="cc8f2-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="cc8f2-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="cc8f2-112">_number_</span><span class="sxs-lookup"><span data-stu-id="cc8f2-112">_number_</span></span> <br/> |<span data-ttu-id="cc8f2-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cc8f2-113">Required</span></span>  <br/> |<span data-ttu-id="cc8f2-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="cc8f2-114">**Numeric**</span></span> <br/> |<span data-ttu-id="cc8f2-115">Nombre à tronquer.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="cc8f2-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="cc8f2-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="cc8f2-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="cc8f2-117">Required</span></span>  <br/> |<span data-ttu-id="cc8f2-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="cc8f2-118">**Numeric**</span></span> <br/> |<span data-ttu-id="cc8f2-119">Nombre de chiffres à _tronqué._</span><span class="sxs-lookup"><span data-stu-id="cc8f2-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="cc8f2-120">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="cc8f2-120">Return value</span></span>

<span data-ttu-id="cc8f2-121">Numérique.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cc8f2-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="cc8f2-122">Remarks</span></span>

<span data-ttu-id="cc8f2-123">Si  _numberofdigits_ est supérieur à  _0,_ le nombre est tronqué en  _nombreofdigits_ à droite de la décimale.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="cc8f2-124">Si  _le nombreofdigits_ est 0,  _le_ nombre est tronqué sur un nombre total.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="cc8f2-125">Si _numberofdigits_ est inférieur à  0, le nombre est tronqué en _nombreofdigits_ à gauche de la décimale.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="cc8f2-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="cc8f2-126">Example 1</span></span>

<span data-ttu-id="cc8f2-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="cc8f2-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="cc8f2-128">Renvoie 123,65.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="cc8f2-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="cc8f2-129">Example 2</span></span>

<span data-ttu-id="cc8f2-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="cc8f2-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="cc8f2-131">Renvoie 123.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="cc8f2-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="cc8f2-132">Example 3</span></span>

<span data-ttu-id="cc8f2-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="cc8f2-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="cc8f2-134">Renvoie 120.</span><span class="sxs-lookup"><span data-stu-id="cc8f2-134">Returns 120.</span></span>
  

