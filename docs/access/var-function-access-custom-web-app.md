---
title: Var Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Renvoie la variation statistique d’un échantillon de population représenté sous la mesure d’un ensemble de valeurs contenues dans un champ spécifié dans une requête.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437755"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="8511c-103">Var Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="8511c-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="8511c-104">Renvoie la variation statistique d’un échantillon de population représenté sous la mesure d’un ensemble de valeurs contenues dans un champ spécifié dans une requête.</span><span class="sxs-lookup"><span data-stu-id="8511c-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="8511c-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="8511c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8511c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8511c-107">Syntax</span></span>

 <span data-ttu-id="8511c-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="8511c-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="8511c-109">La **fonction Var** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="8511c-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="8511c-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="8511c-110">**Argument name**</span></span>|<span data-ttu-id="8511c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8511c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8511c-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="8511c-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="8511c-113">Expression de texte identifiant le champ qui contient les données numériques à évaluer ou expression qui effectue un calcul à l’aide des données de ce champ.</span><span class="sxs-lookup"><span data-stu-id="8511c-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="8511c-114">Les opérandes dans *NumericExpression* peuvent inclure le nom d’un champ de table, d’une constante ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas l’une des autres fonctions d’agrégation SQL).</span><span class="sxs-lookup"><span data-stu-id="8511c-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8511c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="8511c-115">Remarks</span></span>

 <span data-ttu-id="8511c-116">**Var** ne peut être utilisé qu’avec des colonnes numériques.</span><span class="sxs-lookup"><span data-stu-id="8511c-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="8511c-117">Les valeurs Null sont ignorées.</span><span class="sxs-lookup"><span data-stu-id="8511c-117">Null values are ignored.</span></span> 
  

