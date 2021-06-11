---
title: Fonction DateWithTimeFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: aa97cbaa-8b14-42e3-a098-938ebe0769eb
description: Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.
ms.openlocfilehash: ee995d346ca27e683f342cf3f611c1147997d24e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422088"
---
# <a name="datewithtimefromparts-function-access-custom-web-app"></a><span data-ttu-id="de82f-103">Fonction DateWithTimeFromParts (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="de82f-103">DateWithTimeFromParts function (Access custom web app)</span></span>

<span data-ttu-id="de82f-104">Renvoie une date et une heure basées sur une année, un mois, un jour et une heure spécifiés.</span><span class="sxs-lookup"><span data-stu-id="de82f-104">Returns a Date and Time based on a specified year, month, day, and time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="de82f-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="de82f-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="de82f-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="de82f-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="de82f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="de82f-107">Syntax</span></span>

<span data-ttu-id="de82f-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day,* *Hour,* *Minute*, *Second*)</span><span class="sxs-lookup"><span data-stu-id="de82f-108">**DateWithTimeFromParts** (*Year*, *Month*, *Day*, *Hour*, *Minute*, *Second*)</span></span> 
  
<span data-ttu-id="de82f-109">La **fonction DateWithTimeFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="de82f-109">The **DateWithTimeFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="de82f-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="de82f-110">**Argument name**</span></span>|<span data-ttu-id="de82f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="de82f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="de82f-112">*Année*</span><span class="sxs-lookup"><span data-stu-id="de82f-112">*Year*</span></span>  <br/> |<span data-ttu-id="de82f-113">Expression de nombres integer spécifiant une année.</span><span class="sxs-lookup"><span data-stu-id="de82f-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="de82f-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="de82f-114">*Month*</span></span>  <br/> |<span data-ttu-id="de82f-115">Expression de nombres integer spécifiant un mois.</span><span class="sxs-lookup"><span data-stu-id="de82f-115">Integer expression specifying a month.</span></span>  <br/> |
| <span data-ttu-id="de82f-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="de82f-116">*Day*</span></span>  <br/> |<span data-ttu-id="de82f-117">Expression de nombres integer spécifiant un jour.</span><span class="sxs-lookup"><span data-stu-id="de82f-117">Integer expression specifying a day.</span></span>  <br/> |
| <span data-ttu-id="de82f-118">*Hour*</span><span class="sxs-lookup"><span data-stu-id="de82f-118">*Hour*</span></span>  <br/> |<span data-ttu-id="de82f-119">Expression de nombres integer spécifiant les heures.</span><span class="sxs-lookup"><span data-stu-id="de82f-119">Integer expression specifying hours.</span></span>  <br/> |
| <span data-ttu-id="de82f-120">*Minute*</span><span class="sxs-lookup"><span data-stu-id="de82f-120">*Minute*</span></span>  <br/> |<span data-ttu-id="de82f-121">Expression de nombres integer spécifiant les minutes.</span><span class="sxs-lookup"><span data-stu-id="de82f-121">Integer expression specifying minutes.</span></span>  <br/> |
| <span data-ttu-id="de82f-122">*Second*</span><span class="sxs-lookup"><span data-stu-id="de82f-122">*Second*</span></span>  <br/> |<span data-ttu-id="de82f-123">Expression de nombres integer spécifiant les secondes.</span><span class="sxs-lookup"><span data-stu-id="de82f-123">Integer expression specifying seconds.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de82f-124">Remarques</span><span class="sxs-lookup"><span data-stu-id="de82f-124">Remarks</span></span>

<span data-ttu-id="de82f-125">**DateWithTimeFromParts** renvoie une valeur Date/Heure entièrement initialisée.</span><span class="sxs-lookup"><span data-stu-id="de82f-125">**DateWithTimeFromParts** returns a fully initialized Date/Time value.</span></span> <span data-ttu-id="de82f-126">Si les arguments ne sont pas valides, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="de82f-126">If the arguments are not valid, an error is raised.</span></span> <span data-ttu-id="de82f-127">Si les arguments obligatoires sont Null, null est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="de82f-127">If required arguments are Null, then Null is returned.</span></span> 
  

