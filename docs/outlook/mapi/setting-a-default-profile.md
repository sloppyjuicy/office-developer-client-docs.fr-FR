---
title: Définition d’un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 2044969cc79990c9f0325fc7934e3426015fdc72
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591771"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="85364-103">Définition d’un profil par défaut</span><span class="sxs-lookup"><span data-stu-id="85364-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="85364-104">**S’applique à**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="85364-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="85364-105">Le profil par défaut est le profil qui est utilisé si vous ne pas spécifiez explicitement dans l’appel de [MAPILogonEx](mapilogonex.md), définition de l’indicateur MAPI_USE_DEFAULT à la place.</span><span class="sxs-lookup"><span data-stu-id="85364-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="85364-106">**Pour établir un profil par défaut**</span><span class="sxs-lookup"><span data-stu-id="85364-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="85364-107">Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="85364-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="85364-108">Appelez [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="85364-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="85364-109">**SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime la définition pour le profil par défaut précédente.</span><span class="sxs-lookup"><span data-stu-id="85364-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

