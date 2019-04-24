---
title: Fonction Round (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4af7fbe2-ee34-4a52-b55e-ce3983313b5e
description: Renvoie une valeur numérique, arrondie ou tronquée, à la longueur ou à la précision spécifiée.
ms.openlocfilehash: 0afab8c3434aef58c4bb25aee22eefd95732797b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307958"
---
# <a name="round-function-access-custom-web-app"></a><span data-ttu-id="13d1f-103">Fonction Round (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="13d1f-103">Round Function (Access custom web app)</span></span>

<span data-ttu-id="13d1f-104">Renvoie une valeur numérique, arrondie ou tronquée, à la longueur ou à la précision spécifiée.</span><span class="sxs-lookup"><span data-stu-id="13d1f-104">Returns a numeric value, either rounded or truncated, to the specified length or precision.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="13d1f-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="13d1f-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="13d1f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="13d1f-107">Syntax</span></span>

 <span data-ttu-id="13d1f-108">**Arrondi** (*Nombre*, *précision* , [ *TruncateInsteadOfRound* ])</span><span class="sxs-lookup"><span data-stu-id="13d1f-108">**Round** (*Number*, *Precision*  , [  *TruncateInsteadOfRound*  ])</span></span> 
  
<span data-ttu-id="13d1f-109">La fonction **Round** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="13d1f-109">The **Round** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="13d1f-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="13d1f-110">**Argument name**</span></span>|<span data-ttu-id="13d1f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="13d1f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="13d1f-112">*Number*</span><span class="sxs-lookup"><span data-stu-id="13d1f-112">*Number*</span></span>  <br/> |<span data-ttu-id="13d1f-113">Expression numérique.</span><span class="sxs-lookup"><span data-stu-id="13d1f-113">A numeric expression.</span></span>  <br/> |
| <span data-ttu-id="13d1f-114">*Dell*</span><span class="sxs-lookup"><span data-stu-id="13d1f-114">*Precision*</span></span>  <br/> |<span data-ttu-id="13d1f-115">Précision à laquelle le *nombre* doit être arrondi.</span><span class="sxs-lookup"><span data-stu-id="13d1f-115">The precision to which  *Number*  is to be rounded.</span></span>  <span data-ttu-id="13d1f-116">La *précision* doit être une expression numérique.</span><span class="sxs-lookup"><span data-stu-id="13d1f-116">*Precision*  must be a numeric expression.</span></span> <span data-ttu-id="13d1f-117">Lorsque la *précision* est un nombre positif, le *nombre* est arrondi au nombre de positions décimales spécifié par la longueur.</span><span class="sxs-lookup"><span data-stu-id="13d1f-117">When  *Precision*  is a positive number,  *Number*  is rounded to the number of decimal positions specified by length.</span></span> <span data-ttu-id="13d1f-118">Lorsque la *précision* est un nombre négatif, le *nombre* est arrondi à gauche du séparateur décimal, comme spécifié par longueur.</span><span class="sxs-lookup"><span data-stu-id="13d1f-118">When  *Precision*  is a negative number,  *Number*  is rounded on the left side of the decimal point, as specified by length.</span></span>  <br/> |
| <span data-ttu-id="13d1f-119">*TruncateInsteadOfRound*</span><span class="sxs-lookup"><span data-stu-id="13d1f-119">*TruncateInsteadOfRound*</span></span>  <br/> |<span data-ttu-id="13d1f-120">Type d'opération à effectuer.</span><span class="sxs-lookup"><span data-stu-id="13d1f-120">The type of operation to perform.</span></span> <span data-ttu-id="13d1f-121">Si cet argument est omis ou défini sur 0, le *nombre* est arrondi.</span><span class="sxs-lookup"><span data-stu-id="13d1f-121">When omitted or set to 0,  *Number*  is rounded.</span></span> <span data-ttu-id="13d1f-122">Lorsqu'une valeur autre que 0 est spécifiée, le *nombre* est tronqué.</span><span class="sxs-lookup"><span data-stu-id="13d1f-122">When a value other than 0 is specified,  *Number*  is truncated.</span></span> <span data-ttu-id="13d1f-123">La valeur par défaut est 0.</span><span class="sxs-lookup"><span data-stu-id="13d1f-123">The default value is 0.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13d1f-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="13d1f-124">Remarks</span></span>

 <span data-ttu-id="13d1f-125">**Round** renvoie toujours une valeur.</span><span class="sxs-lookup"><span data-stu-id="13d1f-125">**Round** always returns a value.</span></span> <span data-ttu-id="13d1f-126">Si le paramètre longueur est négatif et supérieur au nombre de chiffres avant le séparateur décimal, **Round** renvoie 0.</span><span class="sxs-lookup"><span data-stu-id="13d1f-126">If length is negative and larger than the number of digits before the decimal point, **Round** returns 0.</span></span> 
  

