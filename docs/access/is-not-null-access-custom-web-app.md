---
title: IS [NOT] NULL (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Détermine si une expression spécifiée est NULL.
localization_priority: Priority
ms.openlocfilehash: fe6a0fe4f182a1385304b783e7cfaaf515f732d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311136"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="881bf-103">IS [NOT] NULL (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="881bf-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="881bf-104">Détermine si une expression spécifiée est NULL.</span><span class="sxs-lookup"><span data-stu-id="881bf-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="881bf-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="881bf-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="881bf-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="881bf-107">Syntax</span></span>

 <span data-ttu-id="881bf-108">*expression* **IS** [  *NOT*  ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="881bf-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="881bf-109">Le prédicat **IS [NOT] NULL** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="881bf-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="881bf-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="881bf-110">*expression*</span></span>  <br/> |<span data-ttu-id="881bf-111">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="881bf-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="881bf-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="881bf-112">*NOT*</span></span>  <br/> |<span data-ttu-id="881bf-113">Spécifie que le résultat booléen doit être réfuté.</span><span class="sxs-lookup"><span data-stu-id="881bf-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="881bf-114">Le prédicat inverse ses valeurs renvoyées, renvoyant TRUE si la valeur n’est pas NULL et FALSE si la valeur est NULL.</span><span class="sxs-lookup"><span data-stu-id="881bf-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="881bf-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="881bf-115">Remarks</span></span>

<span data-ttu-id="881bf-116">Si la valeur de l’*expression* est NULL, IS NULL renvoie TRUE ; dans le cas contraire, elle renvoie FALSE.</span><span class="sxs-lookup"><span data-stu-id="881bf-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="881bf-117">Si la valeur de l’expression est NULL, IS NOT NULL renvoie FALSE ; dans le cas contraire, elle renvoie TRUE.</span><span class="sxs-lookup"><span data-stu-id="881bf-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

