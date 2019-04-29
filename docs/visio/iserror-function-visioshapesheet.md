---
title: ISERROR Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251452
localization_priority: Normal
ms.assetid: 4864ebc2-fee6-2415-7c59-e0af8611f8d6
description: Renvoie TRUE si la valeur de cellreference est n'importe quel type d'erreur; dans le cas contraire, elle renvoie la valeur FALSe. La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.
ms.openlocfilehash: a07b2345858e36dc2e4514d7e4f0f0d653491b50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421542"
---
# <a name="iserror-function-visioshapesheet"></a><span data-ttu-id="065a1-104">ISERROR Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="065a1-104">ISERROR Function (VisioShapeSheet)</span></span>

<span data-ttu-id="065a1-105">Renvoie TRUE si la valeur de _cellreference_ est n'importe quel type d'erreur; dans le cas contraire, elle renvoie la valeur FALSe.</span><span class="sxs-lookup"><span data-stu-id="065a1-105">Returns TRUE if the value of  _cellreference_ is any error type; otherwise, it returns FALSE.</span></span> <span data-ttu-id="065a1-106">La fonction ISERROR est utilisée dans les formules qui font référence à une autre cellule.</span><span class="sxs-lookup"><span data-stu-id="065a1-106">The ISERROR function is used in formulas that refer to another cell.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="065a1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="065a1-107">Syntax</span></span>

<span data-ttu-id="065a1-108">ISERROR (\* \* *cellreference* \* \*)</span><span class="sxs-lookup"><span data-stu-id="065a1-108">ISERROR(\*\* *cellreference* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="065a1-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="065a1-109">Parameters</span></span>

|<span data-ttu-id="065a1-110">**Nom**</span><span class="sxs-lookup"><span data-stu-id="065a1-110">**Name**</span></span>|<span data-ttu-id="065a1-111">**Requis/Facultatif**</span><span class="sxs-lookup"><span data-stu-id="065a1-111">**Required/Optional**</span></span>|<span data-ttu-id="065a1-112">**Type de données**</span><span class="sxs-lookup"><span data-stu-id="065a1-112">**Data Type**</span></span>|<span data-ttu-id="065a1-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="065a1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="065a1-114">_cellreference_</span><span class="sxs-lookup"><span data-stu-id="065a1-114">_cellreference_</span></span> <br/> |<span data-ttu-id="065a1-115">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="065a1-115">Required</span></span>  <br/> |<span data-ttu-id="065a1-116">**String**</span><span class="sxs-lookup"><span data-stu-id="065a1-116">**String**</span></span> <br/> |<span data-ttu-id="065a1-117">Référence à une cellule</span><span class="sxs-lookup"><span data-stu-id="065a1-117">Reference to a cell.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="065a1-118">Exemple 1</span><span class="sxs-lookup"><span data-stu-id="065a1-118">Example 1</span></span>

|<span data-ttu-id="065a1-119">**Cellule**</span><span class="sxs-lookup"><span data-stu-id="065a1-119">**Cell**</span></span>|<span data-ttu-id="065a1-120">**Formula**</span><span class="sxs-lookup"><span data-stu-id="065a1-120">**Formula**</span></span>|<span data-ttu-id="065a1-121">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="065a1-121">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="065a1-122">Scratch. a1</span><span class="sxs-lookup"><span data-stu-id="065a1-122">Scratch.A1</span></span>  <br/> |<span data-ttu-id="065a1-123">=NA( )</span><span class="sxs-lookup"><span data-stu-id="065a1-123">=NA( )</span></span>  <br/> |<span data-ttu-id="065a1-124">#N/A!</span><span class="sxs-lookup"><span data-stu-id="065a1-124">#N/A!</span></span>  <br/> |
|<span data-ttu-id="065a1-125">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="065a1-125">Scratch.B1</span></span>  <br/> |<span data-ttu-id="065a1-126">= ESTERREUR (Scratch. a1)</span><span class="sxs-lookup"><span data-stu-id="065a1-126">=ISERROR(Scratch.A1)</span></span>  <br/> |<span data-ttu-id="065a1-127">TRUE</span><span class="sxs-lookup"><span data-stu-id="065a1-127">TRUE</span></span>  <br/> |
   
<span data-ttu-id="065a1-p103">Renvoie TRUE parce que l’erreur #N/A! est reconnue par la fonction ISERROR. Vous pouvez utiliser ISERR pour trouver tous les types d’erreur à l’exception de l’erreur #N/A!.</span><span class="sxs-lookup"><span data-stu-id="065a1-p103">Returns TRUE because the #N/A! error is recognized by the ISERROR function. You can use ISERR to find all types but the #N/A! error.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="065a1-132">Exemple 2</span><span class="sxs-lookup"><span data-stu-id="065a1-132">Example 2</span></span>

|<span data-ttu-id="065a1-133">**Cellule**</span><span class="sxs-lookup"><span data-stu-id="065a1-133">**Cell**</span></span>|<span data-ttu-id="065a1-134">**Formula**</span><span class="sxs-lookup"><span data-stu-id="065a1-134">**Formula**</span></span>|<span data-ttu-id="065a1-135">**Valeur renvoyée**</span><span class="sxs-lookup"><span data-stu-id="065a1-135">**Value returned**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="065a1-136">Scratch. x1</span><span class="sxs-lookup"><span data-stu-id="065a1-136">Scratch.X1</span></span>  <br/> |<span data-ttu-id="065a1-137">= «Maison»</span><span class="sxs-lookup"><span data-stu-id="065a1-137">="House"</span></span>  <br/> |<span data-ttu-id="065a1-138">#VALUE!</span><span class="sxs-lookup"><span data-stu-id="065a1-138">#VALUE!</span></span>  <br/> |
|<span data-ttu-id="065a1-139">Scratch. B1</span><span class="sxs-lookup"><span data-stu-id="065a1-139">Scratch.B1</span></span>  <br/> |<span data-ttu-id="065a1-140">= ESTERREUR (Scratch. X1)</span><span class="sxs-lookup"><span data-stu-id="065a1-140">=ISERROR(Scratch.X1)</span></span>  <br/> |<span data-ttu-id="065a1-141">TRUE</span><span class="sxs-lookup"><span data-stu-id="065a1-141">TRUE</span></span>  <br/> |
   
<span data-ttu-id="065a1-p104">Renvoie TRUE parce que l’erreur #VALEUR! est reconnue par la fonction ISERROR. Pour élaborer une expression basée sur l’erreur #VALEUR!, utilisez la fonction ISERRVALUE.</span><span class="sxs-lookup"><span data-stu-id="065a1-p104">Returns TRUE because the #VALUE! error is recognized by the ISERROR function. To build an expression based on the #VALUE! error, use the ISERRVALUE function.</span></span>
  

