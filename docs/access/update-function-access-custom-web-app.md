---
title: Fonction de mise à jour (accès personnalisé web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 8a8c52c9-81b9-4d10-b42b-e360c67bcf4e
description: Renvoie si une opération d’insertion ou de mise à jour a été tentée sur le champ spécifié.
ms.openlocfilehash: 1685d9f44bd167571b949a34d6c7b6993e63fbc0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782013"
---
# <a name="update-function-access-custom-web-app"></a><span data-ttu-id="84423-103">Fonction de mise à jour (accès personnalisé web app)</span><span class="sxs-lookup"><span data-stu-id="84423-103">Update Function (Access custom web app)</span></span>

<span data-ttu-id="84423-104">Renvoie si une opération d’insertion ou de mise à jour a été tentée sur le champ spécifié.</span><span class="sxs-lookup"><span data-stu-id="84423-104">Returns whether an INSERT or UPDATE operation was attempted on the specified field.</span></span>
  
> [!NOTE]
> <span data-ttu-id="84423-105">La fonctionnalité de stockage dans le nuage décrite dans cet article n’est plus pris en charge dans Office 2013 et Office 2016 et peut entraîner l’erreur suivante : > *Désolé, nous avons des problèmes de serveur, afin que nous ne pouvons pas ajouter \<service\> maintenant. Réessayez ultérieurement.*</span><span class="sxs-lookup"><span data-stu-id="84423-105">The cloud storage feature described in this article is no longer supported in Office 2013 and Office 2016 and may result in the following error: >  *Sorry, we're having server problems, so we can't add \<service\> right now. Please try again later.*</span></span> <span data-ttu-id="84423-106">> Pour le stockage en nuage pour Office Online, Office pour iOS et Office pour Android, vous pouvez rechercher dans notre [Programme de partenariat de stockage dans le nuage Office](https://dev.office.com/programs/officecloudstorage).</span><span class="sxs-lookup"><span data-stu-id="84423-106">> For cloud storage for Office Online, Office for iOS, and Office for Android, you can look into our [Office Cloud Storage Partner Program](https://dev.office.com/programs/officecloudstorage).</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="84423-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="84423-107">Syntax</span></span>

 <span data-ttu-id="84423-108">**Mise à jour** (*Colonne*)</span><span class="sxs-lookup"><span data-stu-id="84423-108">**Update** (*Column*)</span></span> 
  
<span data-ttu-id="84423-109">La fonction de **mise à jour** contient les arguments suivants.</span><span class="sxs-lookup"><span data-stu-id="84423-109">The **Update** function contains the following arguments.</span></span> 
  
|<span data-ttu-id="84423-110">**Nom de l’argument**</span><span class="sxs-lookup"><span data-stu-id="84423-110">**Argument name**</span></span>|<span data-ttu-id="84423-111">**Description**</span><span class="sxs-lookup"><span data-stu-id="84423-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="84423-112">*Colonne*</span><span class="sxs-lookup"><span data-stu-id="84423-112">*Column*</span></span>  <br/> |<span data-ttu-id="84423-113">Le nom du champ à vérifier pour une opération d’insertion ou de mise à jour.</span><span class="sxs-lookup"><span data-stu-id="84423-113">The name of the field to check for an INSERT or UPDATE operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84423-114">Remarques</span><span class="sxs-lookup"><span data-stu-id="84423-114">Remarks</span></span>

<span data-ttu-id="84423-115">La fonction de **mise à jour** renvoie la valeur TRUE que si la tentative d’insertion ou de mise à jour a réussi.</span><span class="sxs-lookup"><span data-stu-id="84423-115">The **Update** function returns TRUE regardless of whether an INSERT or UPDATE attempt is successful.</span></span> 
  

