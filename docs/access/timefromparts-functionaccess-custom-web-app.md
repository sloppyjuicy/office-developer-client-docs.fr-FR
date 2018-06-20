---
title: Fonction TimeFromParts (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Renvoie une valeur de temps en fonction de composants spécifiés.
ms.openlocfilehash: 55a4d1c31fdd2248e3e154d83e803d9f5a5ebb06
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781989"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="08068-103">Fonction TimeFromParts (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="08068-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="08068-104">Renvoie une valeur de temps en fonction de composants spécifiés.</span><span class="sxs-lookup"><span data-stu-id="08068-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="08068-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="08068-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="08068-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="08068-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="08068-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="08068-107">Syntax</span></span>

 <span data-ttu-id="08068-108">**TimeFromParts** (*Heure*, *Minute*, *seconde*)</span><span class="sxs-lookup"><span data-stu-id="08068-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="08068-109">La fonction **TimeFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="08068-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="08068-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="08068-110">**Argument name**</span></span>|<span data-ttu-id="08068-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="08068-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="08068-112">*Heure*</span><span class="sxs-lookup"><span data-stu-id="08068-112">*Hour*</span></span>  <br/> |<span data-ttu-id="08068-113">Expression d’entier spécifiant les heures.</span><span class="sxs-lookup"><span data-stu-id="08068-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="08068-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="08068-114">*Minute*</span></span>  <br/> |<span data-ttu-id="08068-115">Expression d’entier indiquant les minutes.</span><span class="sxs-lookup"><span data-stu-id="08068-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="08068-116">*Seconde*</span><span class="sxs-lookup"><span data-stu-id="08068-116">*Second*</span></span>  <br/> |<span data-ttu-id="08068-117">Expression d’entier indiquant les secondes.</span><span class="sxs-lookup"><span data-stu-id="08068-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="08068-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="08068-118">See also</span></span>

 <span data-ttu-id="08068-119">**TimeFromParts** renvoie une valeur d’heure entièrement initialisé.</span><span class="sxs-lookup"><span data-stu-id="08068-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="08068-120">Si les arguments ne sont pas valides, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="08068-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="08068-121">Si un des paramètres est null, la valeur null est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="08068-121">If any of the parameters are null, null is returned.</span></span> 
  

