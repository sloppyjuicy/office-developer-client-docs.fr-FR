---
title: EOMonth Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: df98bcca-152b-49f2-b4e1-35d68008fb8f
description: Renvoie le dernier jour du mois avant ou le nombre spécifié de mois.
ms.openlocfilehash: 87a837069be223fdd2f9c809d706782e0955e2aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437454"
---
# <a name="eomonth-function-access-custom-web-app"></a><span data-ttu-id="10f0d-103">EOMonth Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="10f0d-103">EOMonth Function (Access custom web app)</span></span>

<span data-ttu-id="10f0d-104">Renvoie le dernier jour du mois avant ou le nombre spécifié de mois.</span><span class="sxs-lookup"><span data-stu-id="10f0d-104">Returns the last day of the month before or specified number of months.</span></span>
  
> [!NOTE]
> <span data-ttu-id="10f0d-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="10f0d-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="10f0d-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="10f0d-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="10f0d-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="10f0d-107">Syntax</span></span>

 <span data-ttu-id="10f0d-108">**EOMonth** (*Date*, *NumberOfMonth*)</span><span class="sxs-lookup"><span data-stu-id="10f0d-108">**EOMonth** (*Date*, *NumberOfMonth*)</span></span> 
  
<span data-ttu-id="10f0d-109">**EOMonth contient** les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="10f0d-109">The **EOMonth** contains the following arguments.</span></span> 
  
|<span data-ttu-id="10f0d-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="10f0d-110">**Argument name**</span></span>|<span data-ttu-id="10f0d-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="10f0d-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="10f0d-112">*Date*</span><span class="sxs-lookup"><span data-stu-id="10f0d-112">*Date*</span></span>  <br/> |<span data-ttu-id="10f0d-113">Date de début au format Date/Heure ou dans une représentation texte acceptée d’une date.</span><span class="sxs-lookup"><span data-stu-id="10f0d-113">The start date in Date/Time format, or in an accepted text representation of a date.</span></span>  <br/> |
| <span data-ttu-id="10f0d-114">*NumberOfMonth*</span><span class="sxs-lookup"><span data-stu-id="10f0d-114">*NumberOfMonth*</span></span>  <br/> |<span data-ttu-id="10f0d-115">Nombre représentant le nombre de mois avant ou après la  *date*  .</span><span class="sxs-lookup"><span data-stu-id="10f0d-115">A number representing the number of months before or after the  *Date*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10f0d-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="10f0d-116">Remarks</span></span>

<span data-ttu-id="10f0d-117">Si  *Date n’est*  pas une date valide, **EOMonth** renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="10f0d-117">If  *Date*  is not a valid date, **EOMonth** returns an error.</span></span> 
  
<span data-ttu-id="10f0d-118">Si  *Date*  plus  *NumberOfMonth*  produit une date non valide, **EOMonth** renvoie une erreur.</span><span class="sxs-lookup"><span data-stu-id="10f0d-118">If  *Date*  plus  *NumberOfMonth*  yields an invalid date, **EOMonth** returns an error.</span></span> 
  

