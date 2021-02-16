---
title: OR (Application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combine deux conditions. Renvoie TRUE lorsque l’une des deux conditions est vraie.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414759"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="67ae2-104">OR (Application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="67ae2-104">OR (Access custom web app)</span></span>

<span data-ttu-id="67ae2-105">Combine deux conditions.</span><span class="sxs-lookup"><span data-stu-id="67ae2-105">Combines two conditions.</span></span> <span data-ttu-id="67ae2-106">Renvoie TRUE lorsque l’une des deux conditions est vraie.</span><span class="sxs-lookup"><span data-stu-id="67ae2-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="67ae2-p103">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="67ae2-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="67ae2-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67ae2-109">Syntax</span></span>

 <span data-ttu-id="67ae2-110">*BooleanExpression* **ou** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="67ae2-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="67ae2-111">**L’opérateur Or** utilise l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="67ae2-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="67ae2-112">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="67ae2-112">**Argument name**</span></span>|<span data-ttu-id="67ae2-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="67ae2-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="67ae2-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="67ae2-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="67ae2-115">Toute expression valide qui renvoie TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="67ae2-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="67ae2-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="67ae2-116">Remarks</span></span>

<span data-ttu-id="67ae2-117">Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, les opérateurs **Or** sont évalués après les opérateurs **And.**</span><span class="sxs-lookup"><span data-stu-id="67ae2-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="67ae2-118">Toutefois, vous pouvez modifier l’ordre d’évaluation à l’aide de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="67ae2-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="67ae2-119">Le tableau suivant indique le résultat de **l’opérateur Or.**</span><span class="sxs-lookup"><span data-stu-id="67ae2-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="67ae2-120">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="67ae2-120">**TRUE**</span></span>|<span data-ttu-id="67ae2-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="67ae2-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="67ae2-122">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="67ae2-122">**TRUE**</span></span> <br/> |<span data-ttu-id="67ae2-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="67ae2-123">TRUE</span></span>  <br/> |<span data-ttu-id="67ae2-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="67ae2-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="67ae2-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="67ae2-125">**FALSE**</span></span> <br/> |<span data-ttu-id="67ae2-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="67ae2-126">TRUE</span></span>  <br/> |<span data-ttu-id="67ae2-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="67ae2-127">FALSE</span></span>  <br/> |
   

