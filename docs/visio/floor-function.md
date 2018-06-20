---
title: FLOOR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: Arrondit un nombre proche de 0 (zéro), à l’entier suivant ou sur l’occurrence suivante du dénominateur.
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788643"
---
# <a name="floor-function"></a><span data-ttu-id="58e8c-103">FLOOR, fonction</span><span class="sxs-lookup"><span data-stu-id="58e8c-103">FLOOR Function</span></span>

<span data-ttu-id="58e8c-104">Arrondit un nombre proche de 0 (zéro), à l’entier suivant ou sur l’occurrence suivante de _multiple_.</span><span class="sxs-lookup"><span data-stu-id="58e8c-104">Rounds a number toward 0 (zero), to the next integer, or to the next instance of  _multiple_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="58e8c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="58e8c-105">Syntax</span></span>

<span data-ttu-id="58e8c-106">FLOOR (** *numéro* **, ** *plusieurs* **)</span><span class="sxs-lookup"><span data-stu-id="58e8c-106">FLOOR(** *number* **, ** *multiple* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="58e8c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="58e8c-107">Parameters</span></span>

|<span data-ttu-id="58e8c-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="58e8c-108">**Name**</span></span>|<span data-ttu-id="58e8c-109">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="58e8c-109">**Required/Optional**</span></span>|<span data-ttu-id="58e8c-110">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="58e8c-110">**Data Type**</span></span>|<span data-ttu-id="58e8c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="58e8c-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="58e8c-112">_number_</span><span class="sxs-lookup"><span data-stu-id="58e8c-112">_number_</span></span> <br/> |<span data-ttu-id="58e8c-113">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="58e8c-113">Required</span></span>  <br/> |<span data-ttu-id="58e8c-114">**Number**</span><span class="sxs-lookup"><span data-stu-id="58e8c-114">**Number**</span></span> <br/> |<span data-ttu-id="58e8c-115">Nombre à arrondir.</span><span class="sxs-lookup"><span data-stu-id="58e8c-115">The number to round.</span></span>  <br/> |
| <span data-ttu-id="58e8c-116">_plusieurs_</span><span class="sxs-lookup"><span data-stu-id="58e8c-116">_multiple_</span></span> <br/> |<span data-ttu-id="58e8c-117">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="58e8c-117">Required</span></span>  <br/> |<span data-ttu-id="58e8c-118">**Number**</span><span class="sxs-lookup"><span data-stu-id="58e8c-118">**Number**</span></span> <br/> |<span data-ttu-id="58e8c-119">Multiple vers lequel arrondir.</span><span class="sxs-lookup"><span data-stu-id="58e8c-119">The multiple to which to round.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="58e8c-120">Valeur renvoy�e</span><span class="sxs-lookup"><span data-stu-id="58e8c-120">Return value</span></span>

<span data-ttu-id="58e8c-121">Nombre</span><span class="sxs-lookup"><span data-stu-id="58e8c-121">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="58e8c-122">Remarques</span><span class="sxs-lookup"><span data-stu-id="58e8c-122">Remarks</span></span>

<span data-ttu-id="58e8c-123">Si _plusieurs_ n’est pas spécifié, le nombre est arrondi proche de 0 à l’entier.</span><span class="sxs-lookup"><span data-stu-id="58e8c-123">If  _multiple_ is not specified, the number rounds toward 0 to the next integer.</span></span> 
  
 <span data-ttu-id="58e8c-124">_Nombre_ et _plusieurs_ doivent avoir le même signe, sinon une #NUM !</span><span class="sxs-lookup"><span data-stu-id="58e8c-124">_Number_ and  _multiple_ must have the same signs, or a #NUM!</span></span> <span data-ttu-id="58e8c-125">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="58e8c-125">error is returned.</span></span> <span data-ttu-id="58e8c-126">Si _nombre_ ou _multiple_ ne peut pas être convertie en une valeur, un #VALUE !</span><span class="sxs-lookup"><span data-stu-id="58e8c-126">If either  _number_ or  _multiple_ cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="58e8c-127">erreur est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="58e8c-127">error is returned.</span></span> <span data-ttu-id="58e8c-128">Si le _nombre_ ou le _multiple_ est égal à 0, le résultat est 0.</span><span class="sxs-lookup"><span data-stu-id="58e8c-128">If either  _number_ or  _multiple_ is 0, the result is 0.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="58e8c-129">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="58e8c-129">Example 1</span></span>

<span data-ttu-id="58e8c-130">FLOOR(3.7)</span><span class="sxs-lookup"><span data-stu-id="58e8c-130">FLOOR(3.7)</span></span>
  
<span data-ttu-id="58e8c-131">Renvoie 3.</span><span class="sxs-lookup"><span data-stu-id="58e8c-131">Returns 3.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="58e8c-132">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="58e8c-132">Example 2</span></span>

<span data-ttu-id="58e8c-133">FLOOR(-3.7)</span><span class="sxs-lookup"><span data-stu-id="58e8c-133">FLOOR(-3.7)</span></span>
  
<span data-ttu-id="58e8c-134">Renvoie -3.</span><span class="sxs-lookup"><span data-stu-id="58e8c-134">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="58e8c-135">Exemple 3</span><span class="sxs-lookup"><span data-stu-id="58e8c-135">Example 3</span></span>

<span data-ttu-id="58e8c-136">FLOOR (3.7, 0,5)</span><span class="sxs-lookup"><span data-stu-id="58e8c-136">FLOOR(3.7, 0.5)</span></span>
  
<span data-ttu-id="58e8c-137">Renvoie 3,5.</span><span class="sxs-lookup"><span data-stu-id="58e8c-137">Returns 3.5.</span></span>
  

