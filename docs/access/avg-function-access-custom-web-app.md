---
title: Fonction Avg (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcule la moyenne arithmétique d'un ensemble de valeurs contenues dans un champ spécifié.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426722"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="1a715-103">Fonction Avg (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="1a715-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="1a715-104">Calcule la moyenne arithmétique d'un ensemble de valeurs contenues dans un champ spécifié.</span><span class="sxs-lookup"><span data-stu-id="1a715-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1a715-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1a715-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1a715-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1a715-107">Syntax</span></span>

 <span data-ttu-id="1a715-108">**AVG (moy** ) (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="1a715-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="1a715-109">La fonction **AVG** contient l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="1a715-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="1a715-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="1a715-110">**Argument**</span></span>|<span data-ttu-id="1a715-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="1a715-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1a715-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="1a715-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="1a715-113">Expression de chaîne identifiant le champ qui contient les données numériques dont vous souhaitez calculer la moyenne ou une expression qui effectue un calcul à l'aide des données de ce champ.</span><span class="sxs-lookup"><span data-stu-id="1a715-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="1a715-114">Les opérandes dans *NumericExpression* peuvent inclure le nom d'un champ de table, une variable ou une fonction (qui peut être intrinsèque ou définie par l'utilisateur, mais pas une des autres fonctions d'agrégation SQL).</span><span class="sxs-lookup"><span data-stu-id="1a715-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1a715-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="1a715-115">Remarks</span></span>

<span data-ttu-id="1a715-p103">La moyenne calculée par **Avg** est la moyenne arithmétique (la somme des valeurs divisée par le nombre de valeurs). Vous pouvez utilisez **Avg**, par exemple, pour calculer des frais de port moyens.</span><span class="sxs-lookup"><span data-stu-id="1a715-p103">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values). You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="1a715-118">La fonction **AVG** n'inclut pas de valeurs **null** dans le calcul.</span><span class="sxs-lookup"><span data-stu-id="1a715-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

