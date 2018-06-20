---
title: Fonction DateWithTimeFromParts (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Renvoie une Date et le temps, basées sur une année, le mois, le jour et l’heure.
ms.openlocfilehash: 8cc1fbe700d18c04d944793bcea889424b0cff3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781784"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="123b6-103">Fonction DateWithTimeFromParts (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="123b6-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="123b6-104">Renvoie une Date et le temps, basées sur une année, le mois, le jour et l’heure.</span><span class="sxs-lookup"><span data-stu-id="123b6-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="123b6-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="123b6-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="123b6-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="123b6-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="123b6-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="123b6-107">Syntax</span></span>

<span data-ttu-id="123b6-108">**DateWithTimeFromParts** (*Année*, *mois*, *jour*, *heure*, *Minute*, *seconde*)</span><span class="sxs-lookup"><span data-stu-id="123b6-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="123b6-109">La fonction **DateWithTimeFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="123b6-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="123b6-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="123b6-110">**Argument name**</span></span>|<span data-ttu-id="123b6-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="123b6-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="123b6-112">*Année*</span><span class="sxs-lookup"><span data-stu-id="123b6-112">*Year*</span></span>  <br/> |<span data-ttu-id="123b6-113">Expression d’entier spécifiant une année.</span><span class="sxs-lookup"><span data-stu-id="123b6-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="123b6-114">*Mois*</span><span class="sxs-lookup"><span data-stu-id="123b6-114">*Month*</span></span>  <br/> |<span data-ttu-id="123b6-115">Expression d’entier spécifiant un mois.</span><span class="sxs-lookup"><span data-stu-id="123b6-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="123b6-116">*Jour*</span><span class="sxs-lookup"><span data-stu-id="123b6-116">*Day*</span></span>  <br/> |<span data-ttu-id="123b6-117">Expression d’entier spécifiant un jour.</span><span class="sxs-lookup"><span data-stu-id="123b6-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="123b6-118">*Heure*</span><span class="sxs-lookup"><span data-stu-id="123b6-118">*Hour*</span></span>  <br/> |<span data-ttu-id="123b6-119">Expression d’entier spécifiant les heures.</span><span class="sxs-lookup"><span data-stu-id="123b6-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="123b6-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="123b6-120">*Minute*</span></span>  <br/> |<span data-ttu-id="123b6-121">Expression d’entier indiquant les minutes.</span><span class="sxs-lookup"><span data-stu-id="123b6-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="123b6-122">*Seconde*</span><span class="sxs-lookup"><span data-stu-id="123b6-122">*Second*</span></span>  <br/> |<span data-ttu-id="123b6-123">Expression d’entier indiquant les secondes.</span><span class="sxs-lookup"><span data-stu-id="123b6-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="123b6-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="123b6-124">Remarks</span></span>

<span data-ttu-id="123b6-125">**DateWithTimeFromParts** renvoie une valeur de Date/heure entièrement initialisée.</span><span class="sxs-lookup"><span data-stu-id="123b6-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="123b6-126">Si les arguments ne sont pas valides, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="123b6-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="123b6-127">Si les arguments obligatoires sont Null, Null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="123b6-127">If required arguments are Null, then Null is returned.</span></span> 
  

