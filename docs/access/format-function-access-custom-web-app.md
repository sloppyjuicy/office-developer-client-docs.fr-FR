---
title: Fonction de format (application web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Renvoie une valeur mise en forme selon un modèle spécifié.
localization_priority: Priority
ms.openlocfilehash: 5331df30f276a7edd0571e9bf24c759d57ec6a54
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308203"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="e1397-103">Fonction de format (application web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="e1397-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="e1397-104">Renvoie une valeur mise en forme selon un modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="e1397-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1397-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="e1397-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="e1397-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="e1397-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e1397-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1397-107">Syntax</span></span>

 <span data-ttu-id="e1397-108">**Format** (*Expression*, *Format*)</span><span class="sxs-lookup"><span data-stu-id="e1397-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="e1397-109">La fonction **Format** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="e1397-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="e1397-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="e1397-110">**Argument name**</span></span>|<span data-ttu-id="e1397-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="e1397-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e1397-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="e1397-112">*Expression*</span></span>  <br/> |<span data-ttu-id="e1397-113">Expression d’un type de données pris en charge à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="e1397-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="e1397-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="e1397-114">*Format*</span></span>  <br/> | <span data-ttu-id="e1397-115">Un modèle de format.</span><span class="sxs-lookup"><span data-stu-id="e1397-115">A format pattern.</span></span> <span data-ttu-id="e1397-116">L’argument Format doit contenir une chaîne de format valide, soit sous la forme d’une chaîne de format standard (par exemple, « C » ou « D ») ou d’un modèle de caractères personnalisés pour les dates et des valeurs numériques (par exemple, « MMMM jj, aaaa (jjjj) »).</span><span class="sxs-lookup"><span data-stu-id="e1397-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="e1397-117">Pour plus d’informations, consultez la rubrique Remarques.</span><span class="sxs-lookup"><span data-stu-id="e1397-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1397-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="e1397-118">Remarks</span></span>

<span data-ttu-id="e1397-119">Pour le paramètre *Format*, vous pouvez passer des chaînes qui correspondent à l’un des modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="e1397-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="e1397-120">Chaînes de format numériques standard</span><span class="sxs-lookup"><span data-stu-id="e1397-120">Standard Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="e1397-121">Chaînes de format numériques personnalisées</span><span class="sxs-lookup"><span data-stu-id="e1397-121">Custom Numeric Format Strings</span></span>](https://msdn.microsoft.com/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="e1397-122">Chaînes de format de date et heure standard</span><span class="sxs-lookup"><span data-stu-id="e1397-122">Standard Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="e1397-123">Chaînes de format de date et heure personnalisées</span><span class="sxs-lookup"><span data-stu-id="e1397-123">Custom Date and Time Format Strings</span></span>](https://msdn.microsoft.com/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="e1397-124">Vous ne pouvez pas utiliser la fonction **Format** dans les zones suivantes d’applications web Access 2013 :</span><span class="sxs-lookup"><span data-stu-id="e1397-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="e1397-125">Colonnes calculées au niveau du tableau</span><span class="sxs-lookup"><span data-stu-id="e1397-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="e1397-126">Macros d’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="e1397-126">UI macros</span></span>
    
- <span data-ttu-id="e1397-127">Expressions dans les vues (par exemple, dans les formulaires)</span><span class="sxs-lookup"><span data-stu-id="e1397-127">Expressions in views (for example, in forms)</span></span>
    

