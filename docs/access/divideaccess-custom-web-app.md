---
title: /(Diviser) (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divise un nombre par un autre.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435186"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="d746e-103">/(Diviser) (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="d746e-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="d746e-104">Divise un nombre par un autre.</span><span class="sxs-lookup"><span data-stu-id="d746e-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="d746e-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="d746e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d746e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d746e-107">Syntax</span></span>

 <span data-ttu-id="d746e-108">\*\*  /  \*\* diviseur de dividendes</span><span class="sxs-lookup"><span data-stu-id="d746e-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="d746e-109">*dividende*  Est l'expression numérique à diviser.</span><span class="sxs-lookup"><span data-stu-id="d746e-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="d746e-110">Peut être toute expression valide de n'importe quel type de données de la catégorie numérique, à l'exception du type de données DateTime.</span><span class="sxs-lookup"><span data-stu-id="d746e-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="d746e-111">\*\* Diviseur  Est l'expression numérique qui permet de diviser le dividende.</span><span class="sxs-lookup"><span data-stu-id="d746e-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="d746e-112">Peut être toute expression valide de n'importe quel type de données de la catégorie numérique, à l'exception du type de données DateTime.</span><span class="sxs-lookup"><span data-stu-id="d746e-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="d746e-113">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="d746e-113">Return Type</span></span>

<span data-ttu-id="d746e-114">Renvoie le type de données de l'argument dont la priorité est la plus élevée.</span><span class="sxs-lookup"><span data-stu-id="d746e-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="d746e-115">Si un nombre \*\* entier dividende est divisé par un diviseur entier, le résultat est un entier dont la partie fractionnaire du résultat est tronquée. \*\*</span><span class="sxs-lookup"><span data-stu-id="d746e-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d746e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="d746e-116">Remarks</span></span>

<span data-ttu-id="d746e-117">La valeur réelle renvoyée par l'opérateur/est le quotient de la première expression divisée par la deuxième expression.</span><span class="sxs-lookup"><span data-stu-id="d746e-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

