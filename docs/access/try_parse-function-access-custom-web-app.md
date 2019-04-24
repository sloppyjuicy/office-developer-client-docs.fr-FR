---
title: Fonction Try_Parse (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ed35263c-b0ad-4269-9caa-c0164015e980
description: Analyse une valeur de texte dans le type de données spécifié dans la culture de l'application ou renvoie la valeur null si la conversion n'est pas valide.
ms.openlocfilehash: 5d201557607d2d18c36238d9658b705a6a49fda8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307797"
---
# <a name="tryparse-function-access-custom-web-app"></a><span data-ttu-id="567d9-103">Fonction Try_Parse (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="567d9-103">Try_Parse Function (Access custom web app)</span></span>

<span data-ttu-id="567d9-104">Analyse une valeur de texte dans le type de données spécifié dans la culture de l'application ou renvoie la valeur null si la conversion n'est pas valide.</span><span class="sxs-lookup"><span data-stu-id="567d9-104">Parses a text value to the specified data type in the culture of the application or returns Null if the conversion is not valid.</span></span>
  
> [!NOTE]
> <span data-ttu-id="567d9-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="567d9-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="567d9-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="567d9-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="567d9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="567d9-107">Syntax</span></span>

 <span data-ttu-id="567d9-108">**Try_Parse** (*TextExpression*, *DataType*)</span><span class="sxs-lookup"><span data-stu-id="567d9-108">**Try_Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="567d9-109">La fonction **Try_Parse** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="567d9-109">The **Try_Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="567d9-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="567d9-110">**Argument name**</span></span>|<span data-ttu-id="567d9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="567d9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="567d9-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="567d9-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="567d9-113">Expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="567d9-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="567d9-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="567d9-114">*DataType*</span></span>  <br/> |<span data-ttu-id="567d9-115">Le type de données dans lequel analyser *TextExpression* .</span><span class="sxs-lookup"><span data-stu-id="567d9-115">The data type into which to parse  *TextExpression*  .</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="567d9-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="567d9-116">Remarks</span></span>

<span data-ttu-id="567d9-117">Utilisez **Try_Parse** uniquement pour convertir une chaîne en type de date/heure et de nombre.</span><span class="sxs-lookup"><span data-stu-id="567d9-117">Use **Try_Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="567d9-118">Pour les conversions de type générales, continuez à utiliser **Convert**.</span><span class="sxs-lookup"><span data-stu-id="567d9-118">For general type conversions, continue to use **Convert**.</span></span> 
  

