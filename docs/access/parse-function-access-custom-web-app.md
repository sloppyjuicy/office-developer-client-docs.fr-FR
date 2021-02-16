---
title: Parse Function (Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: d664985ab1d7a7d33b99c52d5bab4aa714767e40
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411133"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="ff36e-103">Parse Function (Access custom web app)</span><span class="sxs-lookup"><span data-stu-id="ff36e-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="ff36e-104">Elle pare une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.</span><span class="sxs-lookup"><span data-stu-id="ff36e-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ff36e-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="ff36e-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="ff36e-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="ff36e-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ff36e-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ff36e-107">Syntax</span></span>

 <span data-ttu-id="ff36e-108">**Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="ff36e-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="ff36e-109">La **fonction Parse** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="ff36e-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="ff36e-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="ff36e-110">**Argument name**</span></span>|<span data-ttu-id="ff36e-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="ff36e-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ff36e-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="ff36e-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="ff36e-113">Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="ff36e-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="ff36e-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="ff36e-114">*DataType*</span></span>  <br/> |<span data-ttu-id="ff36e-115">Valeur littérale représentant le type de données demandé pour le résultat.</span><span class="sxs-lookup"><span data-stu-id="ff36e-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ff36e-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="ff36e-116">Remarks</span></span>

<span data-ttu-id="ff36e-117">Utilisez **l’utilisation de l’exemple** uniquement pour la conversion de chaînes en types de date/heure et de nombre.</span><span class="sxs-lookup"><span data-stu-id="ff36e-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="ff36e-118">Pour les conversions de type général, utilisez **la fonction Convert.**</span><span class="sxs-lookup"><span data-stu-id="ff36e-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="ff36e-119">Gardez à l’esprit qu’il existe une certaine surcharge de performances lors de l’l’exécution de l’une des valeurs de chaîne.</span><span class="sxs-lookup"><span data-stu-id="ff36e-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

