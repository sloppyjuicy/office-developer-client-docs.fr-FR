---
title: Fonction DatePart (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8936f0b6-f9b2-44ef-bf90-e482b64611cd
description: Renvoie une valeur numérique qui représente la partie de la date spécifiée de la date spécifiée.
ms.openlocfilehash: 81aa1880e5b38c33f75018418a44ed82e5e7e8c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781796"
---
# <a name="datepart-function-access-custom-web-app"></a><span data-ttu-id="36b12-103">Fonction DatePart (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="36b12-103">DatePart function (Access custom web app)</span></span>

<span data-ttu-id="36b12-104">Renvoie une valeur numérique qui représente la partie de la date spécifiée de la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="36b12-104">Returns a numeric value that represents the specified date part of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="36b12-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="36b12-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="36b12-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="36b12-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36b12-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="36b12-107">Syntax</span></span>

<span data-ttu-id="36b12-108">**DatePart** (*DatePart*, *Date*)</span><span class="sxs-lookup"><span data-stu-id="36b12-108">**DatePart** (*DatePart*, *Date*)</span></span> 
  
<span data-ttu-id="36b12-109">La fonction **DatePart** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="36b12-109">The **DatePart** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="36b12-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="36b12-110">**Argument name**</span></span>|<span data-ttu-id="36b12-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="36b12-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="36b12-112">*DatePart*</span><span class="sxs-lookup"><span data-stu-id="36b12-112">*DatePart*</span></span>  <br/> |<span data-ttu-id="36b12-113">La partie de *Date* (une valeur de date ou heure) pour lequel un entier s’afficheront.</span><span class="sxs-lookup"><span data-stu-id="36b12-113">The part of  *Date*  (a date or time value) for which an integer will be returned.</span></span> <span data-ttu-id="36b12-114">Reportez-vous à la section Remarques pour la liste des abréviations valides.</span><span class="sxs-lookup"><span data-stu-id="36b12-114">Refer to the Remarks section for the list of valid abbreviations.</span></span>  <br/> |
| <span data-ttu-id="36b12-115">*Date*</span><span class="sxs-lookup"><span data-stu-id="36b12-115">*Date*</span></span>  <br/> |<span data-ttu-id="36b12-116">Une expression qui peut être résolue sur une valeur de Date/heure.</span><span class="sxs-lookup"><span data-stu-id="36b12-116">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="36b12-117">La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.</span><span class="sxs-lookup"><span data-stu-id="36b12-117">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36b12-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="36b12-118">Remarks</span></span>

<span data-ttu-id="36b12-119">Le tableau suivant répertorie tous les arguments *DatePart* valides.</span><span class="sxs-lookup"><span data-stu-id="36b12-119">The following table lists all valid  *DatePart*  arguments.</span></span> 
  
|<span data-ttu-id="36b12-120">***DatePart***</span><span class="sxs-lookup"><span data-stu-id="36b12-120">***DatePart***</span></span>|
|:-----|
|<span data-ttu-id="36b12-121">**year**</span><span class="sxs-lookup"><span data-stu-id="36b12-121">**year**</span></span> <br/> |
|<span data-ttu-id="36b12-122">**trimestre**</span><span class="sxs-lookup"><span data-stu-id="36b12-122">**quarter**</span></span> <br/> |
|<span data-ttu-id="36b12-123">**Mois**</span><span class="sxs-lookup"><span data-stu-id="36b12-123">**month**</span></span> <br/> |
|<span data-ttu-id="36b12-124">**DAYOFYEAR**</span><span class="sxs-lookup"><span data-stu-id="36b12-124">**dayofyear**</span></span> <br/> |
|<span data-ttu-id="36b12-125">**day**</span><span class="sxs-lookup"><span data-stu-id="36b12-125">**day**</span></span> <br/> |
|<span data-ttu-id="36b12-126">**semaine**</span><span class="sxs-lookup"><span data-stu-id="36b12-126">**week**</span></span> <br/> |
|<span data-ttu-id="36b12-127">**Weekday**</span><span class="sxs-lookup"><span data-stu-id="36b12-127">**weekday**</span></span> <br/> |
|<span data-ttu-id="36b12-128">**heure**</span><span class="sxs-lookup"><span data-stu-id="36b12-128">**hour**</span></span> <br/> |
|<span data-ttu-id="36b12-129">**minute**</span><span class="sxs-lookup"><span data-stu-id="36b12-129">**minute**</span></span> <br/> |
|<span data-ttu-id="36b12-130">**seconde**</span><span class="sxs-lookup"><span data-stu-id="36b12-130">**second**</span></span> <br/> |
|<span data-ttu-id="36b12-131">**milliseconde**</span><span class="sxs-lookup"><span data-stu-id="36b12-131">**millisecond**</span></span> <br/> |
   

