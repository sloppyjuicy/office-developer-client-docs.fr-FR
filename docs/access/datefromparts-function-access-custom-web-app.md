---
title: Fonction DateFromParts (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.
ms.openlocfilehash: 7d47fe93d1990365f1db5885a3ea8fc056aabb9f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423222"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="02750-103">Fonction DateFromParts (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="02750-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="02750-104">Renvoie une valeur de date pour l’année, le mois et le jour spécifiés.</span><span class="sxs-lookup"><span data-stu-id="02750-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="02750-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="02750-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="02750-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="02750-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="02750-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="02750-107">Syntax</span></span>

<span data-ttu-id="02750-108">**DateFromParts** (*Year*, *Month*, *Day*)</span><span class="sxs-lookup"><span data-stu-id="02750-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="02750-109">La **fonction DateFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="02750-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="02750-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="02750-110">**Argument name**</span></span>|<span data-ttu-id="02750-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="02750-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="02750-112">*Année*</span><span class="sxs-lookup"><span data-stu-id="02750-112">*Year*</span></span>  <br/> |<span data-ttu-id="02750-113">Expression de nombres integer spécifiant une année.</span><span class="sxs-lookup"><span data-stu-id="02750-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="02750-114">*Month*</span><span class="sxs-lookup"><span data-stu-id="02750-114">*Month*</span></span>  <br/> |<span data-ttu-id="02750-115">Expression de nombres integer spécifiant un mois, de 1 à 12.</span><span class="sxs-lookup"><span data-stu-id="02750-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="02750-116">*Day*</span><span class="sxs-lookup"><span data-stu-id="02750-116">*Day*</span></span>  <br/> |<span data-ttu-id="02750-117">Expression de nombres integer spécifiant un jour.</span><span class="sxs-lookup"><span data-stu-id="02750-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02750-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="02750-118">Remarks</span></span>

<span data-ttu-id="02750-119">**DateFromParts** renvoie une valeur de date avec la partie date définie sur l’année, le mois et le jour spécifiés, et la partie heure définie sur la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="02750-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="02750-120">Si les arguments ne sont pas valides, une erreur se produit.</span><span class="sxs-lookup"><span data-stu-id="02750-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="02750-121">Si les arguments obligatoires sont null, la valeur NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="02750-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="02750-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="02750-122">Example</span></span>

<span data-ttu-id="02750-123">L’expression suivante utilise **la fonction DateFromParts** pour calculer le premier jour du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="02750-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



