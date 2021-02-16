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
description: 'Renvoie TRUE si la valeur de cellreference est un type d’erreur à l’exception #N/A ; Sinon, elle renvoie FALSE. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.'
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432106"
---
# <a name="iserr-function"></a><span data-ttu-id="ac60e-104">Fonction ISERR</span><span class="sxs-lookup"><span data-stu-id="ac60e-104">ISERR Function</span></span>

<span data-ttu-id="ac60e-105">Renvoie TRUE si la valeur de  _cellreference_ est un type d’erreur à l’exception #N/A ; Sinon, elle renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="ac60e-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="ac60e-106">La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="ac60e-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ac60e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ac60e-107">Syntax</span></span>

<span data-ttu-id="ac60e-108">ISERR(\*\* *cellreference* \*\* )</span><span class="sxs-lookup"><span data-stu-id="ac60e-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ac60e-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ac60e-109">Parameters</span></span>

|<span data-ttu-id="ac60e-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="ac60e-110">**Name**</span></span>|<span data-ttu-id="ac60e-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="ac60e-111">**Required/Optional**</span></span>|<span data-ttu-id="ac60e-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="ac60e-112">**Data Type**</span></span>|<span data-ttu-id="ac60e-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="ac60e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ac60e-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="ac60e-114">_cellreference_</span></span> <br/> |<span data-ttu-id="ac60e-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="ac60e-115">Required</span></span>  <br/> |<span data-ttu-id="ac60e-116">**String**</span><span class="sxs-lookup"><span data-stu-id="ac60e-116">**String**</span></span> <br/> |<span data-ttu-id="ac60e-117">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="ac60e-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="ac60e-118">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="ac60e-118">Example 1</span></span>

|<span data-ttu-id="ac60e-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ac60e-119">**Cell**</span></span>|<span data-ttu-id="ac60e-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="ac60e-120">**Formula**</span></span>|<span data-ttu-id="ac60e-121">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="ac60e-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac60e-122">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="ac60e-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="ac60e-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="ac60e-123">=NA( )</span></span>  <br/> |<span data-ttu-id="ac60e-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="ac60e-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="ac60e-125">Scratch.B1</span><span class="sxs-lookup"><span data-stu-id="ac60e-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="ac60e-126">=ISERR(Scratch.A1)</span><span class="sxs-lookup"><span data-stu-id="ac60e-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="ac60e-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="ac60e-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="ac60e-p103">Renvoie FALSE parce que l’erreur #N/A! n’est pas reconnue par la fonction ISERR. Utilisez ISERROR pour trouver tous les types d’erreur.</span><span class="sxs-lookup"><span data-stu-id="ac60e-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ac60e-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="ac60e-131">Example 2</span></span>

|<span data-ttu-id="ac60e-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="ac60e-132">**Cell**</span></span>|<span data-ttu-id="ac60e-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="ac60e-133">**Formula**</span></span>|<span data-ttu-id="ac60e-134">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="ac60e-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac60e-135">Scratch.X1</span><span class="sxs-lookup"><span data-stu-id="ac60e-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="ac60e-136">="House »</span><span class="sxs-lookup"><span data-stu-id="ac60e-136">="House"</span></span>  <br/> |<span data-ttu-id="ac60e-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="ac60e-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="ac60e-138">Scratch.A1</span><span class="sxs-lookup"><span data-stu-id="ac60e-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="ac60e-139">=ISERR(Scratch.X1)</span><span class="sxs-lookup"><span data-stu-id="ac60e-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="ac60e-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="ac60e-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="ac60e-p104">Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERR.</span><span class="sxs-lookup"><span data-stu-id="ac60e-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

