---
title: Fonction Update (application Web personnalisée Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Renvoie une valeur indiquant si une opération d'insertion ou de mise à jour a été tentée sur le champ spécifié.
ms.openlocfilehash: 20e1b87be857f302f36244a6733625dc477da912
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410916"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="a90d3-103">Fonction Update (application Web personnalisée Access)</span><span class="sxs-lookup"><span data-stu-id="a90d3-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="a90d3-104">Renvoie une valeur indiquant si une opération d'insertion ou de mise à jour a été tentée sur le champ spécifié.</span><span class="sxs-lookup"><span data-stu-id="a90d3-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a90d3-105">La fonctionnalité de stockage cloud décrite dans cet article n’est plus prise en charge dans Office 2013 et Office 2016 et peut entraîner le message d’erreur suivant : > *Sorry, we’re having server problems, so we can’t add \<service\> right now. Please try again later.* (« Nous rencontrons actuellement des problèmes de serveur et nous sommes dans l’incapacité d’ajouter le service. Merci de réessayer ultérieurement. »)</span><span class="sxs-lookup"><span data-stu-id="a90d3-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="a90d3-106">> En ce qui concerne le stockage cloud pour Office Online, Office pour iOS et Office pour Android, consultez notre [programme de partenariat de stockage cloud Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="a90d3-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a90d3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a90d3-107">Syntax</span></span>

 <span data-ttu-id="a90d3-108">**Mettre à jour** (*Colonne*)</span><span class="sxs-lookup"><span data-stu-id="a90d3-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="a90d3-109">La fonction **Update** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="a90d3-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="a90d3-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="a90d3-110">**Argument name**</span></span>|<span data-ttu-id="a90d3-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="a90d3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a90d3-112">*Colonne*</span><span class="sxs-lookup"><span data-stu-id="a90d3-112">*Column*</span></span>  <br/> |<span data-ttu-id="a90d3-113">Nom du champ à vérifier pour une opération d'insertion ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="a90d3-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a90d3-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="a90d3-114">Remarks</span></span>

<span data-ttu-id="a90d3-115">La fonction **Update** renvoie la valeur true, qu'une tentative d'insertion ou de mise à jour ait réussi ou non.</span><span class="sxs-lookup"><span data-stu-id="a90d3-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

