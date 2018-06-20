---
title: Year, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a70751eb-bfde-4f7d-ad90-a1e4cca25dbc
description: Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.
ms.openlocfilehash: f9d72343637734257a2ed9589e5539b845933826
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782010"
---
# <a name="year-function-access-custom-web-app"></a><span data-ttu-id="ae711-103">Year, fonction (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="ae711-103">Year Function (Access custom web app)</span></span>

<span data-ttu-id="ae711-104">Renvoie une valeur numérique qui représente l’année de la date spécifiée dans le calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="ae711-104">Returns a numeric value that represents the year of the specified date in the Gregorian calendar.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ae711-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="ae711-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="ae711-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ae711-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ae711-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ae711-107">Syntax</span></span>

 <span data-ttu-id="ae711-108">**Année** (*Date*)</span><span class="sxs-lookup"><span data-stu-id="ae711-108">**Year** (*Date*)</span></span> 
  
<span data-ttu-id="ae711-109">La fonction **Year** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="ae711-109">The **Year** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ae711-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="ae711-110">**Argument name**</span></span>|<span data-ttu-id="ae711-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ae711-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ae711-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="ae711-112">*Date*</span></span>  <br/> |<span data-ttu-id="ae711-113">Une expression qui peut être résolue sur une valeur de Date/heure.</span><span class="sxs-lookup"><span data-stu-id="ae711-113">An expression that can be resolved to a Date/Time value.</span></span> <span data-ttu-id="ae711-114">La *Date argument* , l’expression de colonne, variable définie par l’utilisateur ou une expression chaîne littérale.</span><span class="sxs-lookup"><span data-stu-id="ae711-114">The  *Date*  argument expression, column expression, user-defined variable or string literal.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ae711-115">Remarques</span><span class="sxs-lookup"><span data-stu-id="ae711-115">Remarks</span></span>

<span data-ttu-id="ae711-116">Valeurs renvoyées par les fonctions de **l’année**, **mois**et **jour** seront grégorien quel que soit le format d’affichage de la valeur de date fournie.</span><span class="sxs-lookup"><span data-stu-id="ae711-116">Values returned by the **Year**, **Month**, and **Day** functions will be Gregorian values regardless of the display format for the supplied date value.</span></span> <span data-ttu-id="ae711-117">Par exemple, si le format d’affichage de la date fournie utilise le calendrier Hijri, les valeurs renvoyées pour **l’année**, **mois**et **jour** fonctions s’être valeurs associé à la date du calendrier grégorien.</span><span class="sxs-lookup"><span data-stu-id="ae711-117">For example, if the display format of the supplied date uses the Hijri calendar, the returned values for the **Year**, **Month**, and **Day** functions will be values associated with the equivalent Gregorian date.</span></span> 
  

