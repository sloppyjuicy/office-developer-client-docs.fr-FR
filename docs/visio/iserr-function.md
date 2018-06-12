---
title: ISERR, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251448
localization_priority: Normal
ms.assetid: 87508007-8ad2-3bcf-55dc-f0207c7c6fe3
description: 'Renvoie la valeur TRUE si la valeur de cellreference est une erreur à l’exception de # n/a ; dans le cas contraire, elle renvoie la valeur FALSE. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: 651b095e53b7f2690aa9c8774d87d5afcede75be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19788852"
---
# <a name="iserr-function"></a><span data-ttu-id="62585-104">ISERR, fonction</span><span class="sxs-lookup"><span data-stu-id="62585-104">ISERR Function</span></span>

<span data-ttu-id="62585-105">Renvoie la valeur TRUE si la valeur de _cellreference_ est une erreur à l’exception de # n/a ; dans le cas contraire, elle renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="62585-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="62585-106">La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="62585-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62585-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62585-107">Syntax</span></span>

<span data-ttu-id="62585-108">ISERR (** *cellreference* **)</span><span class="sxs-lookup"><span data-stu-id="62585-108">ISERR(** *cellreference* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="62585-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="62585-109">Parameters</span></span>

|<span data-ttu-id="62585-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="62585-110">**Name**</span></span>|<span data-ttu-id="62585-111">**Obligatoire/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="62585-111">**Required/Optional**</span></span>|<span data-ttu-id="62585-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="62585-112">**Data Type**</span></span>|<span data-ttu-id="62585-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="62585-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="62585-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="62585-114">_cellreference_</span></span> <br/> |<span data-ttu-id="62585-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="62585-115">Required</span></span>  <br/> |<span data-ttu-id="62585-116">**Chaîne**</span><span class="sxs-lookup"><span data-stu-id="62585-116">**String**</span></span> <br/> |<span data-ttu-id="62585-117">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="62585-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="62585-118">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="62585-118">Example 1</span></span>

|<span data-ttu-id="62585-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="62585-119">**Cell**</span></span>|<span data-ttu-id="62585-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="62585-120">**Formula**</span></span>|<span data-ttu-id="62585-121">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="62585-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="62585-122">Cellule Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="62585-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="62585-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="62585-123">=NA( )</span></span>  <br/> |<span data-ttu-id="62585-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="62585-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="62585-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="62585-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="62585-126">=ISERR(Scratch.a1)</span><span class="sxs-lookup"><span data-stu-id="62585-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="62585-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="62585-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="62585-p103">Renvoie FALSE parce que l’erreur #N/A! n’est pas reconnue par la fonction ISERR. Utilisez ISERROR pour trouver tous les types d’erreur.</span><span class="sxs-lookup"><span data-stu-id="62585-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="62585-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="62585-131">Example 2</span></span>

|<span data-ttu-id="62585-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="62585-132">**Cell**</span></span>|<span data-ttu-id="62585-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="62585-133">**Formula**</span></span>|<span data-ttu-id="62585-134">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="62585-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="62585-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="62585-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="62585-136">="Maison"</span><span class="sxs-lookup"><span data-stu-id="62585-136">="House"</span></span>  <br/> |<span data-ttu-id="62585-137">#VALEUR!</span><span class="sxs-lookup"><span data-stu-id="62585-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="62585-138">Cellule Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="62585-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="62585-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="62585-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="62585-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="62585-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="62585-p104">Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERR.</span><span class="sxs-lookup"><span data-stu-id="62585-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

