---
title: ROUND, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Arrondit un nombre selon la précision indiquée par l’argument nombredechiffres.
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19789506"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="4aba3-103">ROUND, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="4aba3-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="4aba3-104">Arrondit un nombre selon la précision indiquée par *l’argument nombredechiffres* .</span><span class="sxs-lookup"><span data-stu-id="4aba3-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4aba3-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4aba3-105">Syntax</span></span>

<span data-ttu-id="4aba3-106">ROUND (** *numéro* **, ** *nombredechiffres* **)</span><span class="sxs-lookup"><span data-stu-id="4aba3-106">ROUND(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4aba3-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4aba3-107">Parameters</span></span>

|<span data-ttu-id="4aba3-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4aba3-108">**Name**</span></span>|<span data-ttu-id="4aba3-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="4aba3-109">**Required/Optional**</span></span>|<span data-ttu-id="4aba3-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="4aba3-110">**Data Type**</span></span>|<span data-ttu-id="4aba3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="4aba3-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4aba3-112">_number_</span><span class="sxs-lookup"><span data-stu-id="4aba3-112">_number_</span></span> <br/> |<span data-ttu-id="4aba3-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4aba3-113">Required</span></span>  <br/> |<span data-ttu-id="4aba3-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="4aba3-114">**Number**</span></span> <br/> |<span data-ttu-id="4aba3-115">Nombre à arrondir</span><span class="sxs-lookup"><span data-stu-id="4aba3-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="4aba3-116">_nombredechiffres_</span><span class="sxs-lookup"><span data-stu-id="4aba3-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="4aba3-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4aba3-117">Required</span></span>  <br/> |<span data-ttu-id="4aba3-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="4aba3-118">**Number**</span></span> <br/> |<span data-ttu-id="4aba3-119">Nombre de décimales de précision</span><span class="sxs-lookup"><span data-stu-id="4aba3-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4aba3-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="4aba3-120">Remarks</span></span>

<span data-ttu-id="4aba3-121">Si le _nombredechiffres_ est supérieur à 0, _nombre_ est arrondi à _nombredechiffres_ à droite du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="4aba3-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="4aba3-122">Si le _nombredechiffres_ est 0, _nombre_ est arrondi à un entier.</span><span class="sxs-lookup"><span data-stu-id="4aba3-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="4aba3-123">Si le _nombredechiffres_ est inférieur à 0, _nombre_ est arrondi à _nombredechiffres_ à gauche du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="4aba3-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="4aba3-124">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="4aba3-124">Example 1</span></span>

<span data-ttu-id="4aba3-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="4aba3-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="4aba3-126">Renvoie 123,65.</span><span class="sxs-lookup"><span data-stu-id="4aba3-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="4aba3-127">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="4aba3-127">Example 2</span></span>

<span data-ttu-id="4aba3-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="4aba3-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="4aba3-129">Renvoie 124.</span><span class="sxs-lookup"><span data-stu-id="4aba3-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="4aba3-130">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="4aba3-130">Example 3</span></span>

<span data-ttu-id="4aba3-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="4aba3-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="4aba3-132">Renvoie 120.</span><span class="sxs-lookup"><span data-stu-id="4aba3-132">Returns 120.</span></span>
  

