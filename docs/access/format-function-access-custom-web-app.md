---
title: Fonction Format (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 550fc235-f0b9-4d8e-805b-ce467821a8c9
description: Renvoie une valeur de mise en forme selon un modèle spécifié.
ms.openlocfilehash: 974b56ab8e6bc3f97c1931ba67ca9cd08c3511c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19781845"
---
# <a name="format-function-access-custom-web-app"></a><span data-ttu-id="022e9-103">Fonction Format (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="022e9-103">Format Function (Access custom web app)</span></span>

<span data-ttu-id="022e9-104">Renvoie une valeur de mise en forme selon un modèle spécifié.</span><span class="sxs-lookup"><span data-stu-id="022e9-104">Returns a value formatted according to a specified pattern.</span></span>
  
> [!NOTE]
> <span data-ttu-id="022e9-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="022e9-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="022e9-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="022e9-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="022e9-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="022e9-107">Syntax</span></span>

 <span data-ttu-id="022e9-108">**Format** (*Expression*, *Format*)</span><span class="sxs-lookup"><span data-stu-id="022e9-108">**Format** (*Expression*, *Format*)</span></span> 
  
<span data-ttu-id="022e9-109">La fonction **Format** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="022e9-109">The **Format** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="022e9-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="022e9-110">**Argument name**</span></span>|<span data-ttu-id="022e9-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="022e9-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="022e9-112">*Expression*</span><span class="sxs-lookup"><span data-stu-id="022e9-112">*Expression*</span></span>  <br/> |<span data-ttu-id="022e9-113">Expression d’un type de données pris en charge pour mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="022e9-113">Expression of a supported data type to format.</span></span>  <br/> |
| <span data-ttu-id="022e9-114">*Format*</span><span class="sxs-lookup"><span data-stu-id="022e9-114">*Format*</span></span>  <br/> | <span data-ttu-id="022e9-115">Un modèle de format.</span><span class="sxs-lookup"><span data-stu-id="022e9-115">A format pattern.</span></span> <span data-ttu-id="022e9-116">L’argument format doit contenir une chaîne de format valide, sous la forme d’une chaîne de format standard (par exemple, « C » ou « D ») ou un modèle de caractères personnalisés pour les dates et les valeurs numériques (par exemple, « MMMM dd, yyyy (dddd) »).</span><span class="sxs-lookup"><span data-stu-id="022e9-116">The format argument must contain a valid format string, either as a standard format string (for example, "C" or "D"), or as a pattern of custom characters for dates and numeric values (for example, "MMMM dd, yyyy (dddd)").</span></span> <span data-ttu-id="022e9-117">Pour plus d’informations, consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="022e9-117">For more information, see Remarks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="022e9-118">Remarques</span><span class="sxs-lookup"><span data-stu-id="022e9-118">Remarks</span></span>

<span data-ttu-id="022e9-119">Pour le paramètre *Format* , vous pouvez passer des chaînes qui correspondent à un des modèles suivants :</span><span class="sxs-lookup"><span data-stu-id="022e9-119">For the  *Format*  parameter, you can pass strings that match any of the following patterns:</span></span> 
  
- [<span data-ttu-id="022e9-120">Chaînes de Format numérique standard</span><span class="sxs-lookup"><span data-stu-id="022e9-120">Standard Numeric Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/dwhawy9k%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="022e9-121">Chaînes de Format numérique personnalisé</span><span class="sxs-lookup"><span data-stu-id="022e9-121">Custom Numeric Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/0c899ak8%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="022e9-122">Chaînes de Format de Date et heure standard</span><span class="sxs-lookup"><span data-stu-id="022e9-122">Standard Date and Time Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/az4se3k1%28v=vs.110%29.aspx)
    
- [<span data-ttu-id="022e9-123">Chaînes de Format de Date et heure</span><span class="sxs-lookup"><span data-stu-id="022e9-123">Custom Date and Time Format Strings</span></span>](http://msdn.microsoft.com/en-us/library/8kb3ddd4%28v=vs.110%29.aspx)
    
<span data-ttu-id="022e9-124">Vous ne pouvez pas utiliser la fonction **Format** dans les domaines suivants d’Access 2013 web applications :</span><span class="sxs-lookup"><span data-stu-id="022e9-124">You cannot use the **Format** function in the following areas of Access 2013 web apps:</span></span> 
  
- <span data-ttu-id="022e9-125">Colonnes calculées au niveau de la table</span><span class="sxs-lookup"><span data-stu-id="022e9-125">Calculated columns at the table level</span></span>
    
- <span data-ttu-id="022e9-126">Macros de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="022e9-126">UI macros</span></span>
    
- <span data-ttu-id="022e9-127">Expressions dans les affichages (par exemple, dans les formulaires)</span><span class="sxs-lookup"><span data-stu-id="022e9-127">Expressions in views (for example, in forms)</span></span>
    

