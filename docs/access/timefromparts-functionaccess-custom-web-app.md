---
title: Fonction TimeFromParts (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f631b7e-6e3c-46dc-a05f-6a07f9a91268
description: Renvoie une valeur d'heure basée sur des parties spécifiées.
ms.openlocfilehash: 8e2105140056bc65e9af0a6eda6e40fc44caed1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304248"
---
# <a name="timefromparts-function-access-custom-web-app"></a><span data-ttu-id="cfb05-103">Fonction TimeFromParts (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="cfb05-103">TimeFromParts Function (Access custom web app)</span></span>

<span data-ttu-id="cfb05-104">Renvoie une valeur d'heure basée sur des parties spécifiées.</span><span class="sxs-lookup"><span data-stu-id="cfb05-104">Returns a time value based on specified parts.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cfb05-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="cfb05-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="cfb05-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="cfb05-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="cfb05-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cfb05-107">Syntax</span></span>

 <span data-ttu-id="cfb05-108">**TimeFromParts** (*Heure*, *minute*, *seconde*)</span><span class="sxs-lookup"><span data-stu-id="cfb05-108">**TimeFromParts** (*Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="cfb05-109">La fonction **TimeFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="cfb05-109">The **TimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="cfb05-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="cfb05-110">**Argument name**</span></span>|<span data-ttu-id="cfb05-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="cfb05-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cfb05-112">*Hour*</span><span class="sxs-lookup"><span data-stu-id="cfb05-112">*Hour*</span></span>  <br/> |<span data-ttu-id="cfb05-113">Expression de type Integer qui spécifie les heures.</span><span class="sxs-lookup"><span data-stu-id="cfb05-113">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="cfb05-114">*Minute*</span><span class="sxs-lookup"><span data-stu-id="cfb05-114">*Minute*</span></span>  <br/> |<span data-ttu-id="cfb05-115">Expression de nombre entier spécifiant des minutes.</span><span class="sxs-lookup"><span data-stu-id="cfb05-115">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="cfb05-116">*Second*</span><span class="sxs-lookup"><span data-stu-id="cfb05-116">*Second*</span></span>  <br/> |<span data-ttu-id="cfb05-117">Expression de type Integer qui spécifie les secondes.</span><span class="sxs-lookup"><span data-stu-id="cfb05-117">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cfb05-118">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cfb05-118">See also</span></span>

 <span data-ttu-id="cfb05-119">**TimeFromParts** renvoie une valeur d'heure entièrement initialisée.</span><span class="sxs-lookup"><span data-stu-id="cfb05-119">**TimeFromParts** returns a fully initialized time value.</span></span> <span data-ttu-id="cfb05-120">Si les arguments ne sont pas valides, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="cfb05-120">If the arguments are invalid, then an error is raised.</span></span> <span data-ttu-id="cfb05-121">Si l'un des paramètres est null, NULL est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="cfb05-121">If any of the parameters are null, null is returned.</span></span> 
  

