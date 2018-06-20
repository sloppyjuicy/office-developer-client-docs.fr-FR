---
title: Month, fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5df43594-a434-4fb7-8109-e5cf0401ae09
description: Renvoie un entier représentant le mois de la date spécifiée.
ms.openlocfilehash: 5e4a583a5a299456e57b90d7cef41a32b0a6ffba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781959"
---
# <a name="month-function-access-custom-web-app"></a><span data-ttu-id="63605-103">Month, fonction (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="63605-103">Month Function (Access custom web app)</span></span>

<span data-ttu-id="63605-104">Renvoie un entier représentant le mois de la date spécifiée.</span><span class="sxs-lookup"><span data-stu-id="63605-104">Returns an integer that represents the month of the specified date.</span></span>
  
> [!NOTE]
> <span data-ttu-id="63605-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="63605-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="63605-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="63605-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="63605-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="63605-107">Syntax</span></span>

 <span data-ttu-id="63605-108">**Mois** (*Date*)</span><span class="sxs-lookup"><span data-stu-id="63605-108">**Month** (*Date*)</span></span> 
  
<span data-ttu-id="63605-109">La fonction **Month** contient l’argument suivant.</span><span class="sxs-lookup"><span data-stu-id="63605-109">The **Month** function contains the following argument.</span></span> 
  
|<span data-ttu-id="63605-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="63605-110">**Argument name**</span></span>|<span data-ttu-id="63605-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="63605-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="63605-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="63605-112">*Date*</span></span>  <br/> |<span data-ttu-id="63605-113">Une expression qui peut être résolue sur une valeur de Date/heure.</span><span class="sxs-lookup"><span data-stu-id="63605-113">An expression that can be resolved to a Date/Time value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63605-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="63605-114">Remarks</span></span>

 <span data-ttu-id="63605-115">**Mois** renvoie la même valeur que **DatePart** (mois, date).</span><span class="sxs-lookup"><span data-stu-id="63605-115">**Month** returns the same value as **DatePart** (month, date).</span></span> 
  
<span data-ttu-id="63605-116">Si la *Date* contient uniquement une partie de l’heure, la valeur renvoyée est 1, le mois de base.</span><span class="sxs-lookup"><span data-stu-id="63605-116">If  *Date*  contains only a time part, the return value is 1, the base month.</span></span> 
  

