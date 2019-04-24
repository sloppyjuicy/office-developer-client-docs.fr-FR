---
title: /(Diviser) (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divise un nombre par un autre.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308259"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="f2a41-103">/(Diviser) (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="f2a41-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="f2a41-104">Divise un nombre par un autre.</span><span class="sxs-lookup"><span data-stu-id="f2a41-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f2a41-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="f2a41-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f2a41-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2a41-107">Syntax</span></span>

 <span data-ttu-id="f2a41-108">\*\*  /  \*\* diviseur de dividendes</span><span class="sxs-lookup"><span data-stu-id="f2a41-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="f2a41-109">*dividende*  Est l'expression numérique à diviser.</span><span class="sxs-lookup"><span data-stu-id="f2a41-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="f2a41-110">Peut être toute expression valide de n'importe quel type de données de la catégorie numérique, à l'exception du type de données DateTime.</span><span class="sxs-lookup"><span data-stu-id="f2a41-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="f2a41-111">\*\* Diviseur  Est l'expression numérique qui permet de diviser le dividende.</span><span class="sxs-lookup"><span data-stu-id="f2a41-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="f2a41-112">Peut être toute expression valide de n'importe quel type de données de la catégorie numérique, à l'exception du type de données DateTime.</span><span class="sxs-lookup"><span data-stu-id="f2a41-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="f2a41-113">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="f2a41-113">Return Type</span></span>

<span data-ttu-id="f2a41-114">Renvoie le type de données de l'argument dont la priorité est la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="f2a41-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="f2a41-115">Si un nombre \*\* entier dividende est divisé par un diviseur entier, le résultat est un entier dont la partie fractionnaire du résultat est tronquée. \*\*</span><span class="sxs-lookup"><span data-stu-id="f2a41-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f2a41-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="f2a41-116">Remarks</span></span>

<span data-ttu-id="f2a41-117">La valeur réelle renvoyée par l'opérateur/est le quotient de la première expression divisée par la deuxième expression.</span><span class="sxs-lookup"><span data-stu-id="f2a41-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

