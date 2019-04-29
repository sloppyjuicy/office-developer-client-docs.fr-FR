---
title: Fonction log (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a897e812-08dc-49c9-954b-e8908a0daab3
description: Renvoie le logarithme népérien ou le logarithme de la base donnée, de l'expression spécifiée.
ms.openlocfilehash: e2cfd1cf4ad3c1bf44778737faa0f697333f5234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419295"
---
# <a name="log-function-access-custom-web-app"></a><span data-ttu-id="ffd1e-103">Fonction log (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="ffd1e-103">Log Function (Access custom web app)</span></span>

<span data-ttu-id="ffd1e-104">Renvoie le logarithme népérien ou le logarithme de la base donnée, de l'expression spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-104">Returns the natural logarithm, or the logarithm of the given base, of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ffd1e-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ffd1e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ffd1e-107">Syntax</span></span>

 <span data-ttu-id="ffd1e-108">**Journalisation** (*NumericExpression* , [ *base* ])</span><span class="sxs-lookup"><span data-stu-id="ffd1e-108">**Log** (*NumericExpression*  , [  *Base*  ])</span></span> 
  
<span data-ttu-id="ffd1e-109">La fonction **log** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-109">The **Log** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ffd1e-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="ffd1e-110">**Argument name**</span></span>|<span data-ttu-id="ffd1e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ffd1e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ffd1e-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="ffd1e-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="ffd1e-113">Nombre positif pour lequel vous souhaitez obtenir le logarithme.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-113">The positive number for which you want the logarithm.</span></span>  <br/> |
| <span data-ttu-id="ffd1e-114">*Base*</span><span class="sxs-lookup"><span data-stu-id="ffd1e-114">*Base*</span></span>  <br/> |<span data-ttu-id="ffd1e-115">Base du logarithme.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-115">The base of the logarithm.</span></span> <span data-ttu-id="ffd1e-116">Si cet argument est omis, la fonction **log** renvoie le logarithme népérien.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-116">If omitted, the **Log** function returns the natural logarithm.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffd1e-117">Remarques</span><span class="sxs-lookup"><span data-stu-id="ffd1e-117">Remarks</span></span>

<span data-ttu-id="ffd1e-118">La fonction **log10** est similaire, mais renvoie toujours le logarithme courant, c'est-à-dire le logarithme de la base 10.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-118">The function **Log10** is similar, but always returns the common logarithm, meaning the logarithm for the base 10.</span></span> 
  
<span data-ttu-id="ffd1e-119">Le logarithme népérien est le logarithme de la base e, où e est une constante Irrational égale approximativement à 2,718281828.</span><span class="sxs-lookup"><span data-stu-id="ffd1e-119">The natural logarithm is the logarithm to the base e, where e is an irrational constant approximately equal to 2.718281828.</span></span>
  

