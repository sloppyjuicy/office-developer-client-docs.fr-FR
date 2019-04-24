---
title: Fonction DatePart (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Renvoie une valeur numérique qui représente la partie de la date spécifiée de la date spécifiée.
ms.openlocfilehash: 31ac6423614afd61ed943bb7ba375f14696df1ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280767"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="50ce5-103">Fonction DatePart (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="50ce5-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="50ce5-104">Renvoie une valeur numérique qui représente la partie de la date spécifiée de la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="50ce5-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="50ce5-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="50ce5-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="50ce5-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="50ce5-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="50ce5-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="50ce5-107">Syntax</span></span>

<span data-ttu-id="50ce5-108">**DatePart** (*DatePart*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="50ce5-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="50ce5-109">La fonction **DatePart** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="50ce5-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="50ce5-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="50ce5-110">**Argument name**</span></span>|<span data-ttu-id="50ce5-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="50ce5-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="50ce5-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="50ce5-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="50ce5-113">Partie de la *Date* (valeur de date ou d'heure) pour laquelle un entier est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="50ce5-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="50ce5-114">RePortez-vous à la section Remarques pour obtenir la liste des abréviations valides.</span><span class="sxs-lookup"><span data-stu-id="50ce5-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="50ce5-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="50ce5-115">*Date*</span></span>  <br/> |<span data-ttu-id="50ce5-116">Expression qui peut être résolue en une valeur de date/heure.</span><span class="sxs-lookup"><span data-stu-id="50ce5-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="50ce5-117">Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="50ce5-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50ce5-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="50ce5-118">Remarks</span></span>

<span data-ttu-id="50ce5-119">Le tableau suivant répertorie tous les arguments *DatePart* valides.</span><span class="sxs-lookup"><span data-stu-id="50ce5-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="50ce5-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="50ce5-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="50ce5-121">**year**</span><span class="sxs-lookup"><span data-stu-id="50ce5-121">**year**</span></span> <br/> |
|<span data-ttu-id="50ce5-122">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="50ce5-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="50ce5-123">**month**</span><span class="sxs-lookup"><span data-stu-id="50ce5-123">**month**</span></span> <br/> |
|<span data-ttu-id="50ce5-124">**DayOfYear**</span><span class="sxs-lookup"><span data-stu-id="50ce5-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="50ce5-125">**day**</span><span class="sxs-lookup"><span data-stu-id="50ce5-125">**day**</span></span> <br/> |
|<span data-ttu-id="50ce5-126">**mensuel**</span><span class="sxs-lookup"><span data-stu-id="50ce5-126">**week**</span></span> <br/> |
|<span data-ttu-id="50ce5-127">**joursemaine**</span><span class="sxs-lookup"><span data-stu-id="50ce5-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="50ce5-128">**h/24**</span><span class="sxs-lookup"><span data-stu-id="50ce5-128">**hour**</span></span> <br/> |
|<span data-ttu-id="50ce5-129">**précédente**</span><span class="sxs-lookup"><span data-stu-id="50ce5-129">**minute**</span></span> <br/> |
|<span data-ttu-id="50ce5-130">**seconde**</span><span class="sxs-lookup"><span data-stu-id="50ce5-130">**second**</span></span> <br/> |
|<span data-ttu-id="50ce5-131">**exprimée**</span><span class="sxs-lookup"><span data-stu-id="50ce5-131">**millisecond**</span></span> <br/> |
   

