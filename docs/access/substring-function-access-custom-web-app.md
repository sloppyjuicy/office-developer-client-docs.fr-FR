---
title: Fonction SUBSTRING (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae99a0fa-76c4-4c07-9ae9-a7abce23394f
description: Renvoie une partie d'une expression de texte.
ms.openlocfilehash: af93620905af366f41bcc50ab6102114acd3db9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433471"
---
# <a name="substring-function-access-custom-web-app"></a><span data-ttu-id="063aa-103">Fonction SUBSTRING (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="063aa-103">SubString Function (Access custom web app)</span></span>

<span data-ttu-id="063aa-104">Renvoie une partie d'une expression de texte.</span><span class="sxs-lookup"><span data-stu-id="063aa-104">Returns part of a text expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="063aa-p101">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="063aa-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="063aa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="063aa-107">Syntax</span></span>

 <span data-ttu-id="063aa-108">**Sous-chaîne** (*TextExpression*, *Start*, *Length*)</span><span class="sxs-lookup"><span data-stu-id="063aa-108">**SubString** (*TextExpression*, *Start*, *Length*)</span></span> 
  
<span data-ttu-id="063aa-109">La \*\*\*\* fonction SUBSTRING contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="063aa-109">The **SubString** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="063aa-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="063aa-110">**Argument name**</span></span>|<span data-ttu-id="063aa-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="063aa-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="063aa-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="063aa-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="063aa-113">Expression de texte.</span><span class="sxs-lookup"><span data-stu-id="063aa-113">A text expression.</span></span>  <br/> |
| <span data-ttu-id="063aa-114">*Start*</span><span class="sxs-lookup"><span data-stu-id="063aa-114">*Start*</span></span>  <br/> |<span data-ttu-id="063aa-115">Expression de type Integer qui spécifie l'emplacement des caractères renvoyés.</span><span class="sxs-lookup"><span data-stu-id="063aa-115">An integer expression that specifies where the returned characters start.</span></span> <span data-ttu-id="063aa-116">Si Start est inférieur à 1, l'expression renvoyée commence au premier caractère spécifié dans Expression.</span><span class="sxs-lookup"><span data-stu-id="063aa-116">If start is less than 1, the returned expression will begin at the first character that is specified in expression.</span></span> <span data-ttu-id="063aa-117">Dans ce cas, le nombre de caractères renvoyés est la valeur la plus élevée de la somme de start + length-1 ou 0.</span><span class="sxs-lookup"><span data-stu-id="063aa-117">In this case, the number of characters that are returned is the largest value of either the sum of start + length- 1 or 0.</span></span> <span data-ttu-id="063aa-118">Si Start est plus grand que le nombre de caractères dans l'expression de valeur, une expression de longueur nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="063aa-118">If start is greater than the number of characters in the value expression, a zero-length expression is returned.</span></span>  <br/> |
| <span data-ttu-id="063aa-119">*Length*</span><span class="sxs-lookup"><span data-stu-id="063aa-119">*Length*</span></span>  <br/> |<span data-ttu-id="063aa-120">Expression de type entier positif spécifiant le nombre de caractères de l'expression à renvoyer.</span><span class="sxs-lookup"><span data-stu-id="063aa-120">A positive integer expression that specifies how many characters of the expression will be returned.</span></span> <span data-ttu-id="063aa-121">Si length est négatif, une erreur est générée et l'instruction est arrêtée.</span><span class="sxs-lookup"><span data-stu-id="063aa-121">If length is negative, an error is generated and the statement is terminated.</span></span> <span data-ttu-id="063aa-122">Si la somme de début et de longueur est supérieure au nombre de caractères dans expression, l'expression de valeur entière commençant au début est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="063aa-122">If the sum of start and length is greater than the number of characters in expression, the whole value expression beginning at start is returned.</span></span>  <br/> |
   

