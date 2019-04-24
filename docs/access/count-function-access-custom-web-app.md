---
title: Fonction count (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Renvoie le nombre d'enregistrements dans une requête ou une table.
ms.openlocfilehash: 98dbed393bf2f6dc401119f6c5dc7ab6b5ff7864
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282235"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="591ce-103">Fonction count (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="591ce-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="591ce-104">Renvoie le nombre d'enregistrements dans une requête ou une table.</span><span class="sxs-lookup"><span data-stu-id="591ce-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="591ce-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="591ce-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="591ce-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="591ce-107">Syntax</span></span>

<span data-ttu-id="591ce-108">**Nombre** (*Expression*)</span><span class="sxs-lookup"><span data-stu-id="591ce-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="591ce-109">La fonction **Count** contient l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="591ce-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="591ce-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="591ce-110">**Argument name**</span></span>|<span data-ttu-id="591ce-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="591ce-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="591ce-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="591ce-112">*Expression*</span></span>  <br/> |<span data-ttu-id="591ce-113">Expression de chaîne identifiant le champ qui contient les données que vous souhaitez compter ou une expression qui effectue un calcul à l'aide des données du champ.</span><span class="sxs-lookup"><span data-stu-id="591ce-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="591ce-114">Les opérandes dans *expression* peuvent inclure le nom d'un champ de table ou une fonction (qui peut être intrinsèque ou définie par l'utilisateur, mais pas avec d'autres fonctions d'agrégation SQL).</span><span class="sxs-lookup"><span data-stu-id="591ce-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="591ce-115">Vous pouvez compter tous les types de données, y compris du texte.</span><span class="sxs-lookup"><span data-stu-id="591ce-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="591ce-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="591ce-116">Remarks</span></span>

<span data-ttu-id="591ce-117">Vous pouvez utiliser Count pour compter le nombres d'enregistrements dans une requête sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="591ce-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="591ce-118">Par exemple, vous pouvez utiliser Count pour compter le nombre de commandes expédiées vers un pays ou une région spécifique.</span><span class="sxs-lookup"><span data-stu-id="591ce-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="591ce-119">**Nombre** (\*) renvoie le nombre d'éléments dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="591ce-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="591ce-120">Cela inclut les valeurs NULL et les doublons.</span><span class="sxs-lookup"><span data-stu-id="591ce-120">This includes NULL values and duplicates.</span></span> 
  

