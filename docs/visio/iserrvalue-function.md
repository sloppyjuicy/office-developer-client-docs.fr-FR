---
title: ISERRVALUE, fonction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251453
localization_priority: Normal
ms.assetid: c7feec6f-f47a-60ee-b056-7b2dc51ed9a9
description: 'Renvoie TRUE si la valeur de cellreference est de type erreur #VALUE, où un argument dans la formule est du type erroné. La fonction ISERRVALUE est utilisée dans les expressions logiques qui font référence à une autre cellule.'
ms.openlocfilehash: 62058522dc8a2387aec9867e4892da740aba9b44
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404427"
---
# <a name="iserrvalue-function"></a><span data-ttu-id="68e53-104">Fonction ISERRVALUE</span><span class="sxs-lookup"><span data-stu-id="68e53-104">ISERRVALUE Function</span></span>

<span data-ttu-id="68e53-105">Renvoie TRUE si la valeur de  _cellreference_ est de type #VALUE, où un argument dans la formule est du type erroné.</span><span class="sxs-lookup"><span data-stu-id="68e53-105">Returns TRUE if the value of  _cellreference_ is error type #VALUE, where an argument in the formula is the wrong type.</span></span> <span data-ttu-id="68e53-106">La fonction ISERRVALUE est utilisée dans les expressions logiques qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="68e53-106">The ISERRVALUE function is used in logical expressions that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="68e53-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="68e53-107">Syntax</span></span>

<span data-ttu-id="68e53-108">ISERRVALUE(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="68e53-108">ISERRVALUE(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="68e53-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="68e53-109">Parameters</span></span>

|<span data-ttu-id="68e53-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="68e53-110">**Name**</span></span>|<span data-ttu-id="68e53-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="68e53-111">**Required/Optional**</span></span>|<span data-ttu-id="68e53-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="68e53-112">**Data Type**</span></span>|<span data-ttu-id="68e53-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="68e53-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="68e53-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="68e53-114">_cellreference_</span></span> <br/> |<span data-ttu-id="68e53-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="68e53-115">Required</span></span>  <br/> |<span data-ttu-id="68e53-116">**String**</span><span class="sxs-lookup"><span data-stu-id="68e53-116">**String**</span></span> <br/> |<span data-ttu-id="68e53-117">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="68e53-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68e53-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="68e53-118">Remarks</span></span>

<span data-ttu-id="68e53-p103">Les cellules Montage de A à D ne renvoient pas l’erreur #VALEUR! parce que la formule peut contenir des nombres et des lettres dans une même chaîne. Toutefois, les cellules X et Y ne doivent contenir que des nombres.</span><span class="sxs-lookup"><span data-stu-id="68e53-p103">Scratch cells A through D won't return a #VALUE! error because the formula can contain numbers and letters in the same string. Cells X and Y must contain numbers only.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="68e53-122">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="68e53-122">Example 1</span></span>

|<span data-ttu-id="68e53-123">**Cell**</span><span class="sxs-lookup"><span data-stu-id="68e53-123">**Cell**</span></span>|<span data-ttu-id="68e53-124">**Formula**</span><span class="sxs-lookup"><span data-stu-id="68e53-124">**Formula**</span></span>|<span data-ttu-id="68e53-125">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="68e53-125">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68e53-126">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="68e53-126">Scratch.X1</span></span>  <br/> |<span data-ttu-id="68e53-127">="Maison"</span><span class="sxs-lookup"><span data-stu-id="68e53-127">= "House"</span></span>  <br/> |<span data-ttu-id="68e53-128">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="68e53-128">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="68e53-129">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="68e53-129">Scratch.A1</span></span>  <br/> |<span data-ttu-id="68e53-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="68e53-130">= If (ISERRVALUE(Scratch.X1),2,Scratch.X1)</span></span>  <br/> |<span data-ttu-id="68e53-131">2</span><span class="sxs-lookup"><span data-stu-id="68e53-131">2</span></span>  <br/> |
   
<span data-ttu-id="68e53-p104">Renvoie 2 parce que la valeur renvoyée est une erreur #VALEUR! et l’expression demande à Microsoft Visio de renvoyer un 2 à la place de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="68e53-p104">Returns 2 because the value returned is a #VALUE! error, and the expression instructs Microsoft Visio to return a 2 in place of the error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="68e53-134">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="68e53-134">Example 2</span></span>

|<span data-ttu-id="68e53-135">**Cell**</span><span class="sxs-lookup"><span data-stu-id="68e53-135">**Cell**</span></span>|<span data-ttu-id="68e53-136">**Formula**</span><span class="sxs-lookup"><span data-stu-id="68e53-136">**Formula**</span></span>|<span data-ttu-id="68e53-137">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="68e53-137">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68e53-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="68e53-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="68e53-139">="5 + 7"</span><span class="sxs-lookup"><span data-stu-id="68e53-139">="5 + 7"</span></span>  <br/> |<span data-ttu-id="68e53-140">5 + 7</span><span class="sxs-lookup"><span data-stu-id="68e53-140">5 + 7</span></span>  <br/> |
|<span data-ttu-id="68e53-141">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="68e53-141">Scratch.B1</span></span>  <br/> |<span data-ttu-id="68e53-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="68e53-142">=If (ISERRVALUE(Scratch.A1),2,Scratch.A1)</span></span>  <br/> |<span data-ttu-id="68e53-143">5 + 7</span><span class="sxs-lookup"><span data-stu-id="68e53-143">5 + 7</span></span>  <br/> |
   
<span data-ttu-id="68e53-p105">Renvoie 12 parce que la valeur renvoyée n’est pas une erreur #VALEUR! et l’expression demande à Visio de renvoyer la valeur de la cellule d’origine.</span><span class="sxs-lookup"><span data-stu-id="68e53-p105">Returns 12 because the value returned is not a #VALUE! error, and the expression instructs Visio to return the value of the original cell.</span></span>
  

