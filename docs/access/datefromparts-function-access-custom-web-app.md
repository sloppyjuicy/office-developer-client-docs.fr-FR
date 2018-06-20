---
title: Fonction DateFromParts (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4fa49d5f-12ea-4d14-9a03-28418f01746c
description: Renvoie une valeur de date pour l’année, mois et jour.
ms.openlocfilehash: 5a2ff76d99076cf9f53b0dce8c5019f38d910f58
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781786"
---
# <a name="datefromparts-function-access-custom-web-app"></a><span data-ttu-id="ec071-103">Fonction DateFromParts (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="ec071-103">DateFromParts function (Access custom web app)</span></span>

<span data-ttu-id="ec071-104">Renvoie une valeur de date pour l’année, mois et jour.</span><span class="sxs-lookup"><span data-stu-id="ec071-104">Returns a date value for the specified year, month, and day.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ec071-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="ec071-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="ec071-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ec071-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ec071-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ec071-107">Syntax</span></span>

<span data-ttu-id="ec071-108">**DateFromParts** (*Année*, *mois*, *jour*)</span><span class="sxs-lookup"><span data-stu-id="ec071-108">**DateFromParts** (*Year*, *Month*, *Day*)</span></span> 
  
<span data-ttu-id="ec071-109">La fonction **DateFromParts** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="ec071-109">The **DateFromParts** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ec071-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="ec071-110">**Argument name**</span></span>|<span data-ttu-id="ec071-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ec071-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ec071-112">*Année*</span><span class="sxs-lookup"><span data-stu-id="ec071-112">*Year*</span></span>  <br/> |<span data-ttu-id="ec071-113">Expression d’entier spécifiant une année.</span><span class="sxs-lookup"><span data-stu-id="ec071-113">Integer expression specifying a year.</span></span>  <br/> |
| <span data-ttu-id="ec071-114">*Mois*</span><span class="sxs-lookup"><span data-stu-id="ec071-114">*Month*</span></span>  <br/> |<span data-ttu-id="ec071-115">Expression d’entier spécifiant un mois, de 1 à 12.</span><span class="sxs-lookup"><span data-stu-id="ec071-115">Integer expression specifying a month, from 1 to 12.</span></span>  <br/> |
| <span data-ttu-id="ec071-116">*Jour*</span><span class="sxs-lookup"><span data-stu-id="ec071-116">*Day*</span></span>  <br/> |<span data-ttu-id="ec071-117">Expression d’entier spécifiant un jour.</span><span class="sxs-lookup"><span data-stu-id="ec071-117">Integer expression specifying a day.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ec071-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="ec071-118">Remarks</span></span>

<span data-ttu-id="ec071-119">**DateFromParts** renvoie une valeur de date avec la partie de date définie pour l’année, mois et jour et la partie heure la valeur par défaut.</span><span class="sxs-lookup"><span data-stu-id="ec071-119">**DateFromParts** returns a date value with the date portion set to the specified year, month and day, and the time portion set to the default.</span></span> <span data-ttu-id="ec071-120">Si les arguments ne sont pas valides, une erreur est générée.</span><span class="sxs-lookup"><span data-stu-id="ec071-120">If the arguments are not valid, then an error is raised.</span></span> <span data-ttu-id="ec071-121">Si les arguments obligatoires sont nulles, NULL est renvoyée.</span><span class="sxs-lookup"><span data-stu-id="ec071-121">If required arguments are null, then NULL is returned.</span></span> 
  
## <a name="example"></a><span data-ttu-id="ec071-122">Exemple</span><span class="sxs-lookup"><span data-stu-id="ec071-122">Example</span></span>

<span data-ttu-id="ec071-123">L’expression suivante utilise la fonction **DateFromParts** pour calculer le premier jour du mois en cours.</span><span class="sxs-lookup"><span data-stu-id="ec071-123">The following expression uses the **DateFromParts** function to calculate the first day of the current month.</span></span> 
  
`DateFromParts(Year(Today()),Month(Today()),1)`



