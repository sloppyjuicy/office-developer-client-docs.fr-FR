---
title: ROUND Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arrondit un nombre à la précision représentée par numberofdigits .
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439967"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="091df-103">ROUND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="091df-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="091df-104">Arrondit un nombre à la précision représentée par  *numberofdigits*  .</span><span class="sxs-lookup"><span data-stu-id="091df-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="091df-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="091df-105">Syntax</span></span>

<span data-ttu-id="091df-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span><span class="sxs-lookup"><span data-stu-id="091df-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="091df-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="091df-107">Parameters</span></span>

|<span data-ttu-id="091df-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="091df-108">**Name**</span></span>|<span data-ttu-id="091df-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="091df-109">**Required/Optional**</span></span>|<span data-ttu-id="091df-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="091df-110">**Data Type**</span></span>|<span data-ttu-id="091df-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="091df-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="091df-112">_number_</span><span class="sxs-lookup"><span data-stu-id="091df-112">_number_</span></span> <br/> |<span data-ttu-id="091df-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="091df-113">Required</span></span>  <br/> |<span data-ttu-id="091df-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="091df-114">**Number**</span></span> <br/> |<span data-ttu-id="091df-115">Nombre à arrondir</span><span class="sxs-lookup"><span data-stu-id="091df-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="091df-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="091df-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="091df-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="091df-117">Required</span></span>  <br/> |<span data-ttu-id="091df-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="091df-118">**Number**</span></span> <br/> |<span data-ttu-id="091df-119">Nombre de décimales de précision</span><span class="sxs-lookup"><span data-stu-id="091df-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="091df-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="091df-120">Remarks</span></span>

<span data-ttu-id="091df-121">Si  _numberofdigits_ est supérieur à  _0,_ le nombre est arrondi par  _nombreofdigits_ à droite de la décimale.</span><span class="sxs-lookup"><span data-stu-id="091df-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="091df-122">Si  _numberofdigits est_ 0,  _le nombre_ est arrondi à un nombre complet.</span><span class="sxs-lookup"><span data-stu-id="091df-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="091df-123">Si _numberofdigits_ est inférieur à  0, le nombre est arrondi par _nombreofdigits_ à gauche de la décimale.</span><span class="sxs-lookup"><span data-stu-id="091df-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="091df-124">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="091df-124">Example 1</span></span>

<span data-ttu-id="091df-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="091df-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="091df-126">Renvoie 123,65.</span><span class="sxs-lookup"><span data-stu-id="091df-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="091df-127">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="091df-127">Example 2</span></span>

<span data-ttu-id="091df-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="091df-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="091df-129">Renvoie 124.</span><span class="sxs-lookup"><span data-stu-id="091df-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="091df-130">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="091df-130">Example 3</span></span>

<span data-ttu-id="091df-131">ROUND(123,654,-1)</span><span class="sxs-lookup"><span data-stu-id="091df-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="091df-132">Renvoie 120.</span><span class="sxs-lookup"><span data-stu-id="091df-132">Returns 120.</span></span>
  

