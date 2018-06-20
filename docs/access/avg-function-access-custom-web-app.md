---
title: Fonction AVG (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcule la moyenne arithmétique d’un ensemble de valeurs contenues dans un champ spécifié.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781815"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="297ed-103">Fonction AVG (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="297ed-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="297ed-104">Calcule la moyenne arithmétique d’un ensemble de valeurs contenues dans un champ spécifié.</span><span class="sxs-lookup"><span data-stu-id="297ed-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="297ed-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="297ed-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="297ed-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="297ed-107">Syntax</span></span>

 <span data-ttu-id="297ed-108">**Avg** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="297ed-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="297ed-109">La fonction **Avg** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="297ed-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="297ed-110">**Argument**</span><span class="sxs-lookup"><span data-stu-id="297ed-110">**Argument**</span></span>|<span data-ttu-id="297ed-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="297ed-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="297ed-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="297ed-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="297ed-113">Expression chaîne identifiant le champ qui contient les données numériques que vous voulez la moyenne ou une expression qui effectue un calcul à l’aide des données dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="297ed-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="297ed-114">Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, une variable ou une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL).</span><span class="sxs-lookup"><span data-stu-id="297ed-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="297ed-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="297ed-115">Remarks</span></span>

<span data-ttu-id="297ed-116">La moyenne calculée par **Avg** est la moyenne arithmétique (somme des valeurs divisée par le nombre de valeurs).</span><span class="sxs-lookup"><span data-stu-id="297ed-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="297ed-117">Vous pouvez utiliser **Avg**, par exemple, pour calculer la moyenne des frais.</span><span class="sxs-lookup"><span data-stu-id="297ed-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="297ed-118">La fonction **Avg** n’inclut pas toutes les valeurs **Null** dans le calcul.</span><span class="sxs-lookup"><span data-stu-id="297ed-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

