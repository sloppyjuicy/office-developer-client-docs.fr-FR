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
description: Renvoie un nombre tronqué dans le nombre de chiffres spécifié.
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19789934"
---
# <a name="trunc-function"></a><span data-ttu-id="424ac-103">TRUNC, fonction</span><span class="sxs-lookup"><span data-stu-id="424ac-103">TRUNC Function</span></span>

<span data-ttu-id="424ac-104">Renvoie un nombre tronqué dans le nombre de chiffres spécifié.</span><span class="sxs-lookup"><span data-stu-id="424ac-104">Returns a number truncated to the specified number of digits.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="424ac-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="424ac-105">Syntax</span></span>

<span data-ttu-id="424ac-106">TRUNC (** *numéro* **, ** *nombredechiffres* **)</span><span class="sxs-lookup"><span data-stu-id="424ac-106">TRUNC(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="424ac-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="424ac-107">Parameters</span></span>

|<span data-ttu-id="424ac-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="424ac-108">**Name**</span></span>|<span data-ttu-id="424ac-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="424ac-109">**Required/Optional**</span></span>|<span data-ttu-id="424ac-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="424ac-110">**Data Type**</span></span>|<span data-ttu-id="424ac-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="424ac-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="424ac-112">_number_</span><span class="sxs-lookup"><span data-stu-id="424ac-112">_number_</span></span> <br/> |<span data-ttu-id="424ac-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="424ac-113">Required</span></span>  <br/> |<span data-ttu-id="424ac-114">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="424ac-114">**Numeric**</span></span> <br/> |<span data-ttu-id="424ac-115">Nombre à tronquer.</span><span class="sxs-lookup"><span data-stu-id="424ac-115">The number to truncate.</span></span>  <br/> |
| <span data-ttu-id="424ac-116">_nombredechiffres_</span><span class="sxs-lookup"><span data-stu-id="424ac-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="424ac-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="424ac-117">Required</span></span>  <br/> |<span data-ttu-id="424ac-118">**Numérique**</span><span class="sxs-lookup"><span data-stu-id="424ac-118">**Numeric**</span></span> <br/> |<span data-ttu-id="424ac-119">Le nombre de chiffres auquel vous voulez tronquer _nombre_.</span><span class="sxs-lookup"><span data-stu-id="424ac-119">The number of digits to which to truncate  _number_.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="424ac-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="424ac-120">Return value</span></span>

<span data-ttu-id="424ac-121">Numérique</span><span class="sxs-lookup"><span data-stu-id="424ac-121">Numeric.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="424ac-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="424ac-122">Remarks</span></span>

<span data-ttu-id="424ac-123">Si le _nombredechiffres_ est supérieur à 0, _nombre_ est arrondi au _nombredechiffres_ à droite du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="424ac-123">If  _numberofdigits_ is greater than 0,  _number_ is truncated to  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="424ac-124">Si le _nombredechiffres_ est 0, _nombre_ est arrondi à un entier.</span><span class="sxs-lookup"><span data-stu-id="424ac-124">If  _numberofdigits_ is 0,  _number_ is truncated to an integer.</span></span> <span data-ttu-id="424ac-125">Si le _nombredechiffres_ est inférieur à 0, _nombre_ est arrondi au _nombredechiffres_ à gauche du séparateur décimal.</span><span class="sxs-lookup"><span data-stu-id="424ac-125">If  _numberofdigits_ is less than 0,  _number_ is truncated to  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="424ac-126">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="424ac-126">Example 1</span></span>

<span data-ttu-id="424ac-127">TRUNC(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="424ac-127">TRUNC(123.654,2)</span></span>
  
<span data-ttu-id="424ac-128">Renvoie 123,65.</span><span class="sxs-lookup"><span data-stu-id="424ac-128">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="424ac-129">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="424ac-129">Example 2</span></span>

<span data-ttu-id="424ac-130">TRUNC(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="424ac-130">TRUNC(123.654,0)</span></span>
  
<span data-ttu-id="424ac-131">Renvoie 123.</span><span class="sxs-lookup"><span data-stu-id="424ac-131">Returns 123.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="424ac-132">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="424ac-132">Example 3</span></span>

<span data-ttu-id="424ac-133">TRUNC(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="424ac-133">TRUNC(123.654,-1)</span></span>
  
<span data-ttu-id="424ac-134">Renvoie 120.</span><span class="sxs-lookup"><span data-stu-id="424ac-134">Returns 120.</span></span>
  

