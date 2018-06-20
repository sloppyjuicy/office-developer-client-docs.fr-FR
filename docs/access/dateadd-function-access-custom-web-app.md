---
title: Fonction DateAdd (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Renvoie une date spécifiée avec l’intervalle de numéros spécifié (entier positif ou négatif) est ajouté à une partie de la date spécifiée de la date.
ms.openlocfilehash: a2baa58a2ccab7d030750d03d4fddb84e8eb8ff7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781840"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="075e1-103">Fonction DateAdd (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="075e1-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="075e1-104">Renvoie une date spécifiée avec l’intervalle de numéros spécifié (entier positif ou négatif) est ajouté à une partie de la date spécifiée de la date.</span><span class="sxs-lookup"><span data-stu-id="075e1-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="075e1-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="075e1-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="075e1-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="075e1-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="075e1-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="075e1-107">Syntax</span></span>

<span data-ttu-id="075e1-108">**DateAdd** (*DatePart*, *nombre*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="075e1-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="075e1-109">La fonction **DateAdd** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="075e1-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="075e1-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="075e1-110">**Argument name**</span></span>|<span data-ttu-id="075e1-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="075e1-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="075e1-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="075e1-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="075e1-113">La partie de la *Date* à laquelle un nombre entier est ajouté.</span><span class="sxs-lookup"><span data-stu-id="075e1-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="075e1-114">Reportez-vous à la section Remarques pour la liste des paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="075e1-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="075e1-115">*Number*</span><span class="sxs-lookup"><span data-stu-id="075e1-115">*Number*</span></span>  <br/> |<span data-ttu-id="075e1-116">Est une expression qui peut être résolue vers un entier qui est ajouté à une *partie* de *Date* .</span><span class="sxs-lookup"><span data-stu-id="075e1-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="075e1-117">Si vous spécifiez une valeur avec une fraction décimale, la fraction est tronquée.</span><span class="sxs-lookup"><span data-stu-id="075e1-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="075e1-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="075e1-118">*Date*</span></span>  <br/> |<span data-ttu-id="075e1-119">Une expression qui peut être résolue sur une valeur de Date/heure.</span><span class="sxs-lookup"><span data-stu-id="075e1-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="075e1-120">La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.</span><span class="sxs-lookup"><span data-stu-id="075e1-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="075e1-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="075e1-121">Remarks</span></span>

<span data-ttu-id="075e1-122">Le tableau suivant répertorie tous les arguments *DatePart* valides.</span><span class="sxs-lookup"><span data-stu-id="075e1-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="075e1-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="075e1-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="075e1-124">**year**</span><span class="sxs-lookup"><span data-stu-id="075e1-124">**year**</span></span> <br/> |
|<span data-ttu-id="075e1-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="075e1-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="075e1-126">**Mois**</span><span class="sxs-lookup"><span data-stu-id="075e1-126">**month**</span></span> <br/> |
|<span data-ttu-id="075e1-127">**DAYOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="075e1-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="075e1-128">**day**</span><span class="sxs-lookup"><span data-stu-id="075e1-128">**day**</span></span> <br/> |
|<span data-ttu-id="075e1-129">**semaine**</span><span class="sxs-lookup"><span data-stu-id="075e1-129">**week**</span></span> <br/> |
|<span data-ttu-id="075e1-130">**heure**</span><span class="sxs-lookup"><span data-stu-id="075e1-130">**hour**</span></span> <br/> |
|<span data-ttu-id="075e1-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="075e1-131">**minute**</span></span> <br/> |
|<span data-ttu-id="075e1-132">**seconde**</span><span class="sxs-lookup"><span data-stu-id="075e1-132">**second**</span></span> <br/> |
|<span data-ttu-id="075e1-133">**milliseconde**</span><span class="sxs-lookup"><span data-stu-id="075e1-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="075e1-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="075e1-134">Example</span></span>

<span data-ttu-id="075e1-135">L’expression suivante calcule le dernier jour du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="075e1-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="075e1-136">L’expression suivante calcule le dernier jour du mois précédent.</span><span class="sxs-lookup"><span data-stu-id="075e1-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


