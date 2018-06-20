---
title: EST [NOT] NULL (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b941a0c7-9753-4920-bb6d-cbba94ba9422
description: Détermine si une expression est NULL.
ms.openlocfilehash: fcbceb1e8edac65fe232ba9c2b12195b99db9545
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781829"
---
# <a name="is-not-null-access-custom-web-app"></a><span data-ttu-id="1d384-103">EST [NOT] NULL (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="1d384-103">IS [NOT] NULL (Access custom web app)</span></span>

<span data-ttu-id="1d384-104">Détermine si une expression est NULL.</span><span class="sxs-lookup"><span data-stu-id="1d384-104">Determines whether a specified expression is NULL.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1d384-p101">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="1d384-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1d384-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d384-107">Syntax</span></span>

 <span data-ttu-id="1d384-108">*expression* **Est** [ *Pas* ] **NULL**</span><span class="sxs-lookup"><span data-stu-id="1d384-108">*expression* **IS** [  *NOT*  ] **NULL**</span></span>
  
<span data-ttu-id="1d384-109">Le **IS [NOT] NULL** prédicat contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="1d384-109">The **IS [NOT] NULL** predicate contains the following arguments.</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1d384-110">*expression*</span><span class="sxs-lookup"><span data-stu-id="1d384-110">*expression*</span></span>  <br/> |<span data-ttu-id="1d384-111">Toute expression valide.</span><span class="sxs-lookup"><span data-stu-id="1d384-111">Any valid expression.</span></span>  <br/> |
| <span data-ttu-id="1d384-112">*NOT*</span><span class="sxs-lookup"><span data-stu-id="1d384-112">*NOT*</span></span>  <br/> |<span data-ttu-id="1d384-113">Spécifie que le résultat Boolean être inversée.</span><span class="sxs-lookup"><span data-stu-id="1d384-113">Specifies that the Boolean result be negated.</span></span> <span data-ttu-id="1d384-114">Le prédicat inverse ses valeurs de retour, retourner la valeur TRUE si la valeur n’est pas NULL et FALSE si la valeur est NULL.</span><span class="sxs-lookup"><span data-stu-id="1d384-114">The predicate reverses its return values, returning TRUE if the value is not NULL, and FALSE if the value is NULL.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d384-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="1d384-115">Remarks</span></span>

<span data-ttu-id="1d384-116">Si la valeur de *l’expression* est NULL, est NULL renvoie TRUE ; dans le cas contraire, elle renvoie la valeur FALSE.</span><span class="sxs-lookup"><span data-stu-id="1d384-116">If the value of  *expression*  is NULL, IS NULL returns TRUE; otherwise, it returns FALSE.</span></span> 
  
<span data-ttu-id="1d384-117">Si la valeur de l’expression est NULL, n’est pas NULL renvoie la valeur FALSE ; dans le cas contraire, elle renvoie la valeur TRUE.</span><span class="sxs-lookup"><span data-stu-id="1d384-117">If the value of expression is NULL, IS NOT NULL returns FALSE; otherwise, it returns TRUE.</span></span>
  

