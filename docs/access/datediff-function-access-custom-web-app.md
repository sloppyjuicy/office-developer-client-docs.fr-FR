---
title: Fonction DateDiff (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.
ms.openlocfilehash: 1cce8a501c5a57384372e681f903baa4f4c20bef
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415613"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="8317e-103">Fonction DateDiff (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="8317e-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="8317e-104">Renvoie le nombre de limites de partie de date spécifiées entre la date de début spécifiée et la date de fin.</span><span class="sxs-lookup"><span data-stu-id="8317e-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8317e-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="8317e-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="8317e-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8317e-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8317e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8317e-107">Syntax</span></span>

<span data-ttu-id="8317e-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="8317e-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="8317e-109">La **fonction DateDiff** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="8317e-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8317e-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="8317e-110">**Argument name**</span></span>|<span data-ttu-id="8317e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8317e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8317e-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="8317e-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="8317e-113">Est la partie de  *StartDate*  et  *EndDate*  qui spécifie le type de limite croisée.</span><span class="sxs-lookup"><span data-stu-id="8317e-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="8317e-114">Reportez-vous à la section Remarques pour obtenir la liste des paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="8317e-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="8317e-115">*StartDate*</span><span class="sxs-lookup"><span data-stu-id="8317e-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="8317e-116">Expression qui peut être résolue en valeur Date/Heure.</span><span class="sxs-lookup"><span data-stu-id="8317e-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="8317e-117">Expression  *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8317e-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="8317e-118">*EndDate*</span><span class="sxs-lookup"><span data-stu-id="8317e-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="8317e-119">Expression qui peut être résolue en valeur Date/Heure.</span><span class="sxs-lookup"><span data-stu-id="8317e-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="8317e-120">Expression  *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.</span><span class="sxs-lookup"><span data-stu-id="8317e-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8317e-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8317e-121">Remarks</span></span>

<span data-ttu-id="8317e-122">Le tableau suivant répertorie tous les arguments  *DatePart*  valides.</span><span class="sxs-lookup"><span data-stu-id="8317e-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="8317e-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="8317e-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="8317e-124">**year**</span><span class="sxs-lookup"><span data-stu-id="8317e-124">**year**</span></span> <br/> |
|<span data-ttu-id="8317e-125">**quarter**</span><span class="sxs-lookup"><span data-stu-id="8317e-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="8317e-126">**Mois**</span><span class="sxs-lookup"><span data-stu-id="8317e-126">**month**</span></span> <br/> |
|<span data-ttu-id="8317e-127">**dayofyear**</span><span class="sxs-lookup"><span data-stu-id="8317e-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="8317e-128">**day**</span><span class="sxs-lookup"><span data-stu-id="8317e-128">**day**</span></span> <br/> |
|<span data-ttu-id="8317e-129">**semaine**</span><span class="sxs-lookup"><span data-stu-id="8317e-129">**week**</span></span> <br/> |
|<span data-ttu-id="8317e-130">**hour**</span><span class="sxs-lookup"><span data-stu-id="8317e-130">**hour**</span></span> <br/> |
|<span data-ttu-id="8317e-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="8317e-131">**minute**</span></span> <br/> |
|<span data-ttu-id="8317e-132">**second**</span><span class="sxs-lookup"><span data-stu-id="8317e-132">**second**</span></span> <br/> |
|<span data-ttu-id="8317e-133">**milliseconde**</span><span class="sxs-lookup"><span data-stu-id="8317e-133">**millisecond**</span></span> <br/> |
   

