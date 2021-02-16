---
title: Month Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Renvoie un nombre integer qui représente le mois de la date spécifiée.
ms.openlocfilehash: 0ca7059a2fd6dad1f9790ad6f4eafe7affa014dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411490"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="2dbfa-103">Month Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="2dbfa-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="2dbfa-104">Renvoie un nombre integer qui représente le mois de la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="2dbfa-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2dbfa-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="2dbfa-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="2dbfa-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="2dbfa-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2dbfa-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2dbfa-107">Syntax</span></span>

 <span data-ttu-id="2dbfa-108">**Month** (*Date*)</span><span class="sxs-lookup"><span data-stu-id="2dbfa-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="2dbfa-109">La **fonction Month** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="2dbfa-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="2dbfa-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="2dbfa-110">**Argument name**</span></span>|<span data-ttu-id="2dbfa-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="2dbfa-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2dbfa-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="2dbfa-112">*Date*</span></span>  <br/> |<span data-ttu-id="2dbfa-113">Expression qui peut être résolue en valeur Date/Heure.</span><span class="sxs-lookup"><span data-stu-id="2dbfa-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dbfa-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="2dbfa-114">Remarks</span></span>

 <span data-ttu-id="2dbfa-115">**Month** renvoie la même valeur que **DatePart** (mois, date).</span><span class="sxs-lookup"><span data-stu-id="2dbfa-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="2dbfa-116">Si  *Date*  ne contient qu’une partie de l’heure, la valeur de retour est 1, le mois de base.</span><span class="sxs-lookup"><span data-stu-id="2dbfa-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

