---
title: Fonction DateFromParts (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l'année, le mois et le jour spécifiés.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282121"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="70147-103">Fonction DateFromParts (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="70147-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="70147-104">Renvoie une valeur de date pour l'année, le mois et le jour spécifiés.</span><span class="sxs-lookup"><span data-stu-id="70147-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="70147-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="70147-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="70147-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="70147-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="70147-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="70147-107">Syntax</span></span>

<span data-ttu-id="70147-108">**DateFromParts** (*Année*, *mois*, *jour*)</span><span class="sxs-lookup"><span data-stu-id="70147-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="70147-109">La fonction **DateFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="70147-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="70147-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="70147-110">**Argument name**</span></span>|<span data-ttu-id="70147-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="70147-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="70147-112">*Année*</span><span class="sxs-lookup"><span data-stu-id="70147-112">*Year*</span></span>  <br/> |<span data-ttu-id="70147-113">Expression de nombre entier spécifiant une année.</span><span class="sxs-lookup"><span data-stu-id="70147-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="70147-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="70147-114">*Month*</span></span>  <br/> |<span data-ttu-id="70147-115">Expression entière spécifiant un mois, comprise entre 1 et 12.</span><span class="sxs-lookup"><span data-stu-id="70147-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="70147-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="70147-116">*Day*</span></span>  <br/> |<span data-ttu-id="70147-117">Expression de nombre entier spécifiant un jour.</span><span class="sxs-lookup"><span data-stu-id="70147-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70147-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="70147-118">Remarks</span></span>

<span data-ttu-id="70147-119">**DateFromParts** renvoie une valeur date dont la partie date est définie sur l'année, le mois et le jour spécifiés, et la partie heure sur la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="70147-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="70147-120">Si les arguments ne sont pas valides, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="70147-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="70147-121">Si les arguments requis sont NULL, NULL est renvoyé.</span><span class="sxs-lookup"><span data-stu-id="70147-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="70147-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="70147-122">Example</span></span>

<span data-ttu-id="70147-123">L'expression suivante utilise la fonction **DateFromParts** pour calculer le premier jour du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="70147-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



