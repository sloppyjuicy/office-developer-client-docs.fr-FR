---
title: OU (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combine les deux conditions. Renvoie la valeur TRUE lorsqu’une des deux conditions est remplie.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781953"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="53854-104">OU (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="53854-104">OR (Access custom web app)</span></span>

<span data-ttu-id="53854-105">Combine les deux conditions.</span><span class="sxs-lookup"><span data-stu-id="53854-105">Combines two conditions.</span></span> <span data-ttu-id="53854-106">Renvoie la valeur TRUE lorsqu’une des deux conditions est remplie.</span><span class="sxs-lookup"><span data-stu-id="53854-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="53854-p103">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="53854-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53854-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53854-109">Syntax</span></span>

 <span data-ttu-id="53854-110">*BooleanExpression* **Ou** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="53854-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="53854-111">L’opérateur **Or** utilise l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="53854-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="53854-112">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="53854-112">**Argument name**</span></span>|<span data-ttu-id="53854-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="53854-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="53854-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="53854-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="53854-115">Toute expression valide qui retourne la valeur TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="53854-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53854-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="53854-116">Remarks</span></span>

<span data-ttu-id="53854-117">Lorsque plusieurs opérateurs logiques sont utilisés dans une instruction, **ou** les opérateurs sont évalués après les opérateurs **et** .</span><span class="sxs-lookup"><span data-stu-id="53854-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="53854-118">Toutefois, vous pouvez modifier l’ordre d’évaluation à l’aide de parenthèses.</span><span class="sxs-lookup"><span data-stu-id="53854-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="53854-119">Le tableau suivant montre le résultat de l’opérateur **ou** .</span><span class="sxs-lookup"><span data-stu-id="53854-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="53854-120">**LA VALEUR TRUE**</span><span class="sxs-lookup"><span data-stu-id="53854-120">**TRUE**</span></span>|<span data-ttu-id="53854-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="53854-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="53854-122">**LA VALEUR TRUE**</span><span class="sxs-lookup"><span data-stu-id="53854-122">**TRUE**</span></span> <br/> |<span data-ttu-id="53854-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="53854-123">TRUE</span></span>  <br/> |<span data-ttu-id="53854-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="53854-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="53854-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="53854-125">**FALSE**</span></span> <br/> |<span data-ttu-id="53854-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="53854-126">TRUE</span></span>  <br/> |<span data-ttu-id="53854-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="53854-127">FALSE</span></span>  <br/> |
   

