---
title: Fonction de sélections (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insère une chaîne de texte dans une autre chaîne de texte. Elle supprime une longueur de caractères dans la première chaîne à la position de début spécifiée et insère ensuite la deuxième chaîne dans la première chaîne de la position de début.
ms.openlocfilehash: 5540bb5936803370835a0c3d80b420edc13d0de6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781986"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="c63e0-104">Fonction de sélections (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="c63e0-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="c63e0-105">Insère une chaîne de texte dans une autre chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="c63e0-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="c63e0-106">Elle supprime une longueur de caractères dans la première chaîne à la position de début spécifiée et insère ensuite la deuxième chaîne dans la première chaîne de la position de début.</span><span class="sxs-lookup"><span data-stu-id="c63e0-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="c63e0-p103">[!IMPORTANTE] Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="c63e0-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c63e0-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c63e0-109">Syntax</span></span>

 <span data-ttu-id="c63e0-110">**Sélections** (*IntoTextExpression*, *début*, *longueur*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="c63e0-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="c63e0-111">La fonction de **document** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="c63e0-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="c63e0-112">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="c63e0-112">**Argument name**</span></span>|<span data-ttu-id="c63e0-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="c63e0-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c63e0-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="c63e0-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="c63e0-115">Une expression de texte qui spécifie le texte dans lequel le texte spécifié par le *ThisTextExpression* sera inséré.</span><span class="sxs-lookup"><span data-stu-id="c63e0-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="c63e0-116">*Début*</span><span class="sxs-lookup"><span data-stu-id="c63e0-116">*Start*</span></span>  <br/> |<span data-ttu-id="c63e0-117">Entier qui spécifie l’emplacement pour démarrer l’insertion et suppression.</span><span class="sxs-lookup"><span data-stu-id="c63e0-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="c63e0-118">Si start ou length est négatif, une chaîne nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c63e0-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="c63e0-119">Si start est plus long que premier *IntoTextExpression* , une chaîne nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c63e0-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="c63e0-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="c63e0-120">*Length*</span></span>  <br/> |<span data-ttu-id="c63e0-121">Entier qui spécifie le nombre de caractères à supprimer.</span><span class="sxs-lookup"><span data-stu-id="c63e0-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="c63e0-122">Si length est plus longue que première *IntoTextExpression* , suppression s’effectue jusqu’au dernier caractère de dernière *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="c63e0-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="c63e0-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="c63e0-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="c63e0-124">Chapeau expression texte spécifie le texte à insérer dans *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="c63e0-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="c63e0-125">Cette expression remplacera les caractères de longueur de *IntoTextExpression* en commençant à *Démarrer* .</span><span class="sxs-lookup"><span data-stu-id="c63e0-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c63e0-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="c63e0-126">Remarks</span></span>

<span data-ttu-id="c63e0-127">Si les arguments *Start* ou *Length* sont négatifs, ou si la position de début est supérieure à la longueur de la première chaîne, une chaîne nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c63e0-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="c63e0-128">Si la position de début est 0, une valeur nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="c63e0-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="c63e0-129">Si la longueur à effacer est supérieure à la première chaîne, il est supprimé au premier caractère dans la première chaîne.</span><span class="sxs-lookup"><span data-stu-id="c63e0-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

