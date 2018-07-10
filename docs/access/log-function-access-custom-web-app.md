---
title: Fonction log (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: Renvoie le logarithme népérien, soit le logarithme népérien de la base de donnée de l’expression spécifiée.
ms.openlocfilehash: 5004b2b32e89a9d68364d271e8b94d72b012a62c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781800"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="7e9b4-103">Fonction log (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="7e9b4-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="7e9b4-104">Renvoie le logarithme népérien, soit le logarithme népérien de la base de donnée de l’expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="7e9b4-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="7e9b4-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7e9b4-107">Syntax</span></span>

 <span data-ttu-id="7e9b4-108">**Journal** (*NumericExpression* , [ *Base* ])</span><span class="sxs-lookup"><span data-stu-id="7e9b4-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="7e9b4-109">La fonction **Log** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="7e9b4-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="7e9b4-110">**Argument name**</span></span>|<span data-ttu-id="7e9b4-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="7e9b4-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="7e9b4-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="7e9b4-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="7e9b4-113">Nombre positif pour lequel vous souhaitez obtenir le logarithme.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="7e9b4-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="7e9b4-114">*Base*</span></span>  <br/> |<span data-ttu-id="7e9b4-115">La base du logarithme.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-115">The base of the logarithm.</span></span> <span data-ttu-id="7e9b4-116">Si tous deux omis, la fonction **Log** renvoie le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7e9b4-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="7e9b4-117">Remarks</span></span>

<span data-ttu-id="7e9b4-118">La fonction **Log10** est similaire, mais toujours renvoie le logarithme népérien, ce qui signifie le logarithme de base 10.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="7e9b4-119">Le logarithme népérien est le logarithme en base e, où f est une constante irrationnelle égale à 2.718281828 environ.</span><span class="sxs-lookup"><span data-stu-id="7e9b4-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

