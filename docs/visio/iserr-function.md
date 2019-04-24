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
description: "Renvoie TRUE si la valeur de cellreference est un type d'erreur, à l'exception de #N/A; dans le cas contraire, elle renvoie la valeur FALSe. La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule."
ms.openlocfilehash: e2117c38d3cad2408295ed6894aefc78e107596e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297248"
---
# <a name="iserr-function"></a><span data-ttu-id="3463c-104">Fonction ISERR</span><span class="sxs-lookup"><span data-stu-id="3463c-104">ISERR Function</span></span>

<span data-ttu-id="3463c-105">Renvoie TRUE si la valeur de _cellreference_ est un type d'erreur, à l'exception de #N/a; dans le cas contraire, elle renvoie la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="3463c-105">Returns TRUE if the value of  _cellreference_ is any error type except #N/A; otherwise, it returns FALSE.</span></span> <span data-ttu-id="3463c-106">La fonction ISERR est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="3463c-106">The ISERR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3463c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3463c-107">Syntax</span></span>

<span data-ttu-id="3463c-108">ISERR (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="3463c-108">ISERR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3463c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3463c-109">Parameters</span></span>

|<span data-ttu-id="3463c-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="3463c-110">**Name**</span></span>|<span data-ttu-id="3463c-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="3463c-111">**Required/Optional**</span></span>|<span data-ttu-id="3463c-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="3463c-112">**Data Type**</span></span>|<span data-ttu-id="3463c-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="3463c-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3463c-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="3463c-114">_cellreference_</span></span> <br/> |<span data-ttu-id="3463c-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="3463c-115">Required</span></span>  <br/> |<span data-ttu-id="3463c-116">**String**</span><span class="sxs-lookup"><span data-stu-id="3463c-116">**String**</span></span> <br/> |<span data-ttu-id="3463c-117">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="3463c-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="3463c-118">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="3463c-118">Example 1</span></span>

|<span data-ttu-id="3463c-119">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3463c-119">**Cell**</span></span>|<span data-ttu-id="3463c-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="3463c-120">**Formula**</span></span>|<span data-ttu-id="3463c-121">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="3463c-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3463c-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="3463c-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3463c-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="3463c-123">=NA( )</span></span>  <br/> |<span data-ttu-id="3463c-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="3463c-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="3463c-125">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="3463c-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="3463c-126">= ISERR (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="3463c-126">=ISERR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="3463c-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="3463c-127">FALSE</span></span>  <br/> |
   
<span data-ttu-id="3463c-p103">Renvoie FALSE parce que l’erreur #N/A! n’est pas reconnue par la fonction ISERR. Utilisez ISERROR pour trouver tous les types d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3463c-p103">Returns FALSE because the #N/A! error is not recognized by the ISERR function. Use ISERROR to find all error types.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="3463c-131">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="3463c-131">Example 2</span></span>

|<span data-ttu-id="3463c-132">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3463c-132">**Cell**</span></span>|<span data-ttu-id="3463c-133">**Formula**</span><span class="sxs-lookup"><span data-stu-id="3463c-133">**Formula**</span></span>|<span data-ttu-id="3463c-134">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="3463c-134">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3463c-135">Scratch. x1</span><span class="sxs-lookup"><span data-stu-id="3463c-135">Scratch.X1</span></span>  <br/> |<span data-ttu-id="3463c-136">= «Maison»</span><span class="sxs-lookup"><span data-stu-id="3463c-136">="House"</span></span>  <br/> |<span data-ttu-id="3463c-137">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="3463c-137">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="3463c-138">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="3463c-138">Scratch.A1</span></span>  <br/> |<span data-ttu-id="3463c-139">= ISERR (Scratch. X1)</span><span class="sxs-lookup"><span data-stu-id="3463c-139">=ISERR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="3463c-140">TRUE</span><span class="sxs-lookup"><span data-stu-id="3463c-140">TRUE</span></span>  <br/> |
   
<span data-ttu-id="3463c-p104">Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERR.</span><span class="sxs-lookup"><span data-stu-id="3463c-p104">Returns TRUE because the #VALUE! error is recognized by the ISERR function.</span></span>
  

