---
title: Fonction DateAdd (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7174c585-86e1-42a3-bb7f-d6641001b0f2
description: Renvoie une date spécifiée avec l'intervalle de numéros spécifié (entier positif ou négatif) ajouté à une partie de date spécifiée de cette date.
ms.openlocfilehash: 7cfd68c4983eee22a5e542facd72ea083deb3184
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423201"
---
# <a name="dateadd-function-access-custom-web-app"></a><span data-ttu-id="62666-103">Fonction DateAdd (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="62666-103">DateAdd function (Access custom web app)</span></span>

<span data-ttu-id="62666-104">Renvoie une date spécifiée avec l'intervalle de numéros spécifié (entier positif ou négatif) ajouté à une partie de date spécifiée de cette date.</span><span class="sxs-lookup"><span data-stu-id="62666-104">Returns a specified date with the specified number interval (positive or negative integer) added to a specified date part of that date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="62666-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="62666-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="62666-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="62666-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="62666-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="62666-107">Syntax</span></span>

<span data-ttu-id="62666-108">**DATEADD** (*DatePart*, *Number*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="62666-108">**DateAdd** (*DatePart*, *Number*, *Date*)</span></span> 
  
<span data-ttu-id="62666-109">La fonction **DATEADD** contient les arguments suivants:</span><span class="sxs-lookup"><span data-stu-id="62666-109">The **DateAdd** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="62666-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="62666-110">**Argument name**</span></span>|<span data-ttu-id="62666-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="62666-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="62666-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="62666-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="62666-113">Partie de la *Date* à laquelle un nombre entier est ajouté.</span><span class="sxs-lookup"><span data-stu-id="62666-113">The part of  *Date*  to which an integer number is added.</span></span> <span data-ttu-id="62666-114">RePortez-vous à la section Remarques pour obtenir la liste des paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="62666-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="62666-115">*Number*</span><span class="sxs-lookup"><span data-stu-id="62666-115">*Number*</span></span>  <br/> |<span data-ttu-id="62666-116">Est une expression qui peut être résolue en un entier qui est ajouté à \*\* une partie de la *Date* .</span><span class="sxs-lookup"><span data-stu-id="62666-116">Is an expression that can be resolved to an integer that is added to a  *DatePart*  of  *Date*  .</span></span> <span data-ttu-id="62666-117">Si vous spécifiez une valeur avec une fraction décimale, la fraction est tronquée.</span><span class="sxs-lookup"><span data-stu-id="62666-117">If you specify a value with a decimal fraction, the fraction is truncated.</span></span>  <br/> |
| <span data-ttu-id="62666-118">*Date*</span><span class="sxs-lookup"><span data-stu-id="62666-118">*Date*</span></span>  <br/> |<span data-ttu-id="62666-119">Expression qui peut être résolue en une valeur de date/heure.</span><span class="sxs-lookup"><span data-stu-id="62666-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="62666-120">Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="62666-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="62666-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="62666-121">Remarks</span></span>

<span data-ttu-id="62666-122">Le tableau suivant répertorie tous les arguments *DatePart* valides.</span><span class="sxs-lookup"><span data-stu-id="62666-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="62666-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="62666-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="62666-124">**year**</span><span class="sxs-lookup"><span data-stu-id="62666-124">**year**</span></span> <br/> |
|<span data-ttu-id="62666-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="62666-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="62666-126">**Mois**</span><span class="sxs-lookup"><span data-stu-id="62666-126">**month**</span></span> <br/> |
|<span data-ttu-id="62666-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="62666-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="62666-128">**day**</span><span class="sxs-lookup"><span data-stu-id="62666-128">**day**</span></span> <br/> |
|<span data-ttu-id="62666-129">**mensuel**</span><span class="sxs-lookup"><span data-stu-id="62666-129">**week**</span></span> <br/> |
|<span data-ttu-id="62666-130">**h/24**</span><span class="sxs-lookup"><span data-stu-id="62666-130">**hour**</span></span> <br/> |
|<span data-ttu-id="62666-131">**précédente**</span><span class="sxs-lookup"><span data-stu-id="62666-131">**minute**</span></span> <br/> |
|<span data-ttu-id="62666-132">**seconde**</span><span class="sxs-lookup"><span data-stu-id="62666-132">**second**</span></span> <br/> |
|<span data-ttu-id="62666-133">**exprimée**</span><span class="sxs-lookup"><span data-stu-id="62666-133">**millisecond**</span></span> <br/> |
   
## <a name="example"></a><span data-ttu-id="62666-134">Exemple</span><span class="sxs-lookup"><span data-stu-id="62666-134">Example</span></span>

<span data-ttu-id="62666-135">L'expression suivante calcule le dernier jour du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="62666-135">The following expression calculates the last day of the current month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today())+1,0))`

<span data-ttu-id="62666-136">L'expression suivante calcule le dernier jour du mois précédent.</span><span class="sxs-lookup"><span data-stu-id="62666-136">The following expression calculates the last day of the previous month.</span></span>
  
`DateAdd(Day,-1,DateAdd(Month,DateDiff(Month,0,Today()),0))`


