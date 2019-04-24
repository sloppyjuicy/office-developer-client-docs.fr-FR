---
title: Fonction Day (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0a77e4-0653-4a85-b507-13440aef195b
description: Renvoie un entier représentant le jour (jour du mois) de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: 720adaffbd97a735f6b1395e64965f972c6099cd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280690"
---
# <a name="day-function-access-custom-web-app"></a><span data-ttu-id="3d87c-103">Fonction Day (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="3d87c-103">Day function (Access custom web app)</span></span>

<span data-ttu-id="3d87c-104">Renvoie un entier représentant le jour (jour du mois) de la date spécifiée dans le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="3d87c-104">Returns an integer representing the day (day of the month) of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3d87c-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="3d87c-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="3d87c-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="3d87c-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3d87c-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d87c-107">Syntax</span></span>

<span data-ttu-id="3d87c-108">**Jour** (*Date*)</span><span class="sxs-lookup"><span data-stu-id="3d87c-108">**Day** (*Date*)</span></span> 
  
<span data-ttu-id="3d87c-109">La fonction **Day** contient l'argument suivant.</span><span class="sxs-lookup"><span data-stu-id="3d87c-109">The **Day** function contains the following argument.</span></span> 
  
|<span data-ttu-id="3d87c-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="3d87c-110">**Argument name**</span></span>|<span data-ttu-id="3d87c-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="3d87c-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3d87c-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="3d87c-112">*Date*</span></span>  <br/> |<span data-ttu-id="3d87c-113">Expression qui peut être résolue en une valeur de date/heure.</span><span class="sxs-lookup"><span data-stu-id="3d87c-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="3d87c-114">Expression de l'argument *Date* , expression de colonne, variable ou littéral de chaîne défini par l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3d87c-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3d87c-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="3d87c-115">Remarks</span></span>

<span data-ttu-id="3d87c-116">**Day** renvoie la même valeur que **DatePart** (Day, date).</span><span class="sxs-lookup"><span data-stu-id="3d87c-116">**Day** returns the same value as **Datepart** (day, date).</span></span> 
  

