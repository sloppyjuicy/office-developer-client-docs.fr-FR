---
title: Fonction DateDiff (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 1c58ee87-0f57-4643-be4d-62da815df705
description: Renvoie le nombre de limites composant date spécifiée comprises entre la date de début et date de fin.
ms.openlocfilehash: fe898ec5eb59cb341250cb0c0e2e35bc55d37eb3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781838"
---
# <a name="datediff-function-access-custom-web-app"></a><span data-ttu-id="8d0be-103">Fonction DateDiff (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="8d0be-103">DateDiff function (Access custom web app)</span></span>

<span data-ttu-id="8d0be-104">Renvoie le nombre de limites composant date spécifiée comprises entre la date de début et date de fin.</span><span class="sxs-lookup"><span data-stu-id="8d0be-104">Returns the count of the specified date part boundaries crossed between the specified start date and end date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="8d0be-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="8d0be-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="8d0be-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="8d0be-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="8d0be-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d0be-107">Syntax</span></span>

<span data-ttu-id="8d0be-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span><span class="sxs-lookup"><span data-stu-id="8d0be-108">**DateDiff** (*DatePart*, *StartDate*, *EndDate*)</span></span> 
  
<span data-ttu-id="8d0be-109">La fonction **DateDiff** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="8d0be-109">The **DateDiff** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="8d0be-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="8d0be-110">**Argument name**</span></span>|<span data-ttu-id="8d0be-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="8d0be-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="8d0be-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="8d0be-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="8d0be-113">Est la partie de *StartDate* et *EndDate* qui spécifie le type de limite franchi.</span><span class="sxs-lookup"><span data-stu-id="8d0be-113">Is the part of  *StartDate*  and  *EndDate*  that specifies the type of boundary crossed.</span></span> <span data-ttu-id="8d0be-114">Reportez-vous à la section Remarques pour la liste des paramètres valides.</span><span class="sxs-lookup"><span data-stu-id="8d0be-114">Refer to the Remarks section for the list of valid settings.</span></span>  <br/> |
| <span data-ttu-id="8d0be-115">*Date de début*</span><span class="sxs-lookup"><span data-stu-id="8d0be-115">*StartDate*</span></span>  <br/> |<span data-ttu-id="8d0be-116">Une expression qui peut être résolue sur une valeur de Date/heure.</span><span class="sxs-lookup"><span data-stu-id="8d0be-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="8d0be-117">La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.</span><span class="sxs-lookup"><span data-stu-id="8d0be-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
| <span data-ttu-id="8d0be-118">*Date de fin*</span><span class="sxs-lookup"><span data-stu-id="8d0be-118">*EndDate*</span></span>  <br/> |<span data-ttu-id="8d0be-119">Une expression qui peut être résolue sur une valeur de Date/heure.</span><span class="sxs-lookup"><span data-stu-id="8d0be-119">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="8d0be-120">La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.</span><span class="sxs-lookup"><span data-stu-id="8d0be-120">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d0be-121">Remarques</span><span class="sxs-lookup"><span data-stu-id="8d0be-121">Remarks</span></span>

<span data-ttu-id="8d0be-122">Le tableau suivant répertorie tous les arguments *DatePart* valides.</span><span class="sxs-lookup"><span data-stu-id="8d0be-122">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="8d0be-123">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="8d0be-123">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="8d0be-124">**year**</span><span class="sxs-lookup"><span data-stu-id="8d0be-124">**year**</span></span> <br/> |
|<span data-ttu-id="8d0be-125">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="8d0be-125">**quarter**</span></span> <br/> |
|<span data-ttu-id="8d0be-126">**Mois**</span><span class="sxs-lookup"><span data-stu-id="8d0be-126">**month**</span></span> <br/> |
|<span data-ttu-id="8d0be-127">**DAYOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="8d0be-127">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="8d0be-128">**day**</span><span class="sxs-lookup"><span data-stu-id="8d0be-128">**day**</span></span> <br/> |
|<span data-ttu-id="8d0be-129">**semaine**</span><span class="sxs-lookup"><span data-stu-id="8d0be-129">**week**</span></span> <br/> |
|<span data-ttu-id="8d0be-130">**heure**</span><span class="sxs-lookup"><span data-stu-id="8d0be-130">**hour**</span></span> <br/> |
|<span data-ttu-id="8d0be-131">**minute**</span><span class="sxs-lookup"><span data-stu-id="8d0be-131">**minute**</span></span> <br/> |
|<span data-ttu-id="8d0be-132">**seconde**</span><span class="sxs-lookup"><span data-stu-id="8d0be-132">**second**</span></span> <br/> |
|<span data-ttu-id="8d0be-133">**milliseconde**</span><span class="sxs-lookup"><span data-stu-id="8d0be-133">**millisecond**</span></span> <br/> |
   

