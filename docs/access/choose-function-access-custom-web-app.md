---
title: Choose function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70c1ac24-a28f-4401-91d3-61129578bebd
description: Renvoie l’élément à l’index spécifié à partir d’une liste de valeurs.
ms.openlocfilehash: e44655b9c2f4055f1f3dc57befa8adc6884c43b6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414115"
---
# <a name="choose-function-access-custom-web-app"></a><span data-ttu-id="aed29-103">Choose function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="aed29-103">Choose function (Access custom web app)</span></span>

<span data-ttu-id="aed29-104">Renvoie l’élément à l’index spécifié à partir d’une liste de valeurs.</span><span class="sxs-lookup"><span data-stu-id="aed29-104">Returns the item at the specified index from a list of values.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="aed29-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="aed29-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aed29-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="aed29-107">Syntax</span></span>

<span data-ttu-id="aed29-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span><span class="sxs-lookup"><span data-stu-id="aed29-108">**Choose** (*IndexNumber*, *Value*, [*Value_n*])</span></span> 
  
<span data-ttu-id="aed29-109">La **fonction Choose** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="aed29-109">The **Choose** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="aed29-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="aed29-110">**Argument name**</span></span>|<span data-ttu-id="aed29-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="aed29-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="aed29-112">*IndexNumber*</span><span class="sxs-lookup"><span data-stu-id="aed29-112">*IndexNumber*</span></span>  <br/> |<span data-ttu-id="aed29-113">Expression d’un nombre integer qui représente un index de base 1 dans la liste des éléments qui le suivent.</span><span class="sxs-lookup"><span data-stu-id="aed29-113">An integer expression that represents a 1-based index into the list of the items following it.</span></span>  <br/> |
| <span data-ttu-id="aed29-114">*Valeur*</span><span class="sxs-lookup"><span data-stu-id="aed29-114">*Value*</span></span>  <br/> |<span data-ttu-id="aed29-115">Liste des valeurs de n’importe quel type de données.</span><span class="sxs-lookup"><span data-stu-id="aed29-115">List of values of any data type.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aed29-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="aed29-116">Remarks</span></span>

<span data-ttu-id="aed29-117">Si  *IndexNumber fourni n’est*  pas un nombre nombre, la valeur est implicitement convertie en un nombre.</span><span class="sxs-lookup"><span data-stu-id="aed29-117">If the provided  *IndexNumber*  is not an integer, then the value is implicitly converted to an integer.</span></span> 
  
<span data-ttu-id="aed29-118">Si la valeur d’index dépasse les limites du tableau de valeurs, **Choose** renvoie la valeur NULL.</span><span class="sxs-lookup"><span data-stu-id="aed29-118">If the index value exceeds the bounds of the array of values, **Choose** returns NULL.</span></span> 
  

