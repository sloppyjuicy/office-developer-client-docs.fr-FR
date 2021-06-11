---
title: Stuff Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insère une chaîne de texte dans une autre chaîne de texte. Elle supprime une longueur spécifiée de caractères dans la première chaîne à la position de début, puis insère la deuxième chaîne dans la première chaîne à la position de début.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427674"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="be929-104">Stuff Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="be929-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="be929-105">Insère une chaîne de texte dans une autre chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="be929-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="be929-106">Elle supprime une longueur spécifiée de caractères dans la première chaîne à la position de début, puis insère la deuxième chaîne dans la première chaîne à la position de début.</span><span class="sxs-lookup"><span data-stu-id="be929-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="be929-p103">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="be929-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="be929-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="be929-109">Syntax</span></span>

 <span data-ttu-id="be929-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="be929-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="be929-111">La **fonction Stuff** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="be929-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="be929-112">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="be929-112">**Argument name**</span></span>|<span data-ttu-id="be929-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="be929-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="be929-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="be929-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="be929-115">Expression de texte qui spécifie le texte dans lequel le texte spécifié par  *ThisTextExpression*  sera inséré.</span><span class="sxs-lookup"><span data-stu-id="be929-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="be929-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="be929-116">*Start*</span></span>  <br/> |<span data-ttu-id="be929-117">Valeur d’un nombre integer qui spécifie l’emplacement de démarrage de la suppression et de l’insertion.</span><span class="sxs-lookup"><span data-stu-id="be929-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="be929-118">Si le début ou la longueur est négatif, une chaîne null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="be929-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="be929-119">Si le début est plus long que le premier  *IntoTextExpression*  , une chaîne null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="be929-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="be929-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="be929-120">*Length*</span></span>  <br/> |<span data-ttu-id="be929-121">Nombre total qui spécifie le nombre de caractères à supprimer.</span><span class="sxs-lookup"><span data-stu-id="be929-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="be929-122">Si la longueur est plus longue que la première  *intoTextExpression*  , la suppression se produit jusqu’au dernier caractère du dernier  *IntoTextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="be929-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="be929-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="be929-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="be929-124">Un bonnet d’expression de texte spécifie le texte à insérer  *dans IntoTextExpression*  .</span><span class="sxs-lookup"><span data-stu-id="be929-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="be929-125">Cette expression remplace les caractères de longueur *de IntoTextExpression* à partir de *l’écran de démarrage.*</span><span class="sxs-lookup"><span data-stu-id="be929-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be929-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="be929-126">Remarks</span></span>

<span data-ttu-id="be929-127">Si  *les*  *arguments*  Début ou Longueur sont négatifs ou si la position de départ est supérieure à la longueur de la première chaîne, une chaîne null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="be929-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="be929-128">Si la position de début est 0, une valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="be929-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="be929-129">Si la longueur à supprimer est plus longue que la première chaîne, elle est supprimée au premier caractère de la première chaîne.</span><span class="sxs-lookup"><span data-stu-id="be929-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

