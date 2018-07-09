---
title: Fonction Count (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d931535b-428f-4300-93bf-cfe0ebcc2ac9
description: Renvoie le nombre d’enregistrements dans une table ou requête.
ms.openlocfilehash: 300fcbfd2aa927dd19516355ae28eec2adadf521
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781835"
---
# <a name="count-function-access-custom-web-app"></a><span data-ttu-id="83f4c-103">Fonction Count (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="83f4c-103">Count function (Access custom web app)</span></span>

<span data-ttu-id="83f4c-104">Renvoie le nombre d’enregistrements dans une table ou requête.</span><span class="sxs-lookup"><span data-stu-id="83f4c-104">Returns the number of records in a query or table.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="83f4c-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="83f4c-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="83f4c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83f4c-107">Syntax</span></span>

<span data-ttu-id="83f4c-108">**Nombre** (*Expression*)</span><span class="sxs-lookup"><span data-stu-id="83f4c-108">**Count** (*Expression*)</span></span> 
  
<span data-ttu-id="83f4c-109">La fonction **Count** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="83f4c-109">The **Count** function contains the following argument.</span></span> 
  
|<span data-ttu-id="83f4c-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="83f4c-110">**Argument name**</span></span>|<span data-ttu-id="83f4c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="83f4c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="83f4c-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="83f4c-112">*Expression*</span></span>  <br/> |<span data-ttu-id="83f4c-113">Expression chaîne identifiant le champ qui contient les données que vous souhaitez nombre ou une expression qui effectue un calcul en utilisant les données du champ.</span><span class="sxs-lookup"><span data-stu-id="83f4c-113">A string expression identifying the field that contains the data you want to count or an expression that performs a calculation using the data in the field.</span></span> <span data-ttu-id="83f4c-114">Les opérandes de *l’Expression* peuvent inclure le nom d’un champ de table ou d’une fonction (qui peut être intrinsèque ou définie par l’utilisateur, mais pas d’autres SQL fonctions d’agrégation).</span><span class="sxs-lookup"><span data-stu-id="83f4c-114">Operands in  *Expression*  can include the name of a table field or function (which can be either intrinsic or user-defined but not other SQL aggregate functions).</span></span> <span data-ttu-id="83f4c-115">Vous pouvez compter tous les types de données, y compris du texte.</span><span class="sxs-lookup"><span data-stu-id="83f4c-115">You can count any kind of data, including text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="83f4c-116">Notes</span><span class="sxs-lookup"><span data-stu-id="83f4c-116">Remarks</span></span>

<span data-ttu-id="83f4c-117">Vous pouvez utiliser Count pour compter le nombre d’enregistrements dans une requête sous-jacente.</span><span class="sxs-lookup"><span data-stu-id="83f4c-117">You can use Count to count the number of records in an underlying query.</span></span> <span data-ttu-id="83f4c-118">Par exemple, vous pouvez utiliser Count pour compter le nombre de commandes expédiées vers un pays ou une région.</span><span class="sxs-lookup"><span data-stu-id="83f4c-118">For example, you could use Count to count the number of orders shipped to a particular country or region.</span></span>
  
<span data-ttu-id="83f4c-119">**Nombre** (\*) renvoie le nombre d’éléments dans un groupe.</span><span class="sxs-lookup"><span data-stu-id="83f4c-119">**Count** (\*) returns the number of items in a group.</span></span> <span data-ttu-id="83f4c-120">Cela inclut les valeurs NULL et les doublons.</span><span class="sxs-lookup"><span data-stu-id="83f4c-120">This includes NULL values and duplicates.</span></span> 
  

