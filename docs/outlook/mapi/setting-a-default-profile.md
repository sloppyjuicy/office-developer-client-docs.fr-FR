---
title: Définition d'un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: f6bf8f88fa3e87ae619fa32d759fc182290998ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339310"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="9a8aa-103">Définition d'un profil par défaut</span><span class="sxs-lookup"><span data-stu-id="9a8aa-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="9a8aa-104">**S’applique à** : Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a8aa-105">Le profil par défaut est le profil qui est utilisé si vous n'en spécifiez pas explicitement dans l'appel à [MAPILogonEx](mapilogonex.md), en définissant à la place l'indicateur MAPI_USE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="9a8aa-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="9a8aa-106">**Pour établir un profil par défaut**</span><span class="sxs-lookup"><span data-stu-id="9a8aa-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="9a8aa-107">Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d'interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="9a8aa-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="9a8aa-108">Appeler [IProfAdmin:: SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="9a8aa-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="9a8aa-109">**SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime le paramètre pour le profil par défaut précédent.</span><span class="sxs-lookup"><span data-stu-id="9a8aa-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

