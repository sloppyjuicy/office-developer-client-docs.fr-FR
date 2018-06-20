---
title: Analyser la fonction (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09dee0ae-89b2-449c-a3c8-d6b270710b64
description: Analyse d’une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.
ms.openlocfilehash: fa3c453f1faeadca173aaace513ee5ba9115c5fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781962"
---
# <a name="parse-function-access-custom-web-app"></a><span data-ttu-id="53e6f-103">Analyser la fonction (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="53e6f-103">Parse Function (Access custom web app)</span></span>

<span data-ttu-id="53e6f-104">Analyse d’une valeur de texte et renvoie sa valeur dans un type donné à l’aide de la culture de l’application.</span><span class="sxs-lookup"><span data-stu-id="53e6f-104">Parses a text value and returns its value in a given type using the culture of the application.</span></span>
  
> [!NOTE]
> <span data-ttu-id="53e6f-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="53e6f-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="53e6f-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="53e6f-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="53e6f-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53e6f-107">Syntax</span></span>

 <span data-ttu-id="53e6f-108">**Analyser** (*TextExpression*, *type de données*)</span><span class="sxs-lookup"><span data-stu-id="53e6f-108">**Parse** (*TextExpression*, *DataType*)</span></span> 
  
<span data-ttu-id="53e6f-109">La fonction **Parse** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="53e6f-109">The **Parse** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="53e6f-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="53e6f-110">**Argument name**</span></span>|<span data-ttu-id="53e6f-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="53e6f-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="53e6f-112">*TextExpression*</span><span class="sxs-lookup"><span data-stu-id="53e6f-112">*TextExpression*</span></span>  <br/> |<span data-ttu-id="53e6f-113">Une expression de texte représentant la valeur mise en forme à analyser dans le type de données spécifié.</span><span class="sxs-lookup"><span data-stu-id="53e6f-113">A text expression representing the formatted value to parse into the specified data type.</span></span>  <br/> |
| <span data-ttu-id="53e6f-114">*DataType*</span><span class="sxs-lookup"><span data-stu-id="53e6f-114">*DataType*</span></span>  <br/> |<span data-ttu-id="53e6f-115">Valeur littérale qui représente le type de données demandé pour le résultat.</span><span class="sxs-lookup"><span data-stu-id="53e6f-115">Literal value representing the data type requested for the result.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53e6f-116">Remarques</span><span class="sxs-lookup"><span data-stu-id="53e6f-116">Remarks</span></span>

<span data-ttu-id="53e6f-117">Utilisez **analyser** uniquement pour réaliser la conversion d’une chaîne de date/heure et types de numéros.</span><span class="sxs-lookup"><span data-stu-id="53e6f-117">Use **Parse** only for converting from string to date/time and number types.</span></span> <span data-ttu-id="53e6f-118">Pour les conversions de type général, utilisez la fonction **Convert** .</span><span class="sxs-lookup"><span data-stu-id="53e6f-118">For general type conversions, use the **Convert** function.</span></span> <span data-ttu-id="53e6f-119">N’oubliez pas qu’il existe certaines performances une surcharge de l’analyse de la valeur de chaîne.</span><span class="sxs-lookup"><span data-stu-id="53e6f-119">Keep in mind that there is a certain performance overhead in parsing the string value.</span></span> 
  

