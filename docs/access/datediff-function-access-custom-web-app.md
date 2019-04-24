---
title: Fonction DateDiff (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites de la partie de date spécifiée, franchie entre la date de début et la date de fin spécifiées.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280722"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="82874-103">Fonction DateDiff (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="82874-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="82874-104">Renvoie le nombre de limites de la partie de date spécifiée, franchie entre la date de début et la date de fin spécifiées.</span><span class="sxs-lookup"><span data-stu-id="82874-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="82874-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="82874-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="82874-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="82874-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="82874-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="82874-107">Syntax</span></span>

<span data-ttu-id="82874-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="82874-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="82874-109">La fonction **DateDiff** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="82874-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="82874-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="82874-110">**Argument name**</span></span>|<span data-ttu-id="82874-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="82874-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="82874-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="82874-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="82874-113">Est la partie de *StartDate* et *EndDate* qui spécifie le type de la limite franchie.</span><span class="sxs-lookup"><span data-stu-id="82874-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="82874-114">RePortez-vous à la section Remarques pour obtenir la liste des paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="82874-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="82874-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="82874-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="82874-116">Expression qui peut être résolue en une valeur de date/heure.</span><span class="sxs-lookup"><span data-stu-id="82874-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="82874-117">Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82874-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="82874-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="82874-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="82874-119">Expression qui peut être résolue en une valeur de date/heure.</span><span class="sxs-lookup"><span data-stu-id="82874-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="82874-120">Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="82874-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="82874-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="82874-121">Remarks</span></span>

<span data-ttu-id="82874-122">Le tableau suivant répertorie tous les arguments *DatePart* valides.</span><span class="sxs-lookup"><span data-stu-id="82874-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="82874-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="82874-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="82874-124">**year**</span><span class="sxs-lookup"><span data-stu-id="82874-124">**year**</span></span> <br/> |
|<span data-ttu-id="82874-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="82874-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="82874-126">**month**</span><span class="sxs-lookup"><span data-stu-id="82874-126">**month**</span></span> <br/> |
|<span data-ttu-id="82874-127">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="82874-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="82874-128">**day**</span><span class="sxs-lookup"><span data-stu-id="82874-128">**day**</span></span> <br/> |
|<span data-ttu-id="82874-129">**mensuel**</span><span class="sxs-lookup"><span data-stu-id="82874-129">**week**</span></span> <br/> |
|<span data-ttu-id="82874-130">**h/24**</span><span class="sxs-lookup"><span data-stu-id="82874-130">**hour**</span></span> <br/> |
|<span data-ttu-id="82874-131">**précédente**</span><span class="sxs-lookup"><span data-stu-id="82874-131">**minute**</span></span> <br/> |
|<span data-ttu-id="82874-132">**seconde**</span><span class="sxs-lookup"><span data-stu-id="82874-132">**second**</span></span> <br/> |
|<span data-ttu-id="82874-133">**exprimée**</span><span class="sxs-lookup"><span data-stu-id="82874-133">**millisecond**</span></span> <br/> |
   

