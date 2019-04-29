---
title: Fonction Stuff (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4d8d6a34-f884-40a4-b330-5c104d16cf97
description: Insère une chaîne de texte dans une autre chaîne de texte. Il supprime une longueur spécifiée de caractères dans la première chaîne à la position de début, puis insère la deuxième chaîne dans la première chaîne à la position de début.
ms.openlocfilehash: 591823952faa0d593b6db1f5bfb00cc68a894a8d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427674"
---
# <a name="stuff-function-access-custom-web-app"></a><span data-ttu-id="ee6d6-104">Fonction Stuff (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="ee6d6-104">Stuff Function (Access custom web app)</span></span>

<span data-ttu-id="ee6d6-105">Insère une chaîne de texte dans une autre chaîne de texte.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-105">Inserts a text string into another text string.</span></span> <span data-ttu-id="ee6d6-106">Il supprime une longueur spécifiée de caractères dans la première chaîne à la position de début, puis insère la deuxième chaîne dans la première chaîne à la position de début.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-106">It deletes a specified length of characters in the first string at the start position and then inserts the second string into the first string at the start position.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ee6d6-p103">Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ee6d6-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ee6d6-109">Syntax</span></span>

 <span data-ttu-id="ee6d6-110">\*\*\*\* Éléments (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span><span class="sxs-lookup"><span data-stu-id="ee6d6-110">**Stuff** (*IntoTextExpression*, *Start*, *Length*, *ThisTextExpression*)</span></span> 
  
<span data-ttu-id="ee6d6-111">La fonction **Stuff** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-111">The **Stuff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ee6d6-112">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="ee6d6-112">**Argument name**</span></span>|<span data-ttu-id="ee6d6-113">**Description**</span><span class="sxs-lookup"><span data-stu-id="ee6d6-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ee6d6-114">*IntoTextExpression*</span><span class="sxs-lookup"><span data-stu-id="ee6d6-114">*IntoTextExpression*</span></span>  <br/> |<span data-ttu-id="ee6d6-115">Expression de texte qui spécifie le texte dans lequel le texte spécifié par l' *ThisTextExpression* sera inséré.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-115">A text expression that specifies the text into which the text specified by the  *ThisTextExpression*  will be inserted.</span></span>  <br/> |
| <span data-ttu-id="ee6d6-116">*Start*</span><span class="sxs-lookup"><span data-stu-id="ee6d6-116">*Start*</span></span>  <br/> |<span data-ttu-id="ee6d6-117">Valeur entière qui spécifie l'emplacement de début de la suppression et de l'insertion.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-117">An integer value that specifies the location to start deletion and insertion.</span></span> <span data-ttu-id="ee6d6-118">Si start ou length est négatif, une chaîne nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-118">If start or length is negative, a null string is returned.</span></span> <span data-ttu-id="ee6d6-119">Si Start est plus long que le premier *IntoTextExpression* , une chaîne nulle est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-119">If start is longer than the first  *IntoTextExpression*  , a null string is returned.</span></span>  <br/> |
| <span data-ttu-id="ee6d6-120">*Length*</span><span class="sxs-lookup"><span data-stu-id="ee6d6-120">*Length*</span></span>  <br/> |<span data-ttu-id="ee6d6-121">Entier qui spécifie le nombre de caractères à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-121">An integer that specifies the number of characters to delete.</span></span> <span data-ttu-id="ee6d6-122">Si length est plus long que le premier *IntoTextExpression* , la suppression se produit jusqu'au dernier caractère du dernier *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="ee6d6-122">If length is longer than the first  *IntoTextExpression*  , deletion occurs up to the last character in the last  *IntoTextExpression*  .</span></span>  <br/> |
| <span data-ttu-id="ee6d6-123">*ThisTextExpression*</span><span class="sxs-lookup"><span data-stu-id="ee6d6-123">*ThisTextExpression*</span></span>  <br/> |<span data-ttu-id="ee6d6-124">Un chapeau d'expression de texte spécifie le texte à insérer dans *IntoTextExpression* .</span><span class="sxs-lookup"><span data-stu-id="ee6d6-124">A text expression hat specifies the text to insert into  *IntoTextExpression*  .</span></span> <span data-ttu-id="ee6d6-125">Cette expression remplace les caractères de longueur de *IntoTextExpression* en commençant au *début* .</span><span class="sxs-lookup"><span data-stu-id="ee6d6-125">This expression will replace length characters of  *IntoTextExpression*  beginning at  *Start*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee6d6-126">Remarques</span><span class="sxs-lookup"><span data-stu-id="ee6d6-126">Remarks</span></span>

<span data-ttu-id="ee6d6-127">Si les arguments *Start* ou *Length* sont négatifs, ou si la position de départ est supérieure à la longueur de la première chaîne, une chaîne NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-127">If the  *Start*  or  *Length*  arguments are negative, or if the starting position is larger than length of the first string, a null string is returned.</span></span> <span data-ttu-id="ee6d6-128">Si la position de début est 0, une valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-128">If the start position is 0, a null value is returned.</span></span> <span data-ttu-id="ee6d6-129">Si la longueur à supprimer est supérieure à la première chaîne, elle est supprimée jusqu'au premier caractère de la première chaîne.</span><span class="sxs-lookup"><span data-stu-id="ee6d6-129">If the length to delete is longer than the first string, it is deleted to the first character in the first string.</span></span> 
  

