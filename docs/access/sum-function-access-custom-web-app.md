---
title: Sum Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Renvoie la somme de toutes les valeurs de l’expression.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427100"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="78fd1-103">Sum Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="78fd1-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="78fd1-104">Renvoie la somme de toutes les valeurs de l’expression.</span><span class="sxs-lookup"><span data-stu-id="78fd1-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="78fd1-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="78fd1-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="78fd1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="78fd1-107">Syntax</span></span>

 <span data-ttu-id="78fd1-108">**Sum** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="78fd1-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="78fd1-109">La **fonction Sum** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="78fd1-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="78fd1-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="78fd1-110">**Argument name**</span></span>|<span data-ttu-id="78fd1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="78fd1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="78fd1-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="78fd1-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="78fd1-113">Expression identifiant le champ qui contient les données numériques à ajouter ou expression qui effectue un calcul à l’aide des données de ce champ.</span><span class="sxs-lookup"><span data-stu-id="78fd1-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="78fd1-114">Les opérandes dans  *NumericExpression*  peuvent inclure le nom d’un champ de table, d’une constante ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas une des autres fonctions d’agrégation SQL).</span><span class="sxs-lookup"><span data-stu-id="78fd1-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78fd1-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="78fd1-115">Remarks</span></span>

<span data-ttu-id="78fd1-116">La **fonction Sum** ignore les enregistrements qui contiennent des valeurs Null.</span><span class="sxs-lookup"><span data-stu-id="78fd1-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="78fd1-117">La **fonction Sum** ne peut être utilisée qu’avec des colonnes numériques.</span><span class="sxs-lookup"><span data-stu-id="78fd1-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

