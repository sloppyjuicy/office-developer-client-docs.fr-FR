---
title: Égal à (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compare l'égalité de deux expressions.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308224"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="c3fa8-103">Égal à (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="c3fa8-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="c3fa8-104">Compare l'égalité de deux expressions.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c3fa8-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c3fa8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c3fa8-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="c3fa8-108">*expression*  =  *expression*</span><span class="sxs-lookup"><span data-stu-id="c3fa8-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="c3fa8-109">*expression*  représente toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="c3fa8-110">Si les expressions n'ont pas le même type de données, le type de données d'une expression doit être implicitement convertible vers le type de données de l'autre.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="c3fa8-111">La conversion varie en fonction des règles de priorité des types de données.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="c3fa8-112">Type renvoyé</span><span class="sxs-lookup"><span data-stu-id="c3fa8-112">Return Type</span></span>

<span data-ttu-id="c3fa8-113">**Booléen**</span><span class="sxs-lookup"><span data-stu-id="c3fa8-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3fa8-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="c3fa8-114">Remarks</span></span>

<span data-ttu-id="c3fa8-115">Lorsque vous comparez deux expressions de type NULL, le résultat est TRUE.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="c3fa8-116">La comparaison de NULL à une valeur non NULL aboutit toujours à FALSe.</span><span class="sxs-lookup"><span data-stu-id="c3fa8-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

