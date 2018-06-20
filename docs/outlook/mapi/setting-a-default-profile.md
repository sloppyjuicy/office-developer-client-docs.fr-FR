---
title: Définir un profil par défaut
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1d1e862d-ba49-48a1-bb51-0af861323b7b
description: 'Derni�re modification�: samedi 23 juillet 2011'
ms.openlocfilehash: ea21e735dba8690a392629b92b636b834d7d57d7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787126"
---
# <a name="setting-a-default-profile"></a><span data-ttu-id="0c5c1-103">Définir un profil par défaut</span><span class="sxs-lookup"><span data-stu-id="0c5c1-103">Setting a Default Profile</span></span>

  
  
<span data-ttu-id="0c5c1-104">**S’applique à**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0c5c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0c5c1-105">Le profil par défaut est le profil qui est utilisé si vous ne pas spécifiez explicitement dans l’appel de [MAPILogonEx](mapilogonex.md), définition de l’indicateur MAPI_USE_DEFAULT à la place.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-105">The default profile is the profile that is used if you do not explicitly specify one in the call to [MAPILogonEx](mapilogonex.md), setting instead the MAPI_USE_DEFAULT flag.</span></span>
  
 <span data-ttu-id="0c5c1-106">**Pour établir un profil par défaut**</span><span class="sxs-lookup"><span data-stu-id="0c5c1-106">**To establish a default profile**</span></span>
  
1. <span data-ttu-id="0c5c1-107">Appelez la fonction [MAPIAdminProfiles](mapiadminprofiles.md) pour récupérer un pointeur d’interface **IProfAdmin** .</span><span class="sxs-lookup"><span data-stu-id="0c5c1-107">Call the [MAPIAdminProfiles](mapiadminprofiles.md) function to retrieve an **IProfAdmin** interface pointer.</span></span> 
    
2. <span data-ttu-id="0c5c1-108">Appelez [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span><span class="sxs-lookup"><span data-stu-id="0c5c1-108">Call [IProfAdmin::SetDefaultProfile](iprofadmin-setdefaultprofile.md).</span></span> <span data-ttu-id="0c5c1-109">**SetDefaultProfile** définit la propriété **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) pour le nouveau profil par défaut et supprime la définition pour le profil par défaut précédente.</span><span class="sxs-lookup"><span data-stu-id="0c5c1-109">**SetDefaultProfile** sets the **PR_DEFAULT_PROFILE** ([PidTagDefaultProfile](pidtagdefaultprofile-canonical-property.md)) property for the new default profile and removes the setting for the previous default profile.</span></span>
    

