---
title: Year Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: 1400c352bcc070035d15b46f8e547e4637364299
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433121"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="e73f8-103">Year Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="e73f8-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="e73f8-104">Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="e73f8-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e73f8-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="e73f8-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="e73f8-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e73f8-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e73f8-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e73f8-107">Syntax</span></span>

 <span data-ttu-id="e73f8-108">**Year** (*Date*)</span><span class="sxs-lookup"><span data-stu-id="e73f8-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="e73f8-109">La **fonction Year** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e73f8-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e73f8-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="e73f8-110">**Argument name**</span></span>|<span data-ttu-id="e73f8-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e73f8-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e73f8-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="e73f8-112">*Date*</span></span>  <br/> |<span data-ttu-id="e73f8-113">Expression qui peut être résolue en valeur Date/Heure.</span><span class="sxs-lookup"><span data-stu-id="e73f8-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="e73f8-114">Expression  *d’argument Date,*  expression de colonne, variable définie par l’utilisateur ou littéral de chaîne.</span><span class="sxs-lookup"><span data-stu-id="e73f8-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e73f8-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="e73f8-115">Remarks</span></span>

<span data-ttu-id="e73f8-116">Les valeurs renvoyées par les fonctions **Year**, **Month** et **Day** sont des valeurs grégoriennes, quel que soit le format d’affichage de la valeur de date fournie.</span><span class="sxs-lookup"><span data-stu-id="e73f8-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="e73f8-117">Par exemple, si le format d’affichage de la date fournie utilise le calendrier Hijri, les valeurs renvoyées pour les fonctions **Year**, **Month** et **Day** seront des valeurs associées à la date grégorienne équivalente.</span><span class="sxs-lookup"><span data-stu-id="e73f8-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

