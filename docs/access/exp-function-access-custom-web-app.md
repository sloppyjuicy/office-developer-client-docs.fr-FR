---
title: Fonction exp (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Renvoie la valeur exponentielle de l'expression spécifiée.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436411"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="316c0-103">Fonction exp (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="316c0-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="316c0-104">Renvoie la valeur exponentielle de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="316c0-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="316c0-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="316c0-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="316c0-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="316c0-107">Syntax</span></span>

 <span data-ttu-id="316c0-108">**Exp** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="316c0-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="316c0-109">La fonction **exp** contient l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="316c0-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="316c0-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="316c0-110">**Argument name**</span></span>|<span data-ttu-id="316c0-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="316c0-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="316c0-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="316c0-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="316c0-113">Expression de type double ou d'un type pouvant être converti implicitement en double.</span><span class="sxs-lookup"><span data-stu-id="316c0-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="316c0-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="316c0-114">Remarks</span></span>

<span data-ttu-id="316c0-115">La constante **e** (2,718281...) est la base des logarithmes naturels.</span><span class="sxs-lookup"><span data-stu-id="316c0-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="316c0-116">L'exposant d'un nombre est la constante **e** élevée à la puissance du nombre.</span><span class="sxs-lookup"><span data-stu-id="316c0-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="316c0-117">Par exemple **exp** (1,0) = e ^ 1.0 = 2.71828182845905 et **exp** (10) = e ^ 10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="316c0-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="316c0-118">La valeur exponentielle du logarithme népérien d'un nombre est le nombre lui-même: **exp** (log (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="316c0-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="316c0-119">Et le logarithme népérien de l'exponentiel d'un nombre est le numéro lui-même: LOG (**exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="316c0-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

