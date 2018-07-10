---
title: Fonction sous-chaîne (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Renvoie une partie d’une expression de texte.
ms.openlocfilehash: 49d9afefe4b25d91738e518e0ddb2b902067c038
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781998"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="87e11-103">Fonction sous-chaîne (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="87e11-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="87e11-104">Renvoie une partie d’une expression de texte.</span><span class="sxs-lookup"><span data-stu-id="87e11-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="87e11-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="87e11-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/fr-fr/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="87e11-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="87e11-107">Syntax</span></span>

 <span data-ttu-id="87e11-108">**Sous-chaîne** (*TextExpression*, *début*, *longueur*)</span><span class="sxs-lookup"><span data-stu-id="87e11-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="87e11-109">La fonction de **sous-chaîne** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="87e11-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="87e11-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="87e11-110">**Argument name**</span></span>|<span data-ttu-id="87e11-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="87e11-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="87e11-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="87e11-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="87e11-113">Une expression de texte.</span><span class="sxs-lookup"><span data-stu-id="87e11-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="87e11-114">*Début*</span><span class="sxs-lookup"><span data-stu-id="87e11-114">*Start*</span></span>  <br/> |<span data-ttu-id="87e11-115">Entier qui spécifie où commencer les caractères renvoyées.</span><span class="sxs-lookup"><span data-stu-id="87e11-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="87e11-116">Si start est inférieur à 1, l’expression renvoyée commence au premier caractère spécifié dans une expression.</span><span class="sxs-lookup"><span data-stu-id="87e11-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="87e11-117">Dans ce cas, le nombre de caractères qui sont renvoyés est la plus grande valeur soit la somme de début + longueur-1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="87e11-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="87e11-118">Si start est supérieur au nombre de caractères dans l’expression de valeur, une expression de longueur nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="87e11-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="87e11-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="87e11-119">*Length*</span></span>  <br/> |<span data-ttu-id="87e11-120">Une expression d’entier positif qui spécifie le nombre de caractères de l’expression à retourner.</span><span class="sxs-lookup"><span data-stu-id="87e11-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="87e11-121">Si length est négatif, une erreur est générée et l’instruction est terminée.</span><span class="sxs-lookup"><span data-stu-id="87e11-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="87e11-122">Si la somme des start et length est supérieure au nombre de caractères dans une expression, la valeur entière expression en commençant à démarrer est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="87e11-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

