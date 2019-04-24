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
description: Arrondit un nombre à la précision représentée par le NombreDeChiffres.
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315574"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="8c213-103">ROUND Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="8c213-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="8c213-104">Arrondit un nombre à la précision représentée par le *NombreDeChiffres* .</span><span class="sxs-lookup"><span data-stu-id="8c213-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8c213-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8c213-105">Syntax</span></span>

<span data-ttu-id="8c213-106">ROUND (\* \* *nombre* \* \*, \* \* *NombreDeChiffres* \* \*)</span><span class="sxs-lookup"><span data-stu-id="8c213-106">ROUND(\*\* *number* \*\*, \*\* *numberofdigits* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="8c213-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8c213-107">Parameters</span></span>

|<span data-ttu-id="8c213-108">**Nom**</span><span class="sxs-lookup"><span data-stu-id="8c213-108">**Name**</span></span>|<span data-ttu-id="8c213-109">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="8c213-109">**Required/Optional**</span></span>|<span data-ttu-id="8c213-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="8c213-110">**Data Type**</span></span>|<span data-ttu-id="8c213-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8c213-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="8c213-112">_number_</span><span class="sxs-lookup"><span data-stu-id="8c213-112">_number_</span></span> <br/> |<span data-ttu-id="8c213-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c213-113">Required</span></span>  <br/> |<span data-ttu-id="8c213-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="8c213-114">**Number**</span></span> <br/> |<span data-ttu-id="8c213-115">Nombre à arrondir</span><span class="sxs-lookup"><span data-stu-id="8c213-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="8c213-116">_NombreDeChiffres_</span><span class="sxs-lookup"><span data-stu-id="8c213-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="8c213-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="8c213-117">Required</span></span>  <br/> |<span data-ttu-id="8c213-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="8c213-118">**Number**</span></span> <br/> |<span data-ttu-id="8c213-119">Nombre de décimales de précision</span><span class="sxs-lookup"><span data-stu-id="8c213-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8c213-120">Remarques</span><span class="sxs-lookup"><span data-stu-id="8c213-120">Remarks</span></span>

<span data-ttu-id="8c213-121">Si le _NombreDeChiffres_ est supérieur à 0, le _nombre_ est arrondi par le _NombreDeChiffres_ à droite du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="8c213-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="8c213-122">Si le _NombreDeChiffres_ est 0, le _nombre_ est arrondi à un entier.</span><span class="sxs-lookup"><span data-stu-id="8c213-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="8c213-123">Si le _NombreDeChiffres_ est inférieur à 0, le _nombre_ est arrondi par le _NombreDeChiffres_ à gauche du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="8c213-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="8c213-124">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="8c213-124">Example 1</span></span>

<span data-ttu-id="8c213-125">ROUND (123.654, 2)</span><span class="sxs-lookup"><span data-stu-id="8c213-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="8c213-126">Renvoie 123,65.</span><span class="sxs-lookup"><span data-stu-id="8c213-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="8c213-127">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="8c213-127">Example 2</span></span>

<span data-ttu-id="8c213-128">ROUND (123.654, 0)</span><span class="sxs-lookup"><span data-stu-id="8c213-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="8c213-129">Renvoie 124.</span><span class="sxs-lookup"><span data-stu-id="8c213-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="8c213-130">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="8c213-130">Example 3</span></span>

<span data-ttu-id="8c213-131">ROUND (123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="8c213-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="8c213-132">Renvoie 120.</span><span class="sxs-lookup"><span data-stu-id="8c213-132">Returns 120.</span></span>
  

