---
title: IsError, fonction (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Renvoie la valeur TRUE si la valeur de cellreference est une erreur ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.
ms.openlocfilehash: c93801f5d61e45be5d178027405ead3aa129654d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788866"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="34ebe-104">IsError, fonction (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="34ebe-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="34ebe-105">Renvoie la valeur TRUE si la valeur de _cellreference_ est une erreur ; dans le cas contraire, elle renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="34ebe-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="34ebe-106">La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="34ebe-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="34ebe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34ebe-107">Syntax</span></span>

<span data-ttu-id="34ebe-108">ISERROR (** *cellreference* **)</span><span class="sxs-lookup"><span data-stu-id="34ebe-108">ISERROR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="34ebe-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="34ebe-109">Parameters</span></span>

|<span data-ttu-id="34ebe-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="34ebe-110">**Name**</span></span>|<span data-ttu-id="34ebe-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="34ebe-111">**Required/Optional**</span></span>|<span data-ttu-id="34ebe-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="34ebe-112">**Data Type**</span></span>|<span data-ttu-id="34ebe-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="34ebe-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="34ebe-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="34ebe-114">_cellreference_</span></span> <br/> |<span data-ttu-id="34ebe-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="34ebe-115">Required</span></span>  <br/> |<span data-ttu-id="34ebe-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="34ebe-116">**String**</span></span> <br/> |<span data-ttu-id="34ebe-117">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="34ebe-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="34ebe-118">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="34ebe-118">Example 1</span></span>

|<span data-ttu-id="34ebe-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="34ebe-119">**Cell**</span></span>|<span data-ttu-id="34ebe-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="34ebe-120">**Formula**</span></span>|<span data-ttu-id="34ebe-121">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="34ebe-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34ebe-122">Cellule Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="34ebe-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="34ebe-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="34ebe-123">=NA( )</span></span>  <br/> |<span data-ttu-id="34ebe-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="34ebe-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="34ebe-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="34ebe-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="34ebe-126">=IsError(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="34ebe-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="34ebe-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="34ebe-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="34ebe-p103">Renvoie TRUE parce que l’erreur #N/A! est reconnue par la fonction ISERROR. Vous pouvez utiliser ISERR pour trouver tous les types d’erreur à l’exception de l’erreur #N/A!.</span><span class="sxs-lookup"><span data-stu-id="34ebe-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="34ebe-132">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="34ebe-132">Example 2</span></span>

|<span data-ttu-id="34ebe-133">**Cell**</span><span class="sxs-lookup"><span data-stu-id="34ebe-133">**Cell**</span></span>|<span data-ttu-id="34ebe-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="34ebe-134">**Formula**</span></span>|<span data-ttu-id="34ebe-135">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="34ebe-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="34ebe-136">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="34ebe-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="34ebe-137">="Maison"</span><span class="sxs-lookup"><span data-stu-id="34ebe-137">="House"</span></span>  <br/> |<span data-ttu-id="34ebe-138">#VALEUR!</span><span class="sxs-lookup"><span data-stu-id="34ebe-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="34ebe-139">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="34ebe-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="34ebe-140">=IsError(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="34ebe-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="34ebe-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="34ebe-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="34ebe-p104">Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERROR. Pour élaborer une expression basée sur l’erreur #VALEUR!, utilisez la fonction ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="34ebe-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

